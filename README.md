# Analisis Sentimen Ulasan Produk E-Commerce Amazon

Menggunakan Model **IBM Granite (ibm-granite/granite-3.3-8b-instruct)**

## 📌 Deskripsi Proyek

Proyek ini bertujuan untuk menganalisis sentimen ulasan produk pada
platform e-commerce Amazon menggunakan model **IBM Granite**, salah satu
Large Language Model (LLM) terbaru. Dengan memanfaatkan AI, analisis ini
memberikan wawasan mengenai persepsi pelanggan secara lebih akurat
dibanding metode tradisional seperti Naive Bayes, SVM, atau LSTM.

Dataset yang digunakan adalah **Amazon Reviews Dataset** yang diambil
dari
[Kaggle](https://www.kaggle.com/datasets/bittlingmayer/amazonreviews).

## 🎯 Tujuan

-   Mengklasifikasikan ulasan pelanggan menjadi kategori **positif**,
    **negatif**, atau **netral**.\
-   Menghasilkan **insight dan rekomendasi bisnis** berdasarkan
    distribusi sentimen.\
-   Menunjukkan kemampuan IBM Granite dalam pemrosesan bahasa alami
    untuk analisis e-commerce.

## 🛠️ Tools & Teknologi

-   Python (Google Colab)\
-   Pandas & Matplotlib (data processing & visualisasi)\
-   LangChain + Replicate API\
-   Model: **ibm-granite/granite-3.3-8b-instruct**

## 📂 Dataset

Dataset yang digunakan berasal dari Kaggle:\
🔗 [Amazon Reviews Dataset
(Kaggle)](https://www.kaggle.com/datasets/bittlingmayer/amazonreviews)

## 🚀 Langkah Analisis

1.  **Load dataset** dari file fastText `.txt`.\
2.  **Preprocessing data**: mapping label ke `positive` / `negative`.\
3.  **Klasifikasi sentimen** dengan model **IBM Granite**.\
4.  **Evaluasi performa**: akurasi model dibanding label asli.\
5.  **Generasi insight & rekomendasi** dengan bantuan LLM.\
6.  **Visualisasi distribusi sentimen** dalam bentuk grafik.

## 📊 Hasil Analisis

-   **Distribusi Sentimen**: mayoritas ulasan bernuansa positif.\
-   **Akurasi Model**: 96%.\
-   **Insight Utama**: pelanggan cenderung puas, meskipun masih ada
    ulasan negatif yang perlu ditindaklanjuti.

### Visualisasi

Distribusi sentimen hasil prediksi:

![sentiment-distribution](assets/sentiment_distribution.png)

## 💡 Insight & Rekomendasi

-   Pelanggan menunjukkan **bias positif** terhadap produk.\
-   Perusahaan perlu **menangani ulasan negatif** untuk meningkatkan
    kepuasan.\
-   **Testimoni positif** dapat dimanfaatkan dalam strategi pemasaran.\
-   **Monitoring berkelanjutan** penting untuk menjaga kualitas produk.

## 📌 Kesimpulan

Penggunaan **IBM Granite** terbukti efektif dalam analisis sentimen
ulasan e-commerce dengan hasil akurat dan insight yang relevan.
Pendekatan ini dapat membantu perusahaan dalam pengambilan keputusan
berbasis data, meningkatkan pengalaman pelanggan, dan memperkuat
strategi bisnis.
