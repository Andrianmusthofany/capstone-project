# Sentiment Analysis & Summarization of Amazon Product Reviews

Project Overview

Proyek ini merupakan bagian dari Capstone Project – Data Classification and Summarization Using IBM Granite.
Tujuan proyek adalah untuk menganalisis review produk Amazon dengan menggunakan pendekatan Machine Learning klasik dan AI Large Language Model (LLM) IBM Granite untuk mendapatkan insight yang lebih dalam.

Objectives
- Mengklasifikasi sentimen review produk (positive, neutral, negative).  
- Meringkas review panjang menjadi insight singkat yang mudah dipahami.  
- Membandingkan hasil antara **ML Baseline (Logistic Regression)** dengan **IBM Granite (LLM)**.  
- Memberikan rekomendasi actionable untuk meningkatkan kualitas produk & kepuasan pelanggan.  

Dataset
- Sumber: Dataset review produk Amazon (1465 data)  
- Fitur utama:
  - Product info: `product_name`, `category`, `discounted_price`, `actual_price`  
  - Review info: `review_title`, `review_content`, `rating`  
  - User info: `user_id`, `review_id`  
- Dataset sudah melalui preprocessing: normalisasi harga, rating, dan pembuatan label sentimen.

Analysis Process
1. **Preprocessing**  
   - Bersihkan kolom harga, rating, review text  
   - Buat label sentimen:  
     - Rating ≥ 4 → Positive  
     - Rating = 3 → Neutral  
     - Rating < 3 → Negative  

2. **EDA (Exploratory Data Analysis)**  
   - Distribusi rating & sentimen  
   - Visualisasi kategori produk  

3. **ML Baseline (Logistic Regression)**  
   - TF-IDF Vectorizer + Logistic Regression  
   - Evaluasi: Classification report + confusion matrix  

4. **AI Granite (LLM)**  
   - Summarization review (1 kalimat)  
   - Sentiment classification (positive/neutral/negative)  
   - Bandingkan hasil dengan ML baseline  

Insight & Findings
- Mayoritas review bersifat **positif** (±70%).  
- **ML Baseline**: mampu klasifikasi dasar, akurasi ±XX%, namun kesulitan pada review campuran (*mixed sentiment*).  
- **IBM Granite**: lebih konsisten, mampu **merangkum review + memahami konteks**.  
- Tema utama dari review:  
  - Kelebihan → **fast charging, harga terjangkau**  
  - Kekurangan → **durability (cepat rusak)**  

---

Recommendations
1. Tingkatkan **durability produk** → material lebih kuat + garansi.  
2. Optimalkan **strategi diskon** → kombinasikan dengan peningkatan kualitas.  
3. Buat **customer feedback loop** → kumpulkan insight untuk iterasi produk.  
4. Tingkatkan **customer service** → respon cepat meningkatkan kepuasan.  
5. Tambahkan variasi produk → bundle kabel pendek & panjang.  

---

AI Support Explanation
- **ML Baseline (Logistic Regression + TF-IDF):**  
  - Klasifikasi sentimen sederhana berdasarkan teks review.  

- **IBM Granite LLM (`ibm-granite/granite-3.3-8b-instruct`):**  
  - Digunakan untuk **classification & summarization**.  
  - Memberikan insight yang lebih kaya, seperti *“Durable but stopped working after 2 months”*.  
  - Nilai tambah AI: kemampuan memahami konteks & merangkum review.  


Author
-Andrian Musthofany Akhyar 
