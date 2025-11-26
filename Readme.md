# 🔥 Analisis Spasial-Temporal & Clustering Hotspot Karhutla (Sumatera Selatan 2025)

![R](https://img.shields.io/badge/Language-R_%3E=4.3.3-blue.svg?style=for-the-badge&logo=R)
![GeoSpatial](https://img.shields.io/badge/Analysis-Geospatial-green.svg?style=for-the-badge)
![Clustering](https://img.shields.io/badge/Algorithm-K--Means-orange.svg?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success.svg?style=for-the-badge)

> **Pengembangan Fungsi R Terpadu untuk Deteksi Pola dan Zonasi Risiko Kebakaran Hutan dan Lahan.**

---

## 📌 Overview

Project ini mengembangkan **fungsi kustom dalam bahasa R** untuk mengotomatisasi seluruh alur kerja analisis data titik panas (_hotspot_) kebakaran hutan dan lahan (Karhutla). Studi kasus dilakukan di **Provinsi Sumatera Selatan** periode **Januari - Juli 2025** menggunakan data satelit **NOAA-20 (Sensor VIIRS)**.

Fungsi yang dikembangkan mencakup:

1.  **Data Wrangling Otomatis**: Pembersihan dan filtering data satelit mentah.
2.  **Analisis Spasial-Temporal**: Mendeteksi tren bulanan dan pola jam puncak kebakaran.
3.  **Unsupervised Learning**: Penerapan algoritma **K-Means Clustering** untuk zonasi wilayah rawan.
4.  **Validasi Statistik**: Pengujian stabilitas cluster menggunakan metode **Bootstrap Resampling**.

---

## 🎥 Video 

Berikut adalah konten penjelasan fungsi R yang telah dikembangkan beserta penjelasan hasil analisisnya:

[![Watch Video](https://img.shields.io/badge/Klik_Untuk_Tonton_Video-red?style=for-the-badge&logo=youtube&logoColor=white)](https://drive.google.com/file/d/1QhXLBm2ZNdTN2Gd-2I-RD3YN0Vi0woW7/view?usp=sharing)

_(Klik gambar di atas untuk menonton video)_

---

## 📂 Dataset & Laporan Lengkap

Karena batasan ukuran file di GitHub, **Laporan Lengkap (PDF)**, **Kode Program**, dan **Dataset Mentah (.csv/.shp)** dapat diakses melalui tautan berikut:

### 🔗 [Download Full Resources (Google Drive)](https://drive.google.com/drive/folders/1jD-eKMWp-mzBXGQnL-zuW1Hiyw3h6wrl?usp=sharing)

_Link di atas berisi:_

- 📄 `Laporan_3_RB.pdf`: Dokumentasi teknis dan interpretasi hasil lengkap.
- 📊 `fire_archive_J1V-C2_687296.csv`: Data mentah hotspot VIIRS.
- 🗺️ Shapefile Administrasi Sumatera Selatan.

---

## 🛠️ Fitur & Fungsi R yang Dikembangkan

Berikut adalah modul fungsi utama yang dibangun dalam project ini:

| Nama Fungsi                      | Deskripsi                                                                             |
| :------------------------------- | :------------------------------------------------------------------------------------ |
| `load_and_clean_hotspot()`       | Import data, cleaning `NA`, dan filtering berdasarkan threshold **FRP > 1 MW**.       |
| `convert_to_spatial()`           | Konversi data tabular menjadi objek spasial (`sf`) dengan CRS WGS84.                  |
| `analyze_monthly_distribution()` | Agregasi temporal untuk melihat tren kenaikan hotspot bulanan.                        |
| `perform_kmeans_clustering()`    | Algoritma K-Means (k=3) untuk mengelompokkan hotspot berdasarkan kedekatan geografis. |
| `bootstrap_cluster_validation()` | Validasi stabilitas cluster dengan 100x resampling (**CV Result: 1.80%**).            |
| `create_interactive_map()`       | Visualisasi peta interaktif menggunakan `Leaflet`.                                    |

---

## 📊 Key Insights (Hasil Analisis)

Berdasarkan analisis terhadap **2.793 titik hotspot** yang tervalidasi:

### 1. Pola Temporal (Waktu)

- 📈 **Puncak Bulanan:** Terjadi lonjakan eksponensial pada **Juli 2025** dengan 1.404 hotspot (50,2% dari total kejadian).
- ⏰ **Puncak Harian:** Konsentrasi deteksi tertinggi pada pukul **06:00 UTC (13:00 WIB)**, berkorelasi dengan waktu lintas satelit dan suhu maksimum harian.

### 2. Hasil Clustering (Zonasi)

Teridentifikasi **3 Cluster Utama** di Sumatera Selatan:

- 🔴 **Cluster 1 (Pesisir Timur):**
  - _Karakteristik:_ Area gambut & perkebunan.
  - _Insight:_ Intensitas api tertinggi (**Rata-rata FRP 8.73 MW**). Sangat rawan kebakaran besar.
- 🔵 **Cluster 2 (Zona Barat/Perbatasan):**
  - _Karakteristik:_ Dataran tinggi/pegunungan.
  - _Insight:_ Intensitas sedang, jumlah hotspot signifikan (32%).
- 🟢 **Cluster 3 (Tengah-Selatan):**
  - _Karakteristik:_ Campuran pertanian & pemukiman.
  - _Insight:_ **Frekuensi tertinggi** (42.1%), namun intensitas api lebih rendah.

### 3. Validasi Model

Hasil Bootstrap Validation menunjukkan nilai **Coefficient of Variation (CV) sebesar 1.80%** (< 5%), yang berarti struktur cluster yang terbentuk **Sangat Stabil** dan dapat diandalkan untuk pengambilan kebijakan.

---

## 📚 Referensi & Jurnal Terkait

Project ini disusun dengan mengacu pada studi literatur dan jurnal pada tautan berikut:
### 🔗 [Referensi yang digunakan](https://drive.google.com/drive/folders/1BsT6DBLwP5IhEMD0efNfGqOxfS5zcrOW?usp=drive_link)


---

## 👥 Tim Penyusun (Kelompok 3)

Mata Kuliah: **Komputasi Statistika** - **Institut Teknologi Sumatera (ITERA)**

- **Luthfia Laila Ramadhani** (123450004)
- **Feby Angelina** (123450039)
- **Ginda Fajar Riadi Marppaung** (123450103)
- **Muhammad Dzikra** (123450124)

---

_© 2025 Data Science ITERA. All Rights Reserved._

