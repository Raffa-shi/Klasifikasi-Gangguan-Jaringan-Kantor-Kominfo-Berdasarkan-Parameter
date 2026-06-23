<img width="1774" height="887" alt="newbanner" src="https://github.com/user-attachments/assets/ccd0890d-20f0-4f99-8beb-6fcc799a72bf" />

---
<h1 align="center">
Prediksi Gangguan Jaringan Menggunakan Algoritma Random Forest dan Naive Bayes
</h1>

---
<p align="center">
<img src="https://img.shields.io/badge/Python-3.14-blue?logo=python&logoColor=white">
<img src="https://img.shields.io/badge/Flask-Web%20Application-black?logo=flask&logoColor=white">
<img src="https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange?logo=scikitlearn&logoColor=white">
<img src="https://img.shields.io/badge/Pandas-Data%20Analysis-purple?logo=pandas&logoColor=white">
<img src="https://img.shields.io/badge/NumPy-Numerical%20Computing-blue?logo=numpy&logoColor=white">
<img src="https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white">
<img src="https://img.shields.io/badge/Wireshark-Network%20Monitoring-blue?logo=wireshark&logoColor=white">
</p>

---

# Deskripsi Proyek

Penelitian ini bertujuan membangun sistem prediksi gangguan jaringan berbasis website menggunakan algoritma Machine Learning `Random Forest` dan `Gaussian Naive Bayes`.

Sistem memanfaatkan parameter jaringan berupa:

- Bandwidth
- Latency
- Packet Loss
- Uptime

untuk mengklasifikasikan kondisi jaringan menjadi:

- Normal
- Gangguan

Penelitian ini menggunakan metodologi `CRISP-DM (Cross Industry Standard Process for Data Mining)` sebagai kerangka kerja pengembangan model Machine Learning.

---

# Studi Kasus

Dinas Komunikasi dan Informatika Kota Tangerang Selatan

---

# Tujuan Penelitian

- Mengidentifikasi kondisi jaringan berdasarkan parameter monitoring.
- Membandingkan performa algoritma Random Forest dan Naive Bayes.
- Mengimplementasikan model terbaik ke dalam sistem berbasis web menggunakan Flask.
- Membantu proses monitoring dan pengambilan keputusan terkait gangguan jaringan.

---

# Dataset

Dataset dibangun dari hasil monitoring jaringan menggunakan Wireshark yang kemudian melalui proses:

- Data Cleaning
- Feature Engineering
- Severity Scoring
- Clustering Analysis
- Labeling
- Model Training

Parameter yang digunakan:

| Fitur | Deskripsi |
|---------|---------|
| Bandwidth | Kecepatan transfer data |
| Latency | Waktu tunda komunikasi |
| Packet Loss | Persentase kehilangan paket |
| Uptime | Tingkat ketersediaan jaringan |

---

# Metodologi CRISP-DM

## 1. Business Understanding

Identifikasi kebutuhan prediksi gangguan jaringan untuk mendukung proses monitoring jaringan Diskominfo Kota Tangerang Selatan.

## 2. Data Understanding

Eksplorasi dataset hasil monitoring jaringan menggunakan:

- Statistical Summary
- Correlation Analysis
- Distribution Analysis
- Outlier Analysis

## 3. Data Preparation

Tahapan yang dilakukan:

- Missing Value Handling
- Duplicate Removal
- Feature Engineering
- Scaling
- Severity Score Calculation
- K-Means Clustering
- Data Labeling

## 4. Modeling

Model yang digunakan:

### Random Forest

Rumus prediksi Random Forest:

```text
ŷ = mode(h1(x), h2(x), h3(x), ..., hn(x))
```

Keterangan:

- ŷ = hasil prediksi akhir
- h(x) = prediksi masing-masing decision tree
- mode() = voting mayoritas dari seluruh pohon keputusan

### Gaussian Naive Bayes

Teorema Bayes:

```text
P(C|X) = ( P(X|C) × P(C) ) / P(X)
```

Keterangan:

- P(C|X) = probabilitas posterior
- P(X|C) = likelihood
- P(C) = prior probability
- P(X) = evidence
```

Hyperparameter tuning dilakukan menggunakan:

- GridSearchCV
- Cross Validation (CV=5)

## 5. Evaluation

Metrik evaluasi:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Precision Recall Curve
- Confusion Matrix
- Learning Curve

## 6. Deployment

Kedua Model diimplementasikan ke dalam website menggunakan Flask Framework.

---

# Pipeline Sistem

```text
Wireshark
    
Data Collection
    
Data Cleaning
    
Feature Engineering
    
Severity Score
    
K-Means Clustering

Labeling

Train Test Split
Scaling

Random Forest
Naive Bayes

Hyperparameter Tuning
    
Evaluation
    
Model Deployment (Flask)
```

---

# Teknologi yang Digunakan

| Kategori | Teknologi |
|-----------|-----------|
| Programming Language | Python |
| Machine Learning | Scikit-Learn |
| Data Analysis | Pandas |
| Numerical Computing | NumPy |
| Visualization | Matplotlib |
| Visualization | Seaborn |
| Notebook | Jupyter Notebook |
| Deployment | Flask |
| Model Serialization | Joblib |
| Monitoring Data | Wireshark |

---

# Struktur Project

```text
project/
│
├── data/
│   └── labeled_data.csv
│
├── img/
│   └── banner.png
│
├── models/
│   ├── rf_model.pkl
│   ├── nb_model.pkl
│   ├── scaler.pkl
│   └── label_encoder.pkl
│
├── static/
├── templates/
│
├── app.py
├── train_models.py
├── metrics_summary.json
├── requirements.txt
└── klasifikasi_gangguan_jaringan.ipynb
```

---

# Instalasi

## Clone Repository

```bash
git clone https://github.com:Raffa-shi/Klasifikasi-Gangguan-Jaringan-Kantor-Kominfo-Berdasarkan-Parameter.git

cd REPOSITORY
```

---

## Membuat Virtual Environment

Windows:

```bash
python -m venv venv
```

Aktivasi:

```bash
.\venv\Scripts\activate
```

---

## Upgrade Pip

```bash
python -m pip install --upgrade pip
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# Menjalankan Notebook

```bash
jupyter notebook
```

atau

```bash
jupyter lab
```

---

# Training Model

```bash
python train_models.py
```

Output:

```text
models/
├── rf_model.pkl
├── nb_model.pkl
├── scaler.pkl
└── label_encoder.pkl
```

---

# Menjalankan Flask

```bash
python app.py
```

Akses browser:

```text
akan menampilkan localhost
```

---

# Hasil Evaluasi Model

Model evaluasi menggunakan:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC Curve
- Precision Recall Curve
- Confusion Matrix
- Learning Curve

Hasil penelitian menunjukkan bahwa algoritma Random Forest memberikan performa terbaik dibandingkan Gaussian Naive Bayes dalam klasifikasi gangguan jaringan.

---

# Author

Raffa Syahidul Haq Irsi

Program Studi Teknik Informatika

---

# License

Project ini dibuat untuk kebutuhan penelitian akademik dan pengembangan sistem prediksi gangguan jaringan.
