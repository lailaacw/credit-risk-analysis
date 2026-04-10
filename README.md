# Credit Risk Analysis using German Credit Dataset

## Objective
Project ini bertujuan untuk menganalisis faktor-faktor yang mempengaruhi risiko kredit dan membangun model prediksi untuk mengidentifikasi nasabah berisiko (bad credit).

## Dataset
- German Credit Dataset
- 1000 observasi
- 20+ variabel (demografi, kondisi finansial, dan karakteristik kredit)

## Key Findings
- Status rekening (checking account) merupakan faktor paling dominan dalam menentukan risiko kredit  
- Nasabah dengan tabungan rendah (<100 DM) memiliki probabilitas gagal bayar lebih tinggi  
- Durasi kredit yang lebih panjang berkorelasi dengan peningkatan risiko  
- Jumlah kredit (credit amount) yang lebih besar cenderung memiliki variasi risiko yang lebih tinggi  
- Variabel pekerjaan tidak menunjukkan pengaruh signifikan terhadap risiko dibandingkan faktor likuiditas  

## Exploratory Data Analysis (EDA)
Analisis menunjukkan bahwa risiko kredit tidak hanya dipengaruhi oleh satu variabel, tetapi oleh kombinasi beberapa faktor seperti:
- Status rekening + durasi kredit  
- Tabungan + kepemilikan rumah  

Hal ini mengindikasikan adanya hubungan non-linear dalam data.

## Modeling
Dua model digunakan:

- Logistic Regression (untuk interpretabilitas)  
- Random Forest (untuk performa prediksi)  

### Model Performance (ROC-AUC)
- Logistic Regression: ~0.79  
- Random Forest: ~0.79  

Kedua model menunjukkan performa yang kompetitif.
Both Logistic Regression and Random Forest show comparable performance (ROC-AUC ~0.79), with Logistic Regression offering better interpretability.

## Threshold Tuning
Dilakukan penyesuaian threshold untuk meningkatkan kemampuan model dalam mendeteksi nasabah berisiko.

- Default threshold (0.5) cenderung lebih konservatif  
- Threshold 0.4 memberikan trade-off terbaik antara recall dan precision  

Recall untuk kategori bad meningkat secara signifikan tanpa penurunan performa yang drastis.


## Business Insight
- Bank dapat meningkatkan deteksi risiko kredit dengan menyesuaikan threshold keputusan  
- Nasabah dengan saldo rendah dan durasi kredit panjang perlu perhatian khusus  
- Model dapat digunakan sebagai decision support system dalam proses persetujuan kredit  
- Pendekatan ini membantu meminimalkan risiko kerugian akibat kesalahan klasifikasi nasabah berisiko  

## Tools & Libraries
- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib & Seaborn  

## Conclusion
Model yang dibangun mampu mengidentifikasi pola risiko kredit dengan cukup baik.  
Penyesuaian threshold terbukti menjadi faktor penting dalam meningkatkan performa model, khususnya dalam mendeteksi nasabah berisiko tinggi.

## Next Improvement
- Feature engineering tambahan  
- Hyperparameter tuning  
- Implementasi model ke dalam sistem real-time scoring  

