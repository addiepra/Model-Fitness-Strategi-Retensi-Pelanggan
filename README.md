# Model Fitness - Strategi Retensi Pelanggan

Kami, tim Model Fitness, dengan antusias mempersembahkan project "Strategi Retensi Pelanggan." Sebagai waralaba pusat kebugaran yang inovatif, kami terus berkomitmen untuk meningkatkan kualitas layanan kami dan memberikan pengalaman terbaik bagi pelanggan kami.

Salah satu tantangan utama yang kami hadapi adalah fenomena perputaran pelanggan atau customer churn, yang seringkali menjadi isu kritis dalam industri layanan kebugaran. Kami menyadari bahwa melacak dan memahami secara akurat kapan seorang pelanggan benar-benar berhenti menggunakan layanan kami bukanlah tugas yang mudah. Oleh karena itu, kami memandang perlu untuk mengembangkan strategi keterlibatan pelanggan berbasis data analitik untuk mengatasi masalah ini.

Dalam konteks ini, fokus utama proyek ini adalah menganalisis profil pelanggan yang telah kami digitalisasi. Kami percaya bahwa dengan memahami perilaku dan preferensi pelanggan secara lebih mendalam, kami dapat mengidentifikasi pola churn potensial sebelum mereka benar-benar terjadi. Pendekatan ini akan memungkinkan kami untuk merancang strategi retensi pelanggan yang lebih efektif, menyesuaikan pelayanan kami sesuai dengan kebutuhan individual, dan membangun hubungan yang lebih erat dengan setiap anggota komunitas fitness kami.

Melalui proyek ini, kami berharap dapat mengurangi tingkat churn, meningkatkan loyalitas pelanggan, dan pada gilirannya, meningkatkan keberlanjutan bisnis . Dengan dedikasi untuk memberikan pengalaman fitness yang tak terlupakan, kami yakin bahwa pendekatan berbasis data ini akan membawa Model Fitness ke tingkat kesuksesan yang baru. 
## Tujuan
**Tujuan dari project ini yaitu:**

1. Mempelajari cara memprediksi probabilitas churn (untuk bulan berikutnya) bagi setiap pelanggan
2. Membuat segmentasi pengguna dengan memilih kelompok yang paling dominan dan mendeskripsikan fitur-fitur utamanya
3. Menganalisis faktor yang paling memengaruhi churn
4. Menarik kesimpulan dasar dan memberikan rekomendasi terkait cara meningkatkan layanan pelanggan
5. Mengidentifikasi kelompok yang ditargetkan
6. Merekomendasikan langkah-langkah untuk mengurangi churn
7. Mendeskripsikan pola lain yang kamu temui terkait interaksi pelanggan

## Tahapan
**Berikut tahapan yang akan dilakukan antara lain:**

**1. Memuat file data dan pelajari informasi umumnya. File path: `/datasets/gym_churn_us.csv`**

**2. Melakukan analisis data eksploratif (EDA):**
- Perhatikan dataset yang tersedia, apa ada fitur yang hilang?󠀲󠀡󠀥󠀥󠀧󠀨󠀣󠀠󠀳󠀰 Pelajari nilai rata-rata dan standar deviasinya (gunakan metode describe()).󠀲󠀡󠀥󠀥󠀧󠀨󠀣󠀡󠀳
- Lihat nilai fitur rata-ratanya dalam dua kelompok, yaitu untuk mereka yang keluar (churn) dan untuk mereka yang tinggal (gunakan metode groupby()).󠀲󠀡󠀥󠀥󠀧󠀨󠀣󠀢󠀳
- Buat histogram dan distribusi fitur untuk mereka yang keluar (churn) serta mereka yang tinggal.󠀲󠀡󠀥󠀥󠀧󠀨󠀣󠀣󠀳
- Buat matriks korelasi dan tampilkan hasilnya.

**3. Membangun model untuk memprediksi churn pengguna:**
- Bagi datanya menjadi train set dan validation set menggunakan fungsi train_test_split().󠀲󠀡󠀥󠀥󠀧󠀨󠀣󠀨󠀳
- Latih model pada train set dengan dua metode berikut:
  - regresi logistik
  - random forest
- Evaluasi accuracy, precision, dan recall untuk kedua model menggunakan validation set.󠀲󠀡󠀥󠀥󠀧󠀨󠀤󠀢󠀳󠀰 Gunakan metrik-metrik tersebut untuk membandingkan model.󠀲󠀡󠀥󠀥󠀧󠀨󠀤󠀣󠀳󠀰 Model mana yang memberikan hasil terbaik?

**4. Membuat klaster pengguna:**
- Lakukan standardisasi terhadap data.󠀲󠀡󠀥󠀥󠀧󠀨󠀤󠀩󠀳
- Gunakan fungsi linkage() untuk membuat matriks jarak berdasarkan matriks fitur yang telah distandardisasi dan buat grafik dendrogram.󠀲󠀡󠀥󠀥󠀧󠀨󠀥󠀠󠀳󠀰  
- Latih model pengklasteran dengan algoritma K-means dan prediksikan klaster pelanggannya. (Tetapkan jumlah klasternya menjadi n=5 sehingga akan lebih mudah untuk membandingkan hasil yang kamu dapat dengan hasil dari siswa lain.󠀲󠀡󠀥󠀥󠀧󠀨󠀥󠀣󠀳󠀰 Namun ingat ya, di kehidupan nyata tidak akan ada yang memberimu petunjuk seperti itu. Oleh karena itu ke depannya, kamu harus membuat keputusan berdasarkan grafik dari langkah sebelumnya.)󠀲󠀡󠀥󠀥󠀧󠀨󠀥󠀤󠀳
- Lihat nilai rata-rata fitur untuk semua klaster.󠀲󠀡󠀥󠀥󠀧󠀨󠀥󠀥󠀳󠀰 Apa ada yang menarik perhatianmu?󠀲󠀡󠀥󠀥󠀧󠀨󠀥󠀦󠀳
- Buat grafik distribusi fitur untuk setiap klaster.󠀲󠀡󠀥󠀥󠀧󠀨󠀥󠀧󠀳󠀰 Apa kamu memperhatikan sesuatu?
- Hitung tingkat churn untuk setiap klaster (gunakan metode groupby()).󠀲󠀡󠀥󠀥󠀧󠀨󠀥󠀩󠀳󠀰 Apa klaster-klaster tersebut berbeda sehubungan dengan tingkat churn?󠀲󠀡󠀥󠀥󠀧󠀨󠀦󠀠󠀳󠀰 Klaster pelanggan mana yang cenderung akan pergi, dan mana yang akan tetap setia?

**5. Merumuskan kesimpulan dan rekomendasi sederhana untuk bekerja dengan pelanggan.**
