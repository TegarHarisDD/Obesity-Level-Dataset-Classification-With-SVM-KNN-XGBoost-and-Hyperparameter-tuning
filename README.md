## 1. EDA (Exploratory Data Analysis)
- Dataset terdiri dari 2.111 baris dan 17 kolom, dengan variabel target `NObeyesdad` yang merepresentasikan tingkat obesitas.
- Ditemukan beberapa masalah: tipe data tidak konsisten (banyak kolom numerik terbaca sebagai object), adanya nilai hilang (`?`), ketidakseimbangan kelas pada target, dan outlier pada beberapa fitur numerik.

## 2. Data Cleaning
- Nilai `?` diganti dengan NaN, lalu seluruh data duplikat dan nilai hilang dihapus.
- Kolom numerik dikonversi ke tipe float setelah pembersihan karakter tidak valid.
- Outlier pada kolom `Age`, `Height`, dan `Weight` dihapus menggunakan metode IQR.
- Hasil: Data menjadi bersih, tanpa duplikasi, tanpa missing value, dan outlier utama telah diatasi.

## 3. Preprocessing Data
- Fitur kategorikal diubah menjadi numerik dengan Label Encoding.
- Fitur numerik dinormalisasi menggunakan MinMaxScaler.
- Data dibagi menjadi data latih dan data uji dengan proporsi 80:20 serta stratifikasi label target.
- Ketidakseimbangan kelas pada data latih diatasi menggunakan SMOTE sehingga distribusi kelas menjadi seimbang.

## 4. Pemodelan dan Machine Learning
- Tiga model digunakan: SVM, KNN, dan XGBoost.
- Model XGBoost memberikan akurasi tertinggi sebelum tuning, diikuti oleh KNN dan SVM.

## 5. Evaluasi Hasil
- Evaluasi dilakukan menggunakan akurasi dan classification report.
- XGBoost menunjukkan performa terbaik, diikuti oleh KNN dan SVM.
- Visualisasi confusion matrix memperlihatkan prediksi model pada masing-masing kelas.

## 6. Hyperparameter Tuning
- GridSearchCV digunakan untuk mencari parameter terbaik pada SVM, KNN, dan XGBoost.
- Setelah tuning, semua model mengalami peningkatan akurasi, terutama SVM dan KNN.
- XGBoost tetap menjadi model dengan performa terbaik.

---
## Hasil Akurasi
| Model   | Akurasi Sebelum Tuning | Akurasi Setelah Tuning | Parameter Terbaik                                                 |
| ------- | ---------------------- | ---------------------- | ----------------------------------------------------------------- |
| SVM     | 0.82298                | 0.93770                | {'C': 10, 'gamma': 'scale', 'kernel': 'linear'}                   |
| KNN     | 0.83851                | 0.88560                | {'metric': 'manhattan', 'n\_neighbors': 3, 'weights': 'distance'} |
| XGBoost | 0.96894                | 0.97090                | {'learning\_rate': 0.2, 'max\_depth': 5, 'n\_estimators': 100}    |

---

**Kesimpulan Umum:**  
Proses EDA, cleaning, preprocessing, dan balancing data sangat penting untuk memastikan kualitas data sebelum pemodelan. Model XGBoost dengan hyperparameter tuning memberikan hasil terbaik untuk klasifikasi tingkat obesitas pada dataset ini. Pipeline yang sistematis dari EDA hingga tuning terbukti meningkatkan performa model secara signifikan.
