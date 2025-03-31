# Fesmaro-Big-Data
Deskripsi Proyek

Proyek ini bertujuan untuk membangun model prediksi Order Profit Per Order guna mendukung optimasi rantai pasok dan logistik. Dengan memahami pola keuntungan berdasarkan pesanan, perusahaan dapat menyesuaikan strategi pengadaan, distribusi, dan penyimpanan stok agar lebih efisien.

Dataset yang digunakan berasal dari DataCo Smart Supply Chain Dataset, yang mencakup informasi transaksi, pengiriman, pelanggan, serta pesanan. Data ini memungkinkan analisis prediktif untuk optimasi logistik, prediksi permintaan, dan klasifikasi perilaku pelanggan.

Metode yang Digunakan

Proyek ini menggunakan pendekatan Machine Learning dengan berbagai model regresi, termasuk:

LightGBM (LGBMRegressor)

Model berbasis Gradient Boosting Decision Trees yang dioptimalkan dengan Bayesian Optimization menggunakan Hyperopt.

Menggunakan parameter seperti num_leaves, learning_rate, n_estimators, dan lainnya.

Dilengkapi dengan early stopping untuk menghindari overfitting.

XGBoost (XGBRegressor)

Model berbasis Extreme Gradient Boosting yang dirancang untuk menangani hubungan non-linear dalam data.

Menggunakan metrik RMSE dan early stopping dalam proses pelatihan.

CatBoost (CatBoostRegressor)

Model berbasis Gradient Boosting yang dioptimalkan untuk menangani fitur kategorikal dengan efisien.

Menggunakan early stopping dan konfigurasi parameter seperti iterations, learning_rate, depth, dan l2_leaf_reg.

Stacking Ensemble

Menggabungkan prediksi dari LGBM, XGBoost, dan CatBoost menggunakan ElasticNet sebagai final estimator.

Memanfaatkan kombinasi regularisasi L1 dan L2 untuk meningkatkan akurasi prediksi.

Data yang Digunakan

Dataset yang digunakan mencakup berbagai fitur yang berkontribusi terhadap prediksi Order Profit Per Order, termasuk:

Fitur Numerik: Order Item Total, Order Item Quantity, Order Item Profit Ratio, Shipping Delay, Total Discount, Distance.

Fitur Kategorikal: Order Region, Shipping Mode, Market, Order Day of Week, Order Month, Season, Delay Category, Customer Segment, Order Status.

Evaluasi Model

Evaluasi model dilakukan menggunakan metrik:

Mean Absolute Error (MAE)

Root Mean Squared Error (RMSE)

R-squared (R²)

Proses optimasi hyperparameter dilakukan untuk meningkatkan kinerja model serta mengurangi kesalahan prediksi.

Cara Menjalankan Proyek

Persiapan Data

Lakukan preprocessing pada dataset dengan menangani nilai NaN dan mengubah fitur kategorikal ke dalam format numerik jika diperlukan.

Pelatihan Model

Jalankan skrip pelatihan untuk masing-masing model (LGBM, XGBoost, CatBoost).

Lakukan optimasi hyperparameter untuk mendapatkan konfigurasi terbaik.

Evaluasi dan Stacking Ensemble

Bandingkan hasil prediksi setiap model dengan menggunakan metrik evaluasi.

Lakukan stacking ensemble untuk menggabungkan kekuatan dari masing-masing model.

Kesimpulan

Dengan pendekatan berbasis Machine Learning dan Ensemble Learning, proyek ini memberikan model prediksi yang lebih akurat dalam memperkirakan keuntungan per pesanan. Dengan hasil ini, perusahaan dapat mengoptimalkan strategi rantai pasok untuk meningkatkan efisiensi operasional serta profitabilitas.

