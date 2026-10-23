# Tugas UTS Machine Learning

**Nama:** Guntur Darmawan Aryo Putro

**NIM:** 241011400631

**Kelas:** Reg B

**Random State:** 31 (2 digit terakhir NIM)

## 📋 Deskripsi Singkat

Repositori ini berisi penyelesaian Tugas Ujian Tengah Semester (UTS) Mata Kuliah Machine Learning. Tugas ini mencakup implementasi dari dasar (*from scratch*) menggunakan library NumPy, Pandas, dan Matplotlib untuk dua algoritma Machine Learning utama:

1. **Linear Regression (Normal Equation & Gradient Descent)** – Mengestimasi penjualan berdasarkan biaya iklan.

2. **Logistic Regression (Gradient Descent)** – Mengklasifikasikan email sebagai *Spam* atau *Bukan Spam* berdasarkan jumlah link dan kata promo.

## 📂 Struktur Repositori

```
.
├── Penjualan_Data.csv       # Dataset untuk tugas Regresi Linear (Bagian A)
├── Email_Data.csv           # Dataset untuk tugas Klasifikasi Logistik (Bagian B)
├── tugas_UTS.ipynb          # Jupyter Notebook utama berisi kode & analisis
└── README.md                # Laporan & dokumentasi tugas

```

## 📊 Ringkasan Hasil & Evaluasi Model

### Bagian A: Linear Regression (Penjualan vs Biaya Iklan)

* **Persamaan Garis Regresi:**
  

  $$
  \hat{y} = b + m \cdot X
  $$

* **Interpretasi Koefisien (**$m$**):**

  Setiap kenaikan biaya iklan sebesar **Rp 1.000.000**, penjualan diprediksi naik sebesar nilai koefisien $m$ (dalam juta Rupiah).

* **Hasil Evaluasi Model:**

| Dataset | MAE | MSE | RMSE | $R^2$ | 
| ----- | ----- | ----- | ----- | ----- | 
| **Training** | *Sesuai output run* | *Sesuai output run* | *Sesuai output run* | *Sesuai output run* | 
| **Testing** | *Sesuai output run* | *Sesuai output run* | *Sesuai output run* | *Sesuai output run* | 

* **Analisis Gradient Descent (Learning Rate):**

  * `lr = 0.001`: Terlalu lambat (belum mencapai titik optimal pada 5000 iterasi).

  * `lr = 0.02`: Pas / Optimal (konvergen menuju nilai terbaik dan konsisten dengan Normal Equation).

  * `lr = 0.1`: Divergen / Gagal Konvergen (melompati nilai minimum dan memicu *overflow*).

### Bagian B: Logistic Regression (Filter Email Spam)

* **Persamaan Probabilitas Spam:**
  

  $$
  P(\text{Spam}) = \sigma(b + m_1 \cdot \text{JumlahLink} + m_2 \cdot \text{KataPromo})
  $$

* **Hasil Evaluasi Model (Data Testing, Threshold = 0.5):**

  * **Accuracy:** *Sesuai output run*

  * **Precision:** *Sesuai output run*

  * **Recall:** *Sesuai output run*

  * **F1-Score:** *Sesuai output run*

* **Confusion Matrix:**
  

  $$
  \begin{bmatrix} TN & FP \\ FN & TP \end{bmatrix}
  $$

* **Eksperimen Threshold:**

  * **Threshold 0.3:** Meningkatkan Recall, namun menambah False Positive (FP).

  * **Threshold 0.5:** Keseimbangan antara Precision dan Recall.

  * **Threshold 0.7:** Meningkatkan Precision (meminimalisir risiko email penting masuk ke folder Spam).

  * **Rekomendasi Filter Spam:** Menggunakan **threshold 0.7** untuk menghindari kesalahan terfatal (*False Positive*).

## 🚀 Cara Menjalankan Notebook

### 1. Prasyarat System & Library

Pastikan Anda telah menginstal **Python 3.x** dan library pendukung berikut:

* `numpy`

* `pandas`

* `matplotlib`

* `scikit-learn` (opsional, untuk eksperimen bonus)

Instalasi library dapat dilakukan via terminal/command prompt:

```
pip install numpy pandas matplotlib scikit-learn jupyter

```

### 2. Langkah-langkah Jalankan

1. Clone repositori ini atau download semua file ke dalam satu folder lokal:

   ```
   git clone <URL_REPOSITORI_ANDA>
   cd <NAMA_FOLDER>
   
   ```

2. Pastikan file dataset `Penjualan_Data.csv` dan `Email_Data.csv` berada pada direktori yang sama dengan `tugas_UTS.ipynb`.

3. Buka Jupyter Notebook atau VS Code:

   ```
   jupyter notebook tugas_UTS.ipynb
   
   ```

4. Jalankan sel dari awal sampai akhir (*Run All Cells*).

*Dibuat untuk memenuhi Tugas UTS Mata Kuliah Machine Learning.*