# 🏭 Studi Kasus Mandiri 1: Eksplorasi Data Produksi Harian Pabrik

Proyek mandiri ini berfokus pada penerapan analisis data eksploratif (*Exploratory Data Analysis*) pada data operasional lini mesin pabrik komponen otomotif (`factory_production.csv`). Tujuannya adalah untuk membantu manajemen pabrik menggali pola tersembunyi terkait efisiensi shift kerja, faktor penyebab kecacatan produk, serta kebutuhan pemeliharaan preventif (*preventive maintenance*).

---

## 📂 Alur Kerja Proyek & Langkah Analisis

1. **Memuat Dataset:** Mengimpor pustaka esensial (`pandas`, `numpy`, `matplotlib`, `seaborn`) dan memuat data operasional harian yang mencakup 8 kolom utama (`Tanggal`, `Shift`, `Mesin`, `Jumlah_Produksi`, `Jumlah_Cacat`, `Downtime`, `Suhu_Mesin`, `Kelembaban`).
2. **Inspeksi Awal:** Memeriksa struktur data menggunakan `df.info()`, statistik deskriptif dengan `df.describe()`, serta pengecekan nilai kosong (*missing value*) menggunakan `df.isnull().sum()`.
3. **Pembersihan & Imputasi Data:** Mengatasi nilai kosong pada kolom `Downtime`, `Suhu_Mesin`, dan `Kelembaban` menggunakan metode imputasi **median** agar keutuhan baris data tetap terjaga dan tahan terhadap *outlier*.
4. **Visualisasi Data & EDA:**
   * **Visualisasi 1 (Histogram):** Menampilkan distribusi durasi waktu henti (*downtime*) mesin yang menunjukkan kecenderungan *right-skewed*.
   * **Visualisasi 2 (Boxplot):** Membandingkan sebaran jumlah produk cacat berdasarkan shift kerja (Pagi, Siang, Malam).
   * **Visualisasi 3 (Scatter Plot):** Menganalisis hubungan antara suhu operasional mesin (*Suhu_Mesin*) dan jumlah produk cacat (*Jumlah_Cacat*).

---

## 🛠️ Tech Stack
* **Python**
* **Pandas & NumPy** (Manipulasi & Pembersihan Data)
* **Matplotlib & Seaborn** (Visualisasi Statistik)

---

## 💡 Temuan Utama & Insight Bisnis
* **Downtime:** Sebagian besar gangguan mesin berdurasi singkat (di bawah 20 menit), namun terdapat beberapa anomali durasi tinggi yang memerlukan perhatian khusus.
* **Shift Kerja:** Shift malam menunjukkan variasi sebaran data dan jumlah produk cacat yang lebih tinggi dibandingkan shift pagi dan siang.
* **Suhu Mesin:** Terdapat korelasi positif antara suhu operasional dan jumlah produk cacat, di mana suhu di atas 90°C cenderung memicu lonjakan unit cacat.
* **Rekomendasi Manajemen:** Meningkatkan perawatan preventif (*preventive maintenance*), memperketat pengawasan pada shift malam, dan menjaga kestabilan suhu mesin operasional.

---

## 🚀 Cara Menjalankan
1. Pastikan file dataset `factory_production.csv` berada dalam satu direktori dengan notebook.
2. Buka file `.ipynb` menggunakan **Jupyter Notebook** atau **Google Colab**.
3. Jalankan sel kode secara berurutan.
