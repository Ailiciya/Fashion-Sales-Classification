# Kelompok: Tim Analisis Penjualan E-Commerce Fashion

## Anggota Tim:
- **Kevin Rizki Irawan** (Ketua Tim, NIM: 22.11.4870)
- **Marco Ganius** (Data Analyst, NIM: 22.11.4899)

## Klasifikasi Data Penjualan E-Commerce Fashion Menggunakan Machine Learning

Proyek ini memanfaatkan Machine Learning dengan Apache Spark ML untuk menganalisis dan mengklasifikasikan data penjualan dari e-commerce fashion. Tujuan utama adalah memahami pola diskon, harga produk, dan tren penjualan untuk memberikan wawasan yang dapat diimplementasikan dalam pengambilan keputusan bisnis.

## Daftar Isi
1. [Pendahuluan](#pendahuluan)
2. [Deskripsi Dataset](#deskripsi-dataset)
3. [Metodologi](#metodologi)
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
5. [Model Machine Learning](#model-machine-learning)
6. [Metrik Evaluasi](#metrik-evaluasi)
7. [Hasil dan Wawasan](#hasil-dan-wawasan)
8. [Lampiran](#lampiran)
---

## Pendahuluan
Proyek ini bertujuan untuk mengklasifikasikan data penjualan berdasarkan diskon tinggi (lebih dari 50%) menggunakan beberapa algoritma Machine Learning, termasuk Random Forest, Gradient Boosted Tree, Logistic Regression, dan Decision Tree. Proyek ini berfokus pada pengolahan data e-commerce fashion yang mencakup harga asli (MRP), harga jual, dan diskon.

## Deskripsi Dataset
Dataset yang digunakan diambil dari [Kaggle](https://www.kaggle.com/datasets/mukuldeshantri/ecommerce-fashion-dataset). Dataset ini berisi informasi penjualan e-commerce fashion, meliputi:
- **MRP**: Harga asli produk.
- **SellPrice**: Harga jual produk.
- **Discount**: Persentase diskon pada produk.
- **BrandName**: Nama merek produk.
- **Category**: Kategori produk.

Dataset ini diperbarui hingga 4 tahun terakhir untuk memastikan relevansi dengan tren terbaru.

## Metodologi
1. **Pengumpulan Data**: Dataset diimpor dari Kaggle.
2. **Pre-Processing Data**:  
   - Menghapus nilai kosong (null).  
   - Mengonversi tipe data kolom seperti `MRP` dan `SellPrice` ke format numerik.  
   - Menambahkan kolom baru bernama `HighDiscount` untuk mengklasifikasikan produk dengan diskon tinggi (>50%).  
3. **Exploratory Data Analysis (EDA)**:
   - Menggunakan grafik batang, pie chart, dan visualisasi lainnya untuk memahami data.
4. **Pengembangan Model Machine Learning**:
   - Menggunakan algoritma Random Forest, Gradient Boosted Tree, Logistic Regression, dan Decision Tree.
   - Evaluasi model menggunakan metrik seperti AUC, akurasi, F1-Score, presisi, dan recall.
5. **Hyperparameter Tuning**:
   - Menentukan parameter terbaik untuk model dengan performa tertinggi.

## Exploratory Data Analysis (EDA)
Visualisasi yang dilakukan:
1. **Grafik Batang**: Menampilkan merek dan kategori dengan harga jual tertinggi.
2. **Pie Chart**: Distribusi maksimum diskon berdasarkan kategori.
3. **Line Plot**: Diskon maksimum per kategori produk.
4. **Visualisasi Diskon**: Analisis hubungan antara merek dan diskon.

## Model Machine Learning
Model yang digunakan dalam proyek ini:
1. **Random Forest Classifier**: Model berbasis ensemble untuk klasifikasi.
2. **Gradient Boosted Tree Classifier**: Model dengan pendekatan boosting.
3. **Logistic Regression**: Model linier untuk klasifikasi biner.
4. **Decision Tree Classifier**: Model berbasis pohon keputusan.

## Metrik Evaluasi
Model dievaluasi menggunakan beberapa metrik untuk mengukur performa klasifikasi. Berikut adalah metrik yang digunakan untuk menilai hasil model:

1. **AUC (Area Under the ROC Curve)**  
   - AUC mengukur kemampuan model untuk membedakan antara kelas positif dan negatif. Nilai AUC yang lebih tinggi menunjukkan model yang lebih baik dalam membedakan kedua kelas.

2. **Akurasi**  
   - Akurasi menghitung persentase prediksi yang benar dari total data. Ini adalah metrik yang paling umum digunakan, meskipun bisa kurang efektif jika data tidak seimbang.

3. **F1-Score**  
   - F1-Score adalah rata-rata harmonis dari presisi dan recall. Ini adalah metrik yang berguna untuk dataset yang tidak seimbang, karena mempertimbangkan false positives dan false negatives.

4. **Presisi**  
   - Presisi mengukur seberapa banyak prediksi positif yang benar di antara seluruh prediksi positif. Ini menunjukkan kemampuan model untuk menghindari false positives.

5. **Recall**  
   - Recall mengukur seberapa banyak data positif yang berhasil terdeteksi oleh model di antara semua data positif yang ada. Ini membantu mengukur seberapa banyak informasi yang hilang pada model.

Model terbaik dipilih berdasarkan kombinasi dari metrik-metrik ini, dengan mempertimbangkan konteks dan kebutuhan dari masalah bisnis yang dihadapi.

### Evaluasi Model
Model dievaluasi berdasarkan:
- **AUC (Area Under ROC Curve)**  
- **Akurasi**  
- **F1-Score**  
- **Presisi dan Recall**

### Hyperparameter Tuning
Hyperparameter tuning dilakukan untuk model Random Forest dan Gradient Boosted Tree menggunakan grid search dan cross-validation. Parameter yang disesuaikan meliputi:
- **Random Forest**: `numTrees`, `maxDepth`
- **Gradient Boosted Tree**: `maxIter`, `maxDepth`

## Hasil dan Wawasan
1. **Performa Model**:
   - **Random Forest** dan **Gradient Boosted Tree** memberikan hasil terbaik berdasarkan AUC dan F1-Score.
   - Logistic Regression dan Decision Tree menunjukkan performa lebih rendah dibandingkan model berbasis ensemble.
2. **Karakteristik Model**:
   - Random Forest cocok untuk data yang memiliki banyak variabel kategorikal.
   - Gradient Boosted Tree memberikan hasil optimal untuk data yang tidak seimbang.
3. **Wawasan Bisnis**:
   - Merek dan kategori dengan diskon tinggi cenderung memiliki penjualan lebih tinggi.
   - Pola harga dan diskon dapat digunakan untuk strategi pemasaran.

## Lampiran

 - Dataset: E-Commerce Fashion Dataset [Kaggle](https://www.kaggle.com/datasets/mukuldeshantri/ecommerce-fashion-dataset)
 - Notebook Colab: Google Colab [Google Colab](https://colab.research.google.com/drive/18wNjw-FoVbG33Iq3kQvzNLLUXJrCWepR?usp=sharing)
 - Launchinpad [Launchinpad](https://launchinpad.com/project/analisis-dan-klasifikasi-diskon-produk-pada-dataset-e-commerce-fashion-menggunakan-spark-ml-84be5f9)
