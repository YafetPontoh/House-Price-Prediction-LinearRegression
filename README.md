# 🏠 House Price Prediction using Linear Regression

Project ini adalah implementasi **Machine Learning** end-to-end untuk memprediksi harga rumah berdasarkan fitur fisik bangunan. Model ini dibangun menggunakan algoritma **Linear Regression** dengan pendekatan Data Science yang terstruktur.

## 📊 Project Overview
* **Dataset:** Ames Housing Dataset (Train/Test Split)
* **Target:** `SalePrice` (Harga Jual Rumah)
* **Model Accuracy (R2 Score):** 0.80 (80%)
* **Main Features:**
    1.  `GrLivArea` (Luas area tempat tinggal di atas tanah)
    2.  `OverallQual` (Kualitas material dan finish rumah)
    3.  `YearBuilt` (Tahun pembangunan)

## 🛠️ Tech Stack
* **Python 3.x**
* **Pandas & NumPy** (Data Manipulation)
* **Matplotlib & Seaborn** (Data Visualization/EDA)
* **Scikit-Learn** (Modeling & Evaluation)

## 🔍 Key Steps in Notebook
1.  **Data Cleaning:** Menangani *Outliers* yang merusak pola regresi (Rumah luas > 4000 sqft tapi harga murah).
2.  **EDA (Exploratory Data Analysis):** Menggunakan Heatmap dan Scatterplot untuk menemukan korelasi antar variabel.
3.  **Feature Engineering:**
    * Mendeteksi kemiringan distribusi harga (*Skewness*).
    * Menerapkan **Log Transformation** (`np.log1p`) untuk menormalkan distribusi target.
4.  **Modeling:** Melatih model Linear Regression.
5.  **Prediction:** Mengembalikan hasil prediksi ke harga asli menggunakan Inverse Log (`np.expm1`).

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
