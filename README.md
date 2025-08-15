
# Analisis Sentimen Ulasan E-Commerce Indonesia (Tokopedia)

## 📌 Overview
Proyek ini bertujuan untuk menganalisis sentimen ulasan produk Tokopedia dengan bantuan model **IBM Granite 3.0-2B Instruct** di Google Colab.  
Analisis ini mengklasifikasikan ulasan menjadi **positif**, **netral**, dan **negatif**, kemudian menghasilkan insight untuk perbaikan kualitas produk dan layanan.

---

## 📂 Dataset
- **Sumber**: [Tokopedia Product Reviews – Google Drive](https://drive.google.com/file/d/1jXsB5uh_ugOjxl_5MCtJWB_J3y_NUO42/view?usp=sharing)
- **Jumlah data asli**: 40.607 ulasan
- **Kolom yang digunakan**:
  - `text` → teks ulasan
  - `rating` → rating bintang
  - `category` → kategori produk
  - `product_name` → nama produk
- **Label Emas (Gold Label)** dibuat dari rating:
  - 1–2 ⭐ → negatif
  - 3 ⭐ → netral
  - 4–5 ⭐ → positif

---

## ⚙️ Metodologi
1. **Data Preparation**
   - Pembersihan teks: hapus emoji, tanda baca berlebih, dan URL
   - Konversi rating menjadi label sentimen emas
2. **Model**
   - IBM Granite 3.0-2B Instruct (Hugging Face Transformers)
   - Parameter: `max_new_tokens=96`, `temperature=0.0`
3. **Proses Analisis**
   - Sampling 500 ulasan untuk inference
   - Klasifikasi sentimen
   - Evaluasi hasil dengan label emas
   - Ringkasan insight dari ulasan positif & negatif

---

## 📊 Hasil Evaluasi
- **Classification Report**:
                    precision    recall  f1-score   support

           negatif       0.33      0.57      0.42        14
            netral       0.04      0.59      0.07        27
           positif       0.95      0.12      0.21       459
          
          accuracy                           0.16       500
         macro avg       0.33      0.32      0.18       500
      weighted avg       0.88      0.16      0.21       500

- **Confusion Matrix**:  
*(Tambahkan gambar confusion_matrix.png di repo)*

---

## 🔍 Insight & Temuan
Berdasarkan ringkasan AI:
- **Top Positives**:
  - top kasih
  - top harga
  - top fast response
  - top packaging
  - top quality
  - top performance

- **Top Issues**:
  - beberapa barang habis
  - beberapa barang keterang
  - beberapa barang keterang
  - beberapa barang keterang
  - beberapa barang keterang

---

## 🛠 Rekomendasi
- penjualnya fast response
- penjualnya kualitas barang
- penjualnya fast response
- penjualnya kualitas barang
- penjualnya fast response

---

## 🤖 AI Support
- **Model**: IBM Granite 3.0-2B Instruct
- **Platform**: Google Colab (GPU T4)
- **Peran AI**:
  - *Classification*: Mengklasifikasikan sentimen ulasan
  - *Summarization*: Merangkum insight dan rekomendasi

---

## 📅 Timeline Pengerjaan
- Data cleaning & preparation: 14 Agustus 2025
- Model inference & evaluation: 15 Agustus 2025
- Summarization & insight generation: 16 Agustus 2025

---

## 👤 Kontributor
- Nama: Syalva Audina Pratiwi
- Program: Universitas Diponegoro
- Tahun: 2025
