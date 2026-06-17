# 📊 Pengolahan Sinyal Digital - Operasi Dasar Sinyal & Citra

[![Python Version](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/)
[![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green.svg)](https://opencv.org/)
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Platform-orange.svg)](https://colab.research.google.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Repositori ini berisi serangkaian eksperimen dan implementasi komputasi untuk memenuhi tugas mata kuliah **Pengolahan Sinyal Digital**. Fokus utama proyek ini adalah melakukan eksplorasi matematis dan visualisasi terhadap operasi-operasi dasar pada sinyal 1-Dimensi (1D) dan citra digital 2-Dimensi (2D), serta pembuktian empiris sifat linearitas suatu sistem.

---

## 📌 Daftar Isi
* [Cakupan Eksperimen](#-cakupan-eksperimen)
* [Spesifikasi Teknis & Lingkungan](#-spesifikasi-teknis--lingkungan)
* [Struktur Repositori](#-struktur-repositori)
* [Hasil dan Analisis Utama](#-hasil-dan-analisis-utama)
* [Cara Penggunaan](#-cara-penggunaan)
* [Identitas Pengembang](#-identitas-pengembang)

---

## 🚀 Cakupan Eksperimen

### Bagian A: Operasi Sinyal 1D (Diskrit)
* **A.1 Pembangkitan Sinyal:** Pembuatan sinyal Sinusoidal $x_1[n] = \sin(0.5\pi n)$ dan Unit Step Bergeser $x_2[n] = u[n-5]$.
* **A.2 Penjumlahan Sinyal:** Pengamatan efek *DC Offset* akibat perpaduan dua isyarat diskrit.
* **A.3 Penggeseran Sinyal:** Simulasi *Time-Delay* dan *Time-Advance* menggunakan variasi nilai $k = [-3, 0, 4]$.
* **A.4 Amplifikasi Sinyal:** Analisis pelemahan (*atenuasi*), penguatan (*gain*), dan inversi fase via perkalian skalar $\alpha = [0.5, 1, 2, -1]$.

### Bagian B: Operasi Citra 2D (Spasial)
* **B.1 Eksplorasi Metadata:** Ekstraksi dimensi spasial, tipe data array matriks, serta sebaran nilai intensitas piksel.
* **B.2 Penjumlahan Citra:** Teknik penggabungan (*image blending*) gambar asli dengan pola gradasi sintetis beserta penanganan luapan nilai (*clipping*).
* **B.3 Translasi Citra:** Pergeseran koordinat spasial vertikal, horizontal, dan diagonal menggunakan matriks afinitas OpenCV.
* **B.4 Amplifikasi & Histogram:** Manipulasi tingkat kecerahan (*brightness*) dan kontras citra yang divalidasi melalui grafik distribusi frekuensi piksel (histogram).

### Bagian C: Uji Sistem Linier
* Pembuktian prinsip superposisi (Asas Homogenitas dan Additivitas) dengan membandingkan dua karakteristik sistem:
  1. Sistem Linier: $T_1(x) = 2x$ (Selisih pengujian = $0.0$)
  2. Sistem Non-Linier: $T_2(x) = x^2$ (Selisih pengujian $\neq 0.0$)

---

## 🛠️ Spesifikasi Teknis & Lingkungan

Proyek ini sepenuhnya dikembangkan menggunakan bahasa pemrograman **Python** di lingkungan **Google Colab Notebook**. Library utama yang digunakan meliputi:

* **OpenCV (`cv2`):** Untuk pembacaan, manipulasi matriks gambar, dan transformasi afinitas spasial.
* **NumPy (`np`):** Untuk komputasi numerik, pembuatan array sinyal diskrit, dan kalkulasi batas *clipping* matriks.
* **Matplotlib (`plt`):** Untuk visualisasi plot batang diskrit (`stem`), penampilan citra, dan penggambaran grafik histogram.

---

## 📂 Struktur Repositori

```text
├── assets/                  # File gambar pendukung & dokumentasi grafik
├── docs/                    # Laporan PDF formal hasil eksekusi eksperimen
├── notebook/
│   └── operasi_sinyal_citra.ipynb  # File Jupyter Notebook utama (source-code)
└── README.md                # Dokumentasi utama repositori
