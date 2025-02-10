# 📊 Sentiment Analysis Capres

## 📌 Deskripsi
Proyek ini bertujuan untuk melakukan **analisis sentimen** terhadap calon presiden (**capres**) berdasarkan data teks.  
Metode yang digunakan mencakup **pra-pemrosesan teks**, **klasifikasi sentimen**, dan **visualisasi hasil**.

## 📂 Struktur Folder
```
sentiment-analysis-capres/
│── data/                # Folder untuk dataset
│── notebooks/           # Folder untuk notebook Jupyter
│── models/              # Folder untuk menyimpan model
│── src/                 # Folder untuk skrip Python
│── README.md            # Dokumentasi proyek
└── requirements.txt      # Dependensi proyek
```

## 🛠️ Instalasi
Pastikan Anda memiliki **Python** dan pustaka yang diperlukan sebelum menjalankan proyek.  
Gunakan perintah berikut untuk menginstal dependensi:
```bash
pip install -r requirements.txt
```

## 🚀 Cara Menggunakan
1. Clone repositori:
   ```bash
   git clone https://github.com/username/sentiment-analysis-capres.git
   ```
2. Masuk ke direktori proyek:
   ```bash
   cd sentiment-analysis-capres
   ```
3. Jalankan notebook Jupyter:
   ```bash
   jupyter notebook notebooks/sentiment-analysis-capres1.ipynb
   ```

## 📊 Proses Analisis Sentimen
Berikut langkah-langkah utama dalam proyek ini:
✅ **Pengumpulan data** dari berbagai sumber  
✅ **Pra-pemrosesan teks**, termasuk tokenisasi dan stopword removal  
✅ **Pembuatan model machine learning** untuk klasifikasi sentimen  
✅ **Evaluasi performa model**  
✅ **Visualisasi hasil sentimen**  

## 💡 Contoh Kode
Berikut adalah cuplikan kode utama dari analisis sentimen:
```python
import pandas as pd
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.linear_model import LogisticRegression

# Membaca dataset
df = pd.read_csv("data/sentiment_data.csv")

# Preprocessing teks
vectorizer = TfidfVectorizer(stop_words="indonesian")
X = vectorizer.fit_transform(df["teks"])
y = df["label"]

# Training model
model = LogisticRegression()
model.fit(X, y)

# Prediksi contoh teks
sample_text = ["Capres ini sangat baik dan berkualitas"]
sample_vector = vectorizer.transform(sample_text)
prediction = model.predict(sample_vector)

print("Prediksi Sentimen:", prediction[0])
```
