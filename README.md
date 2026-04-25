<div align="center">
  <h1>🚕 Analisis Text Vectorizer pada Dataset Ulasan Gojek (Bahasa Indonesia)</h1>
  <p>
    <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
    <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white" alt="Scikit-Learn" />
    <img src="https://img.shields.io/badge/Gensim-white?style=flat-square&logo=python&logoColor=3776AB" alt="Gensim" />
    <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white" alt="Pandas" />
  </p>
</div>

<br>

Proyek ini bertujuan untuk mengimplementasikan teknik **Natural Language Processing (NLP)** dalam mengekstraksi fitur dari ulasan pengguna aplikasi Gojek. Fokus utama proyek ini adalah membandingkan efektivitas berbagai metode vektorisasi teks dalam menangani bahasa non-formal (slang) yang sering ditemukan pada ulasan aplikasi di Indonesia.

<hr>

<h1>📦 Informasi Dataset</h1>
Dataset yang digunakan dalam proyek ini bersumber dari Kaggle: 
<a href="https://www.kaggle.com/datasets/ucupsedaya/gojek-app-reviews-bahasa-indonesia" target="_blank">Gojek App Reviews Bahasa Indonesia</a>.

<ul>
  <li><b>File Spesifik:</b> <code>GojekAppReviewV4.0.0-V4.9.3_Cleaned.csv</code></li>
  <li><b>Konten:</b> Ulasan pengguna Gojek versi 4.0.0 hingga 4.9.3 yang telah melalui tahap pembersihan awal (cleaned).</li>
  <li><b>Fitur Utama:</b> Kolom <code>content</code> yang berisi teks ulasan dalam Bahasa Indonesia.</li>
  <li><b>Karakteristik:</b> Dataset mencakup berbagai sentimen pengguna dengan kosa kata yang bervariasi, mulai dari bahasa baku hingga bahasa percakapan sehari-hari.</li>
</ul>

<hr>

<h1>⚙️ Teknik Vektorisasi yang Diimplementasikan</h1>
Proyek ini membandingkan tiga pendekatan berbeda untuk merepresentasikan teks ke dalam format numerik:

<ul>
  <li><b>Bag of Words (BoW):</b> Merepresentasikan teks berdasarkan frekuensi kemunculan kata. Sangat berguna untuk melihat kata apa yang paling sering muncul dalam ulasan pengguna.</li>
  <li><b>TF-IDF (Term Frequency-Inverse Document Frequency):</b> Menghitung bobot kepentingan kata. Metode ini membantu menonjolkan kata-kata unik yang memiliki makna penting bagi ulasan tertentu dan mengabaikan kata umum yang tidak informatif.</li>
  <li><b>Word Embedding (Word2Vec):</b> Menggunakan model neural network untuk menangkap kemiripan makna antar kata. Misalnya, model dapat memahami bahwa kata "aplikasi" dan "apps" berada dalam konteks yang serupa.</li>
</ul>

<hr>

<h1>🚀 Tahapan Proyek</h1>
<ul>
  <li><b>Integrasi Data:</b> Memuat dataset dari Google Drive ke lingkungan Google Colab.</li>
  <li><b>Data Sampling:</b> Mengambil 1.000 sampel ulasan teratas untuk menyeimbangkan kecepatan komputasi dan representasi data.</li>
  <li><b>Ekstraksi Fitur:</b> Menjalankan <code>CountVectorizer</code> (BoW), <code>TfidfVectorizer</code>, dan model <code>Word2Vec</code> (Gensim) pada data ulasan.</li>
  <li><b>Konversi Matriks:</b> Transformasi hasil ekstraksi menjadi format <i>Sparse Matrix</i> (untuk BoW/TF-IDF) dan <i>Dense Matrix</i> (untuk Word2Vec).</li>
  <li><b>Eksportasi:</b> Menyimpan seluruh matriks numerik ke dalam file Excel untuk keperluan analisis statistik lebih lanjut.</li>
</ul>

<hr>

<h1>🔗 Akses Notebook (Google Colab)</h1>
Kamu dapat melihat detail implementasi kode melalui tautan berikut:
<ul>
  <li><b>Proses Vektorisasi:</b> <a href="https://colab.research.google.com/drive/1mvGQn13VFg-hpFRs6TBjkqDEtXHL5jyS" target="_blank">Buka Notebook Training</a></li>
  <li><b>Aplikasi QnA Chatbot:</b> <a href="https://colab.research.google.com/drive/1rXcoKMNh6A3ue_BjvmRsL5xhapqKwEEd" target="_blank">Buka Notebook App</a></li>
</ul>

<hr>

<div align="center">
  <p>Proyek ini dikembangkan sebagai bagian dari Tugas UTS Mata Kuliah Text Mining</p>
  <b>Bagaskara Adhi Pradana - Teknik Informatika ITN Malang</b>
</div>
