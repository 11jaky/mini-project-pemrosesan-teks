# 🇮🇩⚽️ Analisis Sentimen Publik Terhadap PSSI dan Timnas Indonesia

**Nama:** Dzaky Abdur Razaq  
**NIM:** 5220411083  

---

## 📘 Deskripsi Proyek

Proyek ini merupakan studi kasus **Analisis Sentimen Publik terhadap Persatuan Sepak Bola Seluruh Indonesia (PSSI)** dan **Tim Nasional Indonesia (Timnas)** menggunakan data dari media sosial **Twitter (sekarang X)**.  

Data dikumpulkan melalui proses **web scraping**, kemudian diolah melalui serangkaian tahapan **Text Preprocessing** untuk mempersiapkannya menuju tahap **Analisis Sentimen**.  

---

## 🎯 Tujuan dan Ruang Lingkup

- **Fokus Analisis:** Menilai persepsi publik terhadap kata kunci **"PSSI"** dan **"Timnas"**.  
- **Target Data:** Minimal **1000 tweet** dalam Bahasa Indonesia.  
- **Ruang Lingkup:** Meliputi proses **pengambilan data**, **pembersihan teks**, hingga **pembentukan model analisis sentimen**.  

---

## 🛠️ Teknologi dan Lingkungan

Proyek ini menggabungkan berbagai pustaka **Python** serta alat bantu **Node.js** untuk otomasi pengambilan dan pengolahan data.

| Tahapan                            | Alat/Pustaka               | Fungsi Utama                                                                 |
| :---------------------------------- | :------------------------- | :--------------------------------------------------------------------------- |
| **Scraping Data**                   | `tweet-harvest` (v2.6.1)   | Mengambil tweet dari Twitter/X berdasarkan kata kunci tertentu.              |
| **Manipulasi Data**                 | `pandas`                   | Membaca, membersihkan, dan menyimpan dataset ke berbagai format CSV.         |
| **Case Folding**                    | `pandas`                   | Mengubah semua teks menjadi huruf kecil agar seragam.                        |
| **Text Cleaning**                   | `re` (regex)               | Menghapus URL, mention, hashtag, simbol, angka, dan karakter tidak relevan.  |
| **Tokenisasi**                      | `nltk`                     | Memecah teks menjadi unit kata (token).                                     |
| **Stopword & Emoji Removal**        | `Sastrawi`, `re`, `tqdm`   | Menghapus kata umum dan emoji untuk meningkatkan kualitas teks.              |
| **Stemming**                        | `Sastrawi`                 | Mengembalikan kata ke bentuk dasarnya (akar kata).                           |
| **Normalisasi Kata**                | `Sastrawi`, `pandas`       | Mengubah kata tidak baku, slang, singkatan, atau typo menjadi bentuk formal. |
| **N-Gram Analysis (Bigram & Trigram)** | `nltk`, `pandas`           | Mengidentifikasi kombinasi 2–3 kata yang sering muncul bersama.              |
| **Word Cloud Visualization**        | `wordcloud`, `matplotlib`  | Menampilkan frekuensi kata/n-gram dalam bentuk visual menarik.               |
| **Analisis Sentimen**               | _(Tahap berikutnya)_       | Menentukan polaritas (positif, negatif, netral) berdasarkan teks bersih.     |

---

## ⚙️ Konfigurasi Pengambilan Data

Data dikumpulkan menggunakan `tweet-harvest` dengan parameter pencarian sebagai berikut:

| Parameter         | Nilai                              |
| :---------------- | :--------------------------------- |
| **Output File**   | `data_mentah.csv`                  |
| **Jumlah Data**   | 2000 tweet                         |
| **Kata Kunci**    | `PSSI OR Timnas`                   |
| **Rentang Waktu** | 1 September 2025 – 10 Oktober 2025 |
| **Bahasa**        | Indonesia (`lang:id`)              |

---

## 🔄 Alur Pemrosesan Data

Berikut tahapan **preprocessing pipeline** yang diterapkan secara berurutan:

1. **Hapus Duplikat Data**  
   Menghapus tweet yang identik agar analisis tidak bias.  
   > Output: `data_bersih.csv`

2. **Case Folding**  
   Mengubah semua huruf menjadi huruf kecil.  
   > Output: `data_casefolding.csv`

3. **Cleaning Teks**  
   Menghapus URL, mention, hashtag, simbol, angka, dan spasi ganda.  
   > Output: `data_clean.csv`

4. **Tokenisasi**  
   Memecah teks menjadi token/kata.  
   > Output: `data_token.csv`

5. **Stopword & Emoji Removal**  
   Menghapus kata umum dan emoji agar teks lebih bermakna.  
   > Output: `data_filtering.csv`

6. **Stemming**  
   Mengubah kata menjadi bentuk dasarnya (contoh: *bermain → main*).  
   > Output: `data_stemming.csv`

7. **Normalisasi Kata**  
   Mengoreksi kata tidak baku, singkatan, typo, dan slang.  
   > Output: `data_normalisasi.csv`

8. **Bigram & Trigram Generation**  
   Membentuk pasangan dua dan tiga kata untuk analisis konteks.  
   > Output: `data_bigram.csv`, `data_trigram.csv`

9. **Word Cloud Visualization**  
   Menampilkan distribusi kata atau n-gram paling sering digunakan.  
   > Output: `wordcloud_trigram.png`

---

## 📊 Hasil Akhir (sementara)

- Dataset bersih dengan kolom utama `full_text`.  
- Tokenisasi dan n-gram siap digunakan untuk **analisis sentimen lanjutan**.  
- Word cloud menunjukkan kata dominan terkait opini publik terhadap **PSSI** dan **Timnas Indonesia**.  

---

