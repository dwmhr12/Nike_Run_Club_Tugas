# 🏃 Analisis Review Nike Run Club

## 📌 Gambaran Umum

Repositori ini berisi analisis menyeluruh terhadap ulasan pengguna aplikasi **Nike Run Club**, dilakukan melalui lima tahap utama:

1. **Pengumpulan Data (Opsional)**  
   Notebook: `01-nike-run-club-reviews-data-collection.ipynb`  
   - Menggunakan library `google_play_scraper`
   - Target: Aplikasi Nike Run Club (`com.nike.plusgps`)
   - Bahasa: Inggris
   - Hasil disimpan sebagai `data/df_nike_reviews.csv` (total 104.211 ulasan)

2. **Analisis Data Eksplorasi (EDA) Awal**  
   Notebook: `02-nike-run-club-reviews-eda.ipynb`  
   - Analisis distribusi skor, tren waktu, panjang ulasan, kata umum, dan hubungan dengan versi aplikasi

3. **Preprocessing Data**  
   Notebook: `03-nike-run-club-reviews-data-preprocessing.ipynb`  
   - Membersihkan teks: emoji, tanda baca, huruf kecil, kontraksi, ejaan, negasi
   - Tokenisasi, stopword removal, dan lemmatisasi
   - Output: `data/df_nike_reviews2.csv` (dataset bersih)

4. **EDA Setelah Preprocessing**  
   Notebook: `04_EDA_After_Preprocessing_Nike_Run_Club_Review_Analysis.ipynb`  
   - Analisis tren per tahun dan per bulan
   - Word cloud untuk sentimen positif dan negatif

5. **Analisis Sentimen dengan TF-IDF**  
   Notebook: `05-nike-run-club-reviews-tfidf-sentiment-analysis.ipynb`  
   - Analisis sentimen menggunakan TF-IDF
   - Visualisasi polaritas, subjektivitas, scatter plot, dan word cloud

> Proyek ini diimplementasikan menggunakan Python di Google Colab, dengan penyimpanan data melalui Google Drive.

---

## 📁 Struktur Proyek

```
nike-run-club-reviews/
├── data/
│   ├── df_nike_reviews.csv                  # Dataset mentah (opsional)
│   └── df_nike_reviews2.csv                 # Dataset hasil preprocessing
├── notebooks/
│   ├── 01-nike-run-club-reviews-data-collection.ipynb
│   ├── 02-nike-run-club-reviews-eda.ipynb
│   ├── 03-nike-run-club-reviews-data-preprocessing.ipynb
│   ├── 04_EDA_After_Preprocessing_Nike_Run_Club_Review_Analysis.ipynb
│   └── 05-nike-run-club-reviews-tfidf-sentiment-analysis.ipynb
├── README.md
```

---

## 🧰 Persyaratan

### ✅ Python
- Versi: **Python 3.x**

### ✅ Library
- `pandas`
- `numpy`
- `re`
- `string`
- `emoji`
- `contractions`
- `symspellpy`
- `langdetect`
- `matplotlib`
- `seaborn`
- `textblob`
- `wordcloud`
- `nltk`
- `google_play_scraper`
- `tqdm`
- `google-colab` *(jika dijalankan di Colab)*

---

## ⚙️ Instalasi

### 1. Klon Repositori

```bash
git clone https://github.com/<your-username>/nike-run-club-reviews.git
cd nike-run-club-reviews
```

### 2. Instalasi via `requirements.txt`

```bash
pip install -r requirements.txt
```

### 3. (Opsional) Instalasi di Google Colab

Di dalam notebook Colab, jalankan:

```python
!pip install pandas numpy emoji contractions symspellpy langdetect matplotlib seaborn textblob wordcloud nltk google_play_scraper tqdm
```

---

## 📥 Download Resource NLTK

Jalankan ini di awal notebook:

```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
nltk.download('omw-1.4')
```

---

## 🔗 Integrasi Google Drive (untuk Colab)

```python
from google.colab import drive
drive.mount('/content/drive')
```

---

## 🚀 Penggunaan

### 1. Pengumpulan Data (Opsional)

- Jalankan `01-nike-run-club-reviews-data-collection.ipynb`
- Hasil: `data/df_nike_reviews.csv`

### 2. EDA Awal

- Jalankan `02-nike-run-club-reviews-eda.ipynb`
- Lihat statistik awal dan distribusi skor

### 3. Preprocessing

- Jalankan `03-nike-run-club-reviews-data-preprocessing.ipynb`
- Hasil: `data/df_nike_reviews2.csv` (siap digunakan untuk analisis)

### 4. EDA Setelah Preprocessing

- Jalankan `04_EDA_After_Preprocessing_Nike_Run_Club_Review_Analysis.ipynb`
- Analisis tren tahunan, bulanan, dan word cloud

### 5. Analisis Sentimen

- Jalankan `05-nike-run-club-reviews-tfidf-sentiment-analysis.ipynb`
- Model dikembangkan menggunakan TF-IDF dan berbagai classifier
- Output: Akurasi, visualisasi, word cloud, dan metrik evaluasi

---

## 💡 Catatan Tambahan

- Preprocessing mencakup koreksi ejaan, tokenisasi, lemmatisasi, dan negation handling.
- Dataset mentah dan bersih disimpan di folder `data/`.
- Analisis dikembangkan modular melalui lima notebook.
- Visualisasi dan hasil model ditampilkan langsung dalam notebook.

---

## 📬 Kontak

Hubungi melalui email: `dewimaharani170104@gmail.com`  
atau buat *issue* di repositori ini.
