# 🏠 House Price Prediction Advanced Regression

Project ini adalah implementasi **Machine Learning** end-to-end untuk memprediksi harga rumah berdasarkan fitur fisik bangunan. Model ini dibangun menggunakan algoritma **Linear Regression, Random Forest Regressor, dan teknik Fusion dan ** dengan pendekatan Data Science yang terstruktur.

## 📊 Project Overview
* **Dataset:** Ames Housing Dataset (Train/Test Split)
* **Target:** `SalePrice` (Harga Jual Rumah)
* **Model Accuracy (R2 Score):** 0.80 (80%)
* **Main Features:**
    1.  `GrLivArea` (Luas area tempat tinggal di atas tanah)
    2.  `OverallQual` (Kualitas material dan finish rumah)
    3.  `YearBuilt` (Tahun pembangunan)
    4.  'GarageCars' (Bagasi Mobil)
    5.  'FullBath' (Kamar mandi lengkap)
    6.  'Neighborhood' (Lingkungan)
    7.  'KitchenQual' (Kualitas Dapur)

## 🛠️ Tech Stack
* **Python 3.x**
* **Pandas & NumPy** (Data Manipulation)
* **Matplotlib & Seaborn** (Data Visualization/EDA)
* **Scikit-Learn** (Modeling & Evaluation)

## 🏆 Achievement Unlocked
Perjalanan menurunkan Error (RMSLE Score) di Kaggle:
* **Baseline (Linear Regression):** 0.18425
* **+ Feature Engineering (Neighborhood):** 0.16965
* **+ Random Forest Regressor:** 0.16463
* **🚀 Final Ensemble (Fusion):** **0.15800** *(Best Score)*

## 🧠 Approach & Methodology

### 1. Data Processing
* **Handling Outliers:** Menghapus data anomali (GrLivArea > 4000) untuk mengurangi bias.
* **Log Transformation:** Mengubah target `SalePrice` menjadi `log(SalePrice)` agar distribusi data lebih normal.
* **Missing Values:** Mengisi nilai kosong (NaN) dengan 0 atau rata-rata.

### 2. Feature Engineering
Mengubah data mentah menjadi format yang bisa dimengerti mesin:
* **One-Hot Encoding:** Mengubah data kategori (Teks) menjadi angka biner (0/1).
    * *Neighborhood:* Agar model tahu pengaruh lokasi (Elite vs Biasa).
    * *KitchenQual:* Kualitas dapur sangat mempengaruhi harga jual.
* **Numerical Features:** Memasukkan fitur fisik seperti `GrLivArea`, `YearBuilt`, `GarageCars`, dan `FullBath`.

### 3. Modeling Strategy (The Secret Sauce)
Alih-alih hanya menggunakan satu model, project ini menggabungkan kekuatan dua algoritma (**Ensemble**):

* **Model A: Linear Regression**
    * Unggul dalam menangkap pola linear (Harga naik seiring luas tanah bertambah).
    * *Kelemahan:* Kaku, sulit menangkap pola kompleks.
* **Model B: Random Forest**
    * Unggul dalam menangkap pola non-linear dan interaksi antar fitur yang rumit.
    * *Kelemahan:* Cenderung overfitting pada data training.
* **Fusion (Weighted Average):**
    * Menggabungkan prediksi keduanya: `(0.6 * LinearReg) + (0.4 * RandomForest)`.
    * Hasilnya saling melengkapi dan menurunkan error secara signifikan.

## 🚀 How to Run
1.  Clone repository ini.
2.  Install library yang dibutuhkan:
    ```bash
    pip install -r requirements.txt
    ```
3.  Jalankan Jupyter Notebook:
    ```bash
    jupyter notebook
    ```
4.  Buka file `House_Price_Prediction.ipynb`.

## 📈 Result
Model berhasil memprediksi harga rumah dengan akurasi yang solid (**R2 Score > 0.80**) dan bias yang minim pada rentang harga menengah.

---
*Created as part of Data Science Learning Journey.*
