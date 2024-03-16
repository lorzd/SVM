# SVM
tugas big data
Data diambil dari kagle link : https://www.kaggle.com/datasets/colearninglounge/predicting-pulsar-starintermediate/code. Data berjudul “prediction pulsar star”. Dataset berisi 8 data kontinu dan 1 data diskrit.
1.	Mean of the integrated profile.
2.	Standard deviation of the integrated profile.
3.	Excess kurtosis of the integrated profile.
4.	Skewness of the integrated profile.
5.	Mean of the DM-SNR curve.
6.	Standard deviation of the DM-SNR curve.
7.	Excess kurtosis of the DM-SNR curve.
8.	Skewness of the DM-SNR curve.
9.	Class
Metode yang akan digunakan untuk mengelola data adalah SVM (support vector machine). Kernel yang digunakan adalah kernel linear dan RBF (Radial Basis Function).
Penjelasan kode:
•	Menggunakan metode SVM dengan kernel Linear dan RBF
•	Menggunakan KKN untuk menangani missing value yaitu pada Excess kurtosis of the integrated profile, Standard deviation of the DM-SNR curve, Skewness of the DM-SNR curve
•	Menggunakan metode IQR untuk menangani Outliner yang ada
•	Scaling mengunakan metode fit
Hasil :
•	Dataset menunjukan banyak outliner yang perlu ditangani
•	Metode Kernel RBF menunjukan Tingkat akurasi sebesar 0.9474725274725275 dengan f1-score 0.95
Parameter terbaik menurut Search VC : C =0.18, degree=2, gamma=0.5, random_state=42, dan tol=0.01
Nilai ROC AUC  0.9469015261680572
•	Metode Linear Menunjukan Tingkat akurasi sebesar 0.9404395604395605 dengan f1-score 0.95
Parameter terbaik menurut Search VC : (C=0.14, degree=5, gamma=0.9, kernel='linear', random_state=42, dan tol=0.01
Nilai ROC AUC = 0.9414437482185044

Hasil analisis menunjukkan bahwa kernel RBF memberikan tingkat akurasi yang lebih tinggi dibandingkan dengan kernel linear, dengan skor akurasi sebesar 0.947 dan nilai ROC AUC mendekati 0.947. Ini menunjukkan bahwa kernel RBF mampu menangkap kompleksitas data lebih baik daripada kernel linear. Parameter terbaik yang ditemukan melalui pencarian grid adalah C=0.18, degree=2, gamma=0.5, dengan random_state=42 dan toleransi 0.01 untuk kernel RBF. Sementara itu, kernel linear menunjukkan akurasi yang sedikit lebih rendah dengan skor akurasi sebesar 0.940 dan nilai ROC AUC sekitar 0.941, dengan parameter terbaik C=0.14, degree=5, gamma=0.9, kernel=‘linear’, random_state=42, dan toleransi 0.01.
