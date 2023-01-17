
# Analisa Performa Bisnis Hotel Menggunakan Visualisasi Data

Link : https://medium.com/@imransutee/analisa-performa-bisnis-hotel-menggunakan-visualisasi-data-6c4ef1492f02

## Latar Belakang

Perkembangan digitalisasi yang cepat, telah menjalar ke berbagai industri yang tentunya membawa keuntungan dan dampak positif termasuk bagi industri perhotelan. Hotel merupakan salah satu sarana pendukung utama yang menunjang dalam bisnis di bidang pariwisata. Berkat kemajuan teknologi telah mengubah pengalaman pelanggan dan membantu perkembangan bisnis perhotelan. Data sains yang merupakan contoh kemajuan teknologi dapat digunakan untuk membantu pihak hotel untuk menganalisis performa bisnisnya. Dalam proyek ini, kita akan mendalami bisnis perhotelan untuk menemukan insight terkait performa bisnis perhotelan. Tujuannya adalah untuk memahami perilaku pelanggan saat melakukan reservasi hotel dan hubungannya dengan tingkat pembatalan hotel. Insight yang ditemukan akan disajikan dalam bentuk visualisasi data yang lebih mudah dipahami dan lebih meyakinkan. [Dataset](https://drive.google.com/uc?id=1VeeJvwMzvhW-_NSTxPqshkkTUGlU6EGU) yang digunakan berasala dari publikasi [Hotel booking demand datasets](https://www.sciencedirect.com/science/article/pii/S2352340918315191) dengan beberapa modifikasi seperti lokasi hotel di indonesia. Penjelasan kolom dalam dataset tersebut sebagai berikut :

**Keterangan** :

-   hotel: Tipe hotel, city hotel atau resort hotel
-   is_canceled: dibatalkan(1) atau tidak dibatalkan(0)
-   lead_time: Jumlah hari yang berlalu antara tanggal masuk pemesanan ke dalam PMS dan tanggal kedatangan
-   arrival_date_year: Informasi tahun kedatangan
-   arrival_date_month: Informasi bulan kedatangan
-   arrival_date_week_number:Informasi minggu kedatangan
-   arrival_date_day_of_month: Informasi tanggal kedatangan
-   stay in_weekend_nights: Jumlah malam weekend (Sabtu atau Minggu) tamu menginap atau memesan untuk menginap di hotel
-   stay in_weekdays_nights: Jumlah malam weekday (Senin sampai Jumat) tamu menginap atau memesan untuk menginap di hotel
-   adults/children/babies: Jumlah orang dewasa/anak-anak/bayi
-   meal: Jenis makanan yang dipesan -> No Meal/Undefined, Breakfast, Dinner, Full board.
-   city: Kota/tempat asal.
-   agent: ID dari travel agency pem-booking
-   company: ID dari perusahaan pem-booking
-   customer_type: Tipe pemesanan -> Personal, Family, Contract, Business
-   reservation_status: Status terakhir pemesanan -> Check-Out, Canceled, No-Show

## Data Preprocessing

Sebelum melakukan analisa, langkah yang pertama kali kita lakukan adalah mempersiapkan data mentah menjadi data yang siap dipakai.

- Mengatasi Missing Value
- Mengganti nilai yang tidak sesuai
- Menghapus data yang tidak diperlukan
- Menghapus data duplikat

## Analisis Pemesanan Hotel Bulanan Berdasarkan Tipe Hotel

![](https://miro.medium.com/max/1050/1*1FmSsOHLfVmdWML-osYNtw.png)

Pemesanan Hotel Bulanan Berdasarkan Tipe Hotel

-   Sekilas, terlihat pelanggan lebih banyak memilih memesan hotel perkotaan dibandingkan dengan hotel resort.
-   Libur paling lama di Indonesia ialah Hari Raya dan Nataru.
-   Pemesanan hotel bertambah signifikan pada bulan yang memiliki lama hari libur banyak, terbukti dengan meningkatnya pemesanan antara mei sampai juli yang merupakan Hari Raya yang bertepatan sekitar bulan Juni dan Juli.
-   Kedua jenis hotel dari januari sampai agustus memiliki pola kenaikan yang sama, namun hotel resort mengalami kenaikan di bulan september, sedangkan hotel perkotaan mengalami sebaliknya.
-   Pada bulan januari hingga maret sedikit yang memesan hotel dapat diasumsikan kemungkinan masa sibuk bekerja.

## Analisis Dampak Durasi Menginap terhadap Tingkat Pembatalan Pemesanan Hotel

![](https://miro.medium.com/max/1050/1*Hxa2tyufSyT19UJchU3aFQ.png)

Grafik Durasi Menginap dengan Tingkat Pembatalan

-   Dilihat dari grafik tingkat pembatalan hotel perkotaan lebih tinggi dari hotel resort.
-   Semakin lama hari menginap semakin tinggi tingkat pembatalan.
-   Tingkat pembatalan paling tinggi pada kedua jenis hotel lebih dari 15 hari.
-   Oleh sebab itu sebaiknya pihak hotel memberikan aturan tegas seperti pemotongan biaya sebagai biaya pembatalan.

# Analisis Dampak Lead Time terhadap Tingkat Pembatalan Pemesanan Hotel

Bisnis hotel biasanya memperbolehkan pelanggan memesan hotel sebelum hari kedatangannya. Jarak waktu pun sangat beragam oleh sebab itu, kita perlu menganalisis bagaimana korelasi antara jarak waktu pemesanan hotel(lead_time) terhadap tingkat pembatalan pemesanan hotel.

![](https://miro.medium.com/max/1050/1*3NY8pTv1i8alqrxg5LTg6A.png)

Grafik Lead Time dengan Tingkat Pembatalan

-   Sekilas terlihat tingkat pembatalan pada hotel perkotaan lebih tinggi daripada hotel resort.
-   Dalam setahun, semakin lama jarak waktu pemesanan semakin tinggi tingkat pembatalannya.
-   Tingkat pembatalan hotel perkotaan naik setiap bulan.
-   Tingkat pembatalan hotel resort hampir stagnan sekitar 30%.
-   Tingkat pembatalan hotel paling kecil berada dalam satu bulan waktu pemesanan.
-   Tingkat pembatalan hotel paling tinggi berada dalam 10–12 bulan pemesanan.
-   Dilihat dari data, maka sebaiknya pihak hotel membatasi jarak waktu pemesanan yang dibolehkan, misalnya tidak boleh lebih dari 30 hari.

## Kesimpulan

Dari hasil analisis diatas dapat diambil kesimpulan sebagai berikut:

-   Pemesanan hotel bertambah signifikan pada bulan yang memiliki lama hari libur banyak, terbukti dengan meningkatnya pemesanan antara mei sampai juli yang merupakan Hari Raya yang bertepatan sekitar bulan Juni dan Juli.
-   Semakin lama durasi menginap yang dipesan semakin tinggi tingkat pembatalan.
-   Semakin lama antara jarak waktu pemesanan dengan hari kedatangan, semakin tinggi tingkat pembatalannya.
-   Saran bisnis yang dapat direkomendasikan yaitu sebaiknya pihak hotel memberikan aturan tegas seperti pemotongan biaya sebagai biaya pembatalan dan membatasi jarak waktu pemesanan yang dibolehkan.
