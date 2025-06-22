# 📚 Exploratory Analysis of Book Metadata

## 📖 Project Overview

### **Latar Belakang**
Industri penerbitan buku terus berkembang seiring meningkatnya akses pembaca terhadap berbagai sumber digital. Untuk membantu pemahaman yang lebih baik tentang tren literasi dan produksi buku, analisis data diperlukan untuk menjawab pertanyaan-pertanyaan seperti:
 1. Buku berbahasa apa yang paling umum tersedia?
 2. Penerbit mana yang paling aktif menerbitkan buku?
 3. Genre apa yang paling banyak diproduksi?
Dengan menjawab pertanyaan-pertanyaan tersebut, stakeholder seperti penulis, penerbit, dan pengembang aplikasi buku dapat membuat keputusan berbasis data.

### **Tujuan Proyek**
Tujuan dari proyek ini adalah untuk melakukan eksplorasi awal (Exploratory Data Analysis / EDA) terhadap dataset buku guna memahami karakteristik dasar dari kumpulan data tersebut, khususnya dari segi bahasa buku, penerbit terbanyak, dan genre yang paling umum. Hasil dari EDA ini dapat digunakan sebagai dasar untuk pengembangan sistem rekomendasi buku, pengelompokan pengguna berdasarkan preferensi, atau strategi distribusi konten oleh penerbit.

### **Permasalahan**
Beberapa permasalahan spesifik yang ingin dijawab dalam proyek ini adalah
 1. Bahasa apa yang paling umum digunakan dalam buku-buku di dataset ini?
 2. Penerbit mana yang paling banyak menerbitkan buku?
 3. Genre apa yang paling sering muncul?
Ketiga hal ini merupakan aspek fundamental dalam memahami karakteristik distribusi konten literasi dalam dataset.

### **Pendekatan**
Untuk menjawab permasalahan tersebut, pendekatan eksploratif akan digunakan dengan :
 1. Melihat distribusi frekuensi pada kolom language, publisher, dan genre.
 2. Menyaring dan mengurutkan nilai berdasarkan jumlah kemunculan.
 3. Menyajikan hasil dalam bentuk tabel dan ringkasan statistik tanpa visualisasi.
Pendekatan ini sederhana namun efektif untuk memperoleh wawasan awal dari data secara objektif.

## 🔗 Raw Dataset
Dataset ini berasal dari **Google Books API** dan dilengkapi dengan beberapa entri yang ditambahkan secara manual. Dataset ini berisi informasi detail tentang kumpulan buku dari berbagai **genre**, **bahasa**, dan **periode terbit**.  
Proyek ini dirancang untuk **peneliti, analis data, dan penggemar buku** yang ingin mengeksplorasi **metadata buku**, **tren publikasi**, serta **keterlibatan pembaca** berdasarkan data yang tersedia.
- **Link Dataset**: [Books Dataset on Kaggle](https://www.kaggle.com/datasets/madankhatri123h/books-dataset)
- **Format**: CSV
- **Kolom Utama**: `title`, `author`, `pages`, `genre`, `description`, `published_date`, `publisher`, `language`, `average_rating`, `ratings_count`, `thumbnail`

---

## 🔍 Insight & Findings

### 1. **Bahasa yang Paling Umum Digunakan**
- Mayoritas buku berbahasa Inggris (`en`) sebanyak **1958 buku**.
- Bahasa lainnya seperti Indonesia (`id`), Italia (`it`), dan Spanyol (`es`) hanya sedikit, menandakan ketimpangan distribusi bahasa.

### 2. **Penerbit yang Paling Banyak Menerbitkan Buku**
- **"Unknown Publisher"** mendominasi dengan **532 buku**, menunjukkan kualitas metadata yang rendah.
- Penerbit akademik ternama seperti **Cambridge**, **Oxford**, **Springer**, dan **Routledge** juga termasuk yang paling banyak.

### 3. **Genre yang Paling Sering Muncul**
- Genre paling umum: `Unknown Genre`, `Fiction`, dan `Literary Criticism`.
- Beberapa genre akademik seperti `Education`, `Social Science`, dan `Psychology` juga signifikan.

---

## 📌 Conclusion

Dataset buku ini menunjukkan:
- **Dominasi bahasa Inggris** dan **minimnya buku berbahasa lokal**
- **Banyak entri publisher dan genre tidak diketahui**
- **Kandungan buku akademik cukup tinggi**, didominasi oleh penerbit ternama

---

## 💡 Recommendations

### 🌠 Bahasa:
- Diversifikasi koleksi buku berbahasa non-Inggris (terutama Indonesia dan Spanyol)
- Analisis peluang pasar lokal dari bahasa yang belum tergarap

### 🏢 Penerbit:
- Analisis performa buku per penerbit (berdasarkan rating dan ulasan)
- Kolaborasi strategis dengan penerbit akademik berkinerja tinggi

### 📚 Genre:
- Kurasi koleksi akademik untuk institusi pendidikan
- Buat koleksi khusus genre fiksi atau sastra untuk pembaca umum
- Imputasi genre yang tidak diketahui menggunakan model AI

---

## 🤖 AI Support

### 🧠 1. Language Classification using LLM or Fine-Tuned Model
- **Tujuan**: Mengatasi entri `"Unknown Language"`
- **Metode**: Gunakan model seperti GPT-4 atau mBERT untuk memprediksi bahasa dari `title`, `description`, atau `author`.

### 🧠 2. Genre Classification using LLM or Traditional ML
- **Tujuan**: Mengisi nilai `"Unknown Genre"` secara otomatis
- **Metode**: Gunakan model LLM atau klasifikasi multikelas (SVM, Naive Bayes, Random Forest) berdasarkan teks dari `title` dan `description`.

### ❤️ 3. Sentiment Analysis for Reader Reviews
- **Tujuan**: Menilai kualitas buku berdasarkan ulasan pembaca
- **Metode**: Klasifikasikan sentimen menjadi positif, netral, atau negatif jika terdapat kolom `review` atau `comment`.

