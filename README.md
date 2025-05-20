# 📊 Klasifikasi Tingkat Obesitas dengan SVM, KNN, XGBoost & Hyperparameter Tuning

Proyek ini bertujuan untuk mengklasifikasikan tingkat obesitas individu berdasarkan berbagai fitur gaya hidup dan kebiasaan makan menggunakan algoritma pembelajaran mesin seperti SVM, KNN, dan XGBoost. Proses ini mencakup eksplorasi data, praproses, pelatihan model, dan tuning hyperparameter untuk meningkatkan akurasi prediksi.

## 🗂️ Struktur Proyek

* `ObesityDataSet.csv` — Dataset utama yang digunakan.
* `EDA.ipynb` — Notebook untuk eksplorasi data awal.
* `Klasifikasi.ipynb` — Notebook utama untuk pelatihan model dan evaluasi.
* `models/` — Folder untuk menyimpan model yang telah dilatih.
* `dataset_info.md` — Informasi detail tentang dataset.

## ⚙️ Setting

* Python 3.x
* Jupyter Notebook
* Scikit-learn
* XGBoost
* Pandas & NumPy
* Matplotlib & Seaborn

## 🧪 Langkah-Langkah Analisis

1. **Eksplorasi Data (EDA)**: Analisis distribusi fitur dan deteksi nilai yang hilang.
2. **Praproses Data**: Normalisasi, encoding variabel kategorikal, dan penanganan ketidakseimbangan kelas.
3. **Pelatihan Model**: Implementasi SVM, KNN, dan XGBoost.
4. **Tuning Hyperparameter**: Penggunaan GridSearchCV untuk optimasi parameter model.
5. **Evaluasi Model**: Menggunakan metrik seperti akurasi, precision, recall, dan confusion matrix.

## 📈 Hasil

| No. | Model       | Akurasi |   |
| --- | ----------- | ------- | - |
| 1   | KNN Default | 85.08%  |   |
| 2   | SVM Default | 95.56%  |   |
| 3   | XGB Default | 99.60%  |   |
| 4   | KNN Tuned   | 91.53%  |   |
| 5   | SVM Tuned   | 96.77%  |   |
| 6   | XGB Tuned   | 99.60%  |   |
