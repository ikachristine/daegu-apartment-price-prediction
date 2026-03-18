🏢 Apartment Price Prediction (Machine Learning Project)

**Overview**
Proyek ini bertujuan untuk membangun model machine learning yang dapat memprediksi harga apartemen berdasarkan karakteristik properti dan faktor lokasi. Model ini dirancang sebagai **decision-support tool** untuk membantu proses penentuan harga yang lebih akurat dan berbasis data.

**Business Background**
Pertumbuhan urbanisasi dan keterbatasan lahan di perkotaan meningkatkan kebutuhan akan hunian vertikal seperti apartemen. Dalam praktiknya, penentuan harga apartemen sering dilakukan tanpa analisis data yang komprehensif.

Hal ini menimbulkan risiko:
- Overpricing → properti sulit terjual (time on market tinggi)
- Underpricing → kehilangan potensi keuntungan

**Problem Statement**
Penentuan harga apartemen yang tidak tepat dapat menyebabkan kerugian bisnis dan inefisiensi dalam proses penjualan. Saat ini belum tersedia sistem berbasis data yang dapat membantu memperkirakan harga apartemen secara objektif dan konsisten.

**Objective**
Mengembangkan model prediksi harga apartemen berbasis machine learning untuk:
- Menghasilkan estimasi harga yang akurat
- Membantu penentuan harga yang kompetitif
- Mendukung pengambilan keputusan berbasis data

**Stakeholders**
- **Real Estate Agent**  
  Menentukan harga listing yang kompetitif agar properti lebih cepat terjual
- **Property Owner / Developer**  
  Menetapkan harga jual optimal sesuai kondisi pasar
- **Buyer / Investor**  
  Mengevaluasi kewajaran harga untuk keputusan pembelian/investasi

**Dataset**
Dataset berisi informasi properti apartemen, termasuk:
- Karakteristik fisik (luas, tahun, fasilitas)
- Faktor lokasi (transportasi, fasilitas sekitar)
- Harga aktual (target)
Dataset ini relevan karena fitur-fitur tersebut secara langsung memengaruhi nilai properti di pasar.

**Methodology**
1. Data Cleaning (missing value & duplicate check)
2. Exploratory Data Analysis (EDA)
3. Feature Engineering
   - One-Hot Encoding (data kategorikal tanpa urutan)
   - Ordinal Encoding (data kategorikal berurutan)
4. Modeling (Random Forest Regressor)
5. Hyperparameter Tuning
6. Model Evaluation (MAPE)
7. Model Interpretation (SHAP)

**Model Explanation**
Model yang digunakan adalah **Random Forest Regressor**, yang bekerja dengan membangun banyak decision tree dan menggabungkan hasilnya untuk meningkatkan akurasi serta mengurangi overfitting.
Model ini dipilih karena mampu menangkap hubungan non-linear antar variabel dan cukup robust terhadap variasi data.

**Model Performance**
Model menghasilkan:
**MAPE ≈ 19%**
Interpretasi:
- Error rata-rata sekitar ±19% dari harga aktual
- Dalam konteks real estate:
  - <10% → sangat baik
  - 10–20% → baik / acceptable
  - >20% → perlu perbaikan
Model termasuk kategori **baik**, namun masih dapat ditingkatkan.

**Business Recommendation**
**1. Gunakan Rentang Harga**
Gunakan hasil prediksi dalam bentuk range: **Prediksi ± 19%**
Contoh:
- Prediksi: Rp1.000.000.000  
- Rentang: Rp810.000.000 – Rp1.190.000.000  

**2. Kapan Model Dapat Dipercaya**
- Properti dengan karakteristik umum  
- Data lengkap & sesuai training  
- Harga dalam rentang normal  

**3. Kapan Harus Hati-hati**
- Properti premium / sangat mahal  
- Properti dengan fitur unik  
- Kondisi pasar berubah drastis  

**4. Penggunaan dalam Bisnis**
Model digunakan sebagai: **Decision-support tool**, bukan penentu harga final

**Limitations**
- Tidak semua faktor harga tersedia (misalnya kualitas interior, view, dll)
- Model kurang presisi pada properti high-end
- Tidak mempertimbangkan faktor ekonomi makro

**Future Improvement**
- Menambahkan fitur yang lebih kaya
- Menggunakan model yang lebih kompleks (XGBoost, dll)
- Menambahkan data eksternal (ekonomi, demand pasar)

**Tools & Libraries**
- Python
- Pandas, NumPy
- Scikit-learn
- SHAP
- Matplotlib / Seaborn

**Conclusion**
Model mampu memprediksi harga apartemen dengan performa yang cukup baik (MAPE ~19%) dan dapat digunakan sebagai alat bantu dalam pengambilan keputusan harga. Dengan pendekatan berbasis data, risiko kesalahan penetapan harga dapat dikurangi.
## 👤 Author

Ika Christine Purba
