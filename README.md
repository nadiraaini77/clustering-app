# ✈️ Airline Passenger Segmentation

Aplikasi web untuk melakukan **segmentasi penumpang maskapai** menggunakan algoritma **K-Means Clustering**, dibangun dengan **Streamlit**.

🔗 **Live Demo:** https://clustering-app-cxkre4sgcwb2tcjjjjjrhu.streamlit.app/

---

## 📌 Tentang Project

Project ini bertujuan untuk mengelompokkan penumpang maskapai berdasarkan karakteristik perjalanan, tingkat kepuasan, kualitas layanan, serta pola keterlambatan penerbangan.

Dengan pendekatan **Machine Learning Unsupervised Learning (Clustering)**, penumpang dapat dikelompokkan ke dalam beberapa segmen sehingga maskapai dapat memahami kebutuhan setiap kelompok pelanggan dan menyusun strategi layanan yang lebih tepat sasaran.

Hasil segmentasi menghasilkan 4 kelompok utama:

* **Loyal Satisfied Passenger**
* **Severely Delayed Passenger**
* **Digitally Frustrated Passenger**
* **Delay Sensitive Passenger**

---

## 📈 Model Information

Menggunakan:

* RobustScaler
* Principal Component Analysis (PCA)
* K-Means Clustering

Jumlah Cluster Optimal:

| Model | Cluster |
|---------|---------|
| K-Means | 4 |

---

## 🎯 Segment Description

### 1. Loyal Satisfied Passenger
Penumpang loyal dengan tingkat kepuasan tinggi dan pengalaman perjalanan yang baik.

**Karakteristik:**
- Loyal Customer
- Service Score tinggi
- Digital Experience baik
- Delay rendah

**Rekomendasi:**
- Program loyalitas
- Membership eksklusif
- Reward dan promo khusus

---

### 2. Severely Delayed Passenger
Penumpang yang mengalami keterlambatan penerbangan cukup tinggi.

**Karakteristik:**
- Total delay sangat tinggi
- Tingkat kepuasan rendah
- Risiko churn tinggi

**Rekomendasi:**
- Kompensasi keterlambatan
- Prioritas penanganan operasional
- Peningkatan ketepatan waktu penerbangan

---

### 3. Digitally Frustrated Passenger
Penumpang yang kurang puas terhadap layanan digital maskapai.

**Karakteristik:**
- Online boarding rendah
- Ease of online booking rendah
- Digital experience buruk

**Rekomendasi:**
- Perbaikan aplikasi dan website
- Penyederhanaan proses booking
- Peningkatan user experience

---

### 4. Delay Sensitive Passenger
Penumpang dengan toleransi rendah terhadap keterlambatan.

**Karakteristik:**
- Delay relatif kecil namun memengaruhi kepuasan
- Sensitif terhadap ketepatan waktu

**Rekomendasi:**
- Notifikasi real-time
- Informasi penerbangan yang akurat
- Peningkatan komunikasi kepada penumpang

---

## 🗂️ Struktur Project

```bash
/
├── models/                 # Model clustering yang telah disimpan
├── main.py                 # Main Streamlit Application
├── requirements.txt        # Dependencies
└── README.md
```

---

## 🔄 Workflow Project

```text
Dataset Airline Passenger Satisfaction
              ↓
       Data Cleaning
              ↓
    Feature Engineering
              ↓
      Data Encoding
              ↓
      Robust Scaling
              ↓
             PCA
              ↓
    K-Means Clustering
              ↓
      Cluster Profiling
              ↓
   Streamlit Deployment
```

---

## ⚙️ Feature Engineering

Beberapa fitur baru yang digunakan dalam proses clustering:

| Feature | Description |
|----------|------------|
| total_delay | Total keterlambatan keberangkatan dan kedatangan |
| age_group | Kelompok usia penumpang |
| travel_distance_category | Kategori jarak perjalanan |
| avg_service_score | Rata-rata kualitas layanan |
| avg_digital_score | Rata-rata pengalaman digital |
| avg_comfort_score | Rata-rata kenyamanan perjalanan |
| avg_airport_experience_score | Rata-rata pengalaman di bandara |
| delay_category | Kategori tingkat keterlambatan |

---

## 🚀 Cara Menjalankan Lokal

```bash
# 1. Clone repository
git clone https://github.com/nadiraaini77/clustering-app.git

# 2. Masuk ke folder project
cd clustering-app

# 3. Buat virtual environment
python -m venv venv

# Windows
venv\Scripts\activate

# Mac/Linux
source venv/bin/activate

# 4. Install dependency
pip install -r requirements.txt

# 5. Jalankan aplikasi
streamlit run main.py
```

Aplikasi akan berjalan di:

```text
http://localhost:8501
```

---

## 🌐 Deployment

Aplikasi telah dideploy menggunakan **Streamlit Community Cloud**.

Setiap perubahan pada branch utama dapat digunakan untuk melakukan update aplikasi.

🔗 Live App:

https://clustering-app-cxkre4sgcwb2tcjjjjjrhu.streamlit.app/

---

## 🛠️ Tech Stack

* Python
* Streamlit
* Pandas
* NumPy
* Scikit-Learn
* Joblib
* Plotly
* Matplotlib

---

## 📊 Dataset

Dataset yang digunakan adalah **Airline Passenger Satisfaction Dataset**.

Dataset berisi informasi mengenai:

* Profil Penumpang
* Customer Type
* Type of Travel
* Class
* Flight Distance
* Service Ratings
* Delay Information
* Passenger Satisfaction

### Target Analisis

Melakukan segmentasi pelanggan untuk:

- Mengidentifikasi kelompok penumpang berdasarkan perilaku dan pengalaman perjalanan.
- Mengetahui faktor utama yang memengaruhi kepuasan pelanggan.
- Membantu maskapai menyusun strategi peningkatan layanan.

---

## ⚠️ Catatan

* Model menggunakan pendekatan unsupervised learning sehingga hasil berupa segmentasi pelanggan, bukan prediksi kelas tertentu.
* Segment yang dihasilkan dapat digunakan sebagai dasar strategi bisnis dan peningkatan layanan maskapai.
* Project dibuat untuk tujuan pembelajaran dan analisis data.
