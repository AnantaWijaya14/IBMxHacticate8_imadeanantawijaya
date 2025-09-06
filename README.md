# 📌 Analisis Sentimen Ulasan Produk E-Commerce Amazon menggunakan IBM Granite LLM  

## 📖 Gambaran Proyek  
E-commerce seperti Amazon menghasilkan jutaan ulasan pelanggan setiap hari. Ulasan ini mengandung informasi berharga tentang kepuasan pelanggan, kualitas produk, dan performa layanan. Metode analisis sentimen tradisional seperti Naive Bayes, SVM, atau LSTM sering kali kesulitan menangkap makna kontekstual yang kompleks dalam bahasa alami.  

Pada proyek ini digunakan **Large Language Model (LLM)** — khususnya **ibm-granite/granite-3.3-8b-instruct** — untuk melakukan klasifikasi sentimen pada **Amazon Reviews Dataset** dari Kaggle. Model ini tidak hanya digunakan untuk klasifikasi **positif** atau **negatif**, tetapi juga menghasilkan **analisis insight** dan **rekomendasi bisnis**.  

---

## 🎯 Tujuan  
- Mengklasifikasikan ulasan produk Amazon ke dalam kategori sentimen.  
- Membandingkan prediksi model dengan label asli untuk mengukur akurasi.  
- Menampilkan distribusi sentimen pelanggan.  
- Mengekstrak insight dan memberikan rekomendasi untuk e-commerce.  

---

## 📊 Dataset  
- **Sumber**: [Amazon Reviews Dataset - Kaggle](https://www.kaggle.com/datasets/bittlingmayer/amazonreviews)  
- **Format**: FastText (`.ft.txt`)  
- **Label**:  
  - `__label__1` → Negatif  
  - `__label__2` → Positif  

---

## ⚙️ Tools & Frameworks  
- **Python**  
- **Google Colab**  
- **LangChain**  
- **Replicate API** (akses model IBM Granite)  
- **Pandas**  
- **tqdm**  

---

## 🚀 Cara Menjalankan  

### 1. Instalasi dependensi  
```bash
!pip install -U langchain langchain-community langchain-experimental replicate pandas tqdm
```

### 2. Load dan preprocessing dataset  
```python
df = load_fasttext_file("test.ft.txt")
```

### 3. Jalankan klasifikasi sentimen  
```python
sample_df = df.head(50).copy()
preds = [classify_review(r) for r in sample_df["review"]]
sample_df["predicted_sentiment"] = preds
```

### 4. Evaluasi performa  
```python
print(sample_df[["review", "sentiment_label", "predicted_sentiment"]].head(10))
print("Distribusi:", sample_df["predicted_sentiment"].value_counts())
print("Akurasi:", (sample_df["predicted_sentiment"] == sample_df["sentiment_label"]).mean())
```

### 5. Hasilkan insight & rekomendasi  
```python
insights = llm.invoke(insight_prompt)
recommendations = llm.invoke(recommendation_prompt)
```

---

## 📈 Hasil  
- Distribusi sentimen ulasan (positif vs negatif).  
- Skor akurasi dibandingkan label asli.  
- Insight terkait pola kepuasan pelanggan.  
- Rekomendasi yang dapat ditindaklanjuti untuk e-commerce.  

---

## 🔍 Insight Utama  
- IBM Granite menunjukkan pemahaman kontekstual yang baik terhadap ulasan.  
- Prediksi cukup selaras dengan label asli, menghasilkan akurasi kompetitif.  
- Memberikan **klasifikasi sekaligus insight** yang berguna bagi bisnis.  

---

## 📢 Kesimpulan  
Proyek ini menunjukkan potensi **ibm-granite/granite-3.3-8b-instruct** dalam **analisis sentimen e-commerce**, melampaui pendekatan tradisional dengan menghasilkan **klasifikasi berbasis konteks**, **penjelasan yang mudah dipahami**, serta **rekomendasi bisnis yang relevan**.  

---

## 📌 Sitasi  
Jika menggunakan repositori ini, silakan sitasi dataset:  
> Bittlingmayer, A. (Kaggle, 2020). *Amazon Reviews Dataset*. Tersedia di: [https://www.kaggle.com/datasets/bittlingmayer/amazonreviews](https://www.kaggle.com/datasets/bittlingmayer/amazonreviews)  
