# 🇮🇩 Analisis Sentimen Publik Terhadap PSSI dan Timnas Indonesia

**Nama:** Dzaky Abdur Razaq  
**NIM:** 5220411094

---

## 📘 Deskripsi Proyek

Proyek ini merupakan studi kasus **Analisis Sentimen Publik** terhadap **Persatuan Sepak Bola Seluruh Indonesia (PSSI)** dan **Tim Nasional (Timnas) Indonesia**, dengan memanfaatkan data dari media sosial **Twitter (sekarang X)**.  
Data diperoleh melalui proses _web scraping_ dan diproses menggunakan teknik **Natural Language Processing (NLP)** untuk mendapatkan representasi teks yang siap dianalisis.

---

## 🎯 Tujuan dan Ruang Lingkup

- **Fokus Analisis:** Mengamati persepsi publik terhadap kata kunci **"PSSI"** dan **"Timnas"**.
- **Target Data:** Minimal **2000 tweet** dalam Bahasa Indonesia.
- **Tugas Utama:**
  1. Pengambilan data menggunakan _scraper_ berbasis Node.js.
  2. Implementasi **Case Folding** dalam tahap _text preprocessing_.
  3. Persiapan untuk analisis sentimen menggunakan pustaka NLP.

---

## 🛠️ Teknologi dan Lingkungan

Proyek ini menggabungkan pustaka Python dan alat Node.js untuk setiap tahapan pengolahan data.

| Tahapan                         | Alat/Pustaka             | Fungsi                                                            |
| :------------------------------ | :----------------------- | :---------------------------------------------------------------- |
| **Scraping Data**               | `tweet-harvest` (v2.6.1) | Mengambil data tweet dari Twitter (X).                            |
| **Manipulasi Data**             | `pandas`                 | Mengelola dan membersihkan data tabular.                          |
| **Tokenisasi**                  | `nltk`                   | Memecah teks menjadi kata-kata (tokens).                          |
| **Stemming & Stopword Removal** | `Sastrawi`               | Membersihkan kata umum dan mengembalikan kata ke bentuk dasarnya. |
| **Analisis Sentimen**           | _(Tahap berikutnya)_     | Akan digunakan untuk klasifikasi polaritas teks.                  |

---

## ⚙️ Konfigurasi Pengambilan Data

Data dikumpulkan menggunakan `tweet-harvest` dengan parameter pencarian yang spesifik untuk menjaga relevansi topik.

| Parameter         | Nilai                              |
| :---------------- | :--------------------------------- |
| **Output File**   | `data_mentah.csv`                  |
| **Jumlah Data**   | 2000 tweet                         |
| **Kata Kunci**    | `PSSI OR Timnas`                   |
| **Rentang Waktu** | 1 September 2025 – 10 Oktober 2025 |
| **Bahasa**        | Indonesia (`lang:id`)              |
