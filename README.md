# Resume Project

Anggota Kelompok 10:
1. QHAULAN SYAQHILA
2. GEVANO KEVIN RAVENSY
3. NAZILA IMKANI
4. ADHYATMIKA EKA SAPUTRA


## Data Understanding

Trashnet adalah dataset yang digunakan untuk tugas klasifikasi citra sampah. Dataset ini biasanya berisi gambar dari berbagai jenis sampah yang dikategorikan ke dalam beberapa kelas. Tujuan utama dari dataset ini adalah untuk memungkinkan pembangunan model machine learning yang dapat mengklasifikasikan jenis sampah.

Kategori umum dalam Trashnet biasanya mencakup paper, plastic, glass, metal, dan cardboard. Namun, dalam kasus ini, hanya tiga kategori yang digunakan: paper, plastic, dan trash.

Jumlah Data

Total jumlah data yang digunakan adalah 300 gambar.

Data dibagi menjadi tiga kelas:
- Paper: 100 gambar
- Plastic: 100 gambar
- Trash: 100 gambar

### Preprocessing

langkah preprocessing:

Remove Background: Menghapus latar belakang untuk fokus pada objek utama.
Grayscale: Mengonversi gambar berwarna menjadi hitam-putih.
Normalization: Menormalkan nilai piksel ke rentang [0, 255].
Equalization: Meningkatkan kontras dengan ekualisasi histogram.
Mean Filtering: Menghaluskan gambar menggunakan mean filter.

### Feature Selection

Fitur tekstur dari GLCM dipilih karena mereka dapat menangkap informasi penting tentang pola dan distribusi intensitas piksel dalam gambar, yang sangat relevan untuk tugas klasifikasi citra sampah. Fitur-fitur yang diekstraksi meliputi:

Contrast: Mengukur intensitas lokal yang kuat di dalam gambar.
Dissimilarity: Mengukur perbedaan lokal di dalam gambar.
Homogeneity: Mengukur keseragaman distribusi piksel.
Energy: Mengukur tekstur yang seragam dan berulang.
Correlation: Mengukur korelasi antara piksel yang berdekatan.
ASM (Angular Second Moment): Mengukur keseragaman tekstur.
Entropy: Mengukur ketidakteraturan tekstur.


## Evaluation
Evaluasi yang digunakan adalah menggunakan model KNN, SVM, dan random forest.

# JUDUL
_SISTEM KLASIFIKASI SAMPAH DALAM MENDUKUNG PENGOLAHAN LIMBAH DENGAN METODE_

# LATAR BELAKANG
Pengelolaan limbah merupakan tantangan utama di masyarakat modern akibat volume sampah yang terus meningkat. Seiring bertambahnya populasi dan aktivitas manusia, jumlah sampah yang dihasilkan semakin besar dan kompleks, menyebabkan masalah lingkungan serius seperti pencemaran tanah, air, dan udara, serta dampak negatif terhadap kesehatan manusia. Upaya untuk mengelola limbah secara efisien dan efektif menjadi sangat penting. Salah satu pendekatan untuk meningkatkan efisiensi pemilahan limbah adalah dengan memanfaatkan teknologi pengolahan citra digital, yang memungkinkan pengenalan dan klasifikasi berbagai jenis sampah secara otomatis, sehingga proses pemilahan dapat dilakukan lebih cepat dan akurat dibandingkan dengan cara manual. Sistem klasifikasi sampah berbasis teknologi pengolahan citra digital diharapkan dapat mendukung upaya daur ulang dan mengurangi jumlah sampah yang berakhir di tempat pembuangan akhir (TPA).

Dataset TrashNet merupakan salah satu dataset yang digunakan untuk mengembangkan sistem klasifikasi sampah. Dataset ini berisi gambar berbagai jenis sampah yang telah diklasifikasikan ke dalam enam kategori utama, yaitu Paper (Kertas), Glass (Kaca), Plastic (Plastik), Metal (Logam), Cardboard (Karton), dan Trash (Sampah Umum). Setiap gambar dalam dataset ini memiliki label yang sesuai dengan jenis sampahnya, sehingga dapat digunakan untuk melatih dan menguji model pembelajaran mesin. Dalam penelitian ini, kami mengembangkan sistem klasifikasi sampah menggunakan berbagai teknik pengolahan citra dan algoritma pembelajaran mesin.

Proses pengembangan sistem ini meliputi beberapa tahap. Pertama, pengumpulan data citra dilakukan dengan mengambil gambar dari dataset TrashNet dan memastikan distribusi data yang seimbang untuk setiap kategori sampah. Kedua, serangkaian tahap pra-pemrosesan diterapkan, termasuk resize citra, penghapusan latar belakang, konversi ke grayscale, normalisasi, ekualisasi histogram, dan mean filter untuk meningkatkan kualitas citra yang akan dianalisis. Ketiga, metode Gray-Level Co-occurrence Matrix (GLCM) digunakan untuk mengekstraksi fitur-fitur tekstur penting dari citra yang telah diproses. Keempat, Principal Component Analysis (PCA) diterapkan untuk mereduksi dimensi fitur yang diekstraksi, sehingga model pembelajaran mesin dapat dilatih lebih efisien dan risiko overfitting berkurang. Terakhir, beberapa model klasifikasi seperti K-Nearest Neighbors (KNN), Support Vector Machine (SVM), dan Random Forest dilatih pada data yang telah diproses, serta performa masing-masing model dievaluasi menggunakan metrik akurasi, precision, recall, dan F1-Score.

Implementasi sistem klasifikasi sampah berbasis teknologi pengolahan citra digital ini diharapkan dapat memberikan kontribusi signifikan terhadap pengelolaan limbah yang lebih baik. Dengan sistem ini, proses pemilahan sampah dapat dilakukan secara otomatis dan lebih efisien, mendukung upaya daur ulang, serta mengurangi jumlah sampah yang berakhir di TPA. Sebagai hasilnya, lingkungan yang lebih bersih dan sehat dapat tercipta, serta masalah pencemaran dan dampak negatif terhadap kesehatan manusia dapat diminimalkan. Pengembangan sistem ini tidak hanya menjadi solusi teknologi bagi pengelolaan limbah, tetapi juga memberikan contoh konkret bagaimana teknologi canggih seperti pengolahan citra digital dan pembelajaran mesin dapat digunakan untuk menyelesaikan masalah lingkungan yang mendesak. Dengan dukungan teknologi ini, diharapkan kesadaran dan partisipasi masyarakat dalam pengelolaan limbah dan daur ulang semakin meningkat, sehingga tujuan lingkungan yang berkelanjutan dapat tercapai.
# MASALAH
_1. Bagaimana menangani data citra yang memiliki latar belakang beragam untuk meningkatkan akurasi klasifikasi?
_2. Bagaimana mengekstraksi fitur dari citra untuk mendapatkan informasi yang bermakna bagi model pembelajaran mesin?
_3. Bagaimana melakukan pra-pemrosesan citra agar model pembelajaran mesin dapat bekerja dengan baik?
_4. Bagaimana memilih dan melatih model klasifikasi yang tepat untuk tugas klasifikasi citra?
# SOLUSI
_1. Menggunakan teknik penghapusan latar belakang (background removal) untuk mengisolasi objek utama dari citra, sehingga fitur yang diekstraksi lebih relevan dan tidak terganggu oleh variasi latar belakang.
_2. Menggunakan metode ekstraksi fitur tekstur seperti Gray-Level Co-occurrence Matrix (GLCM) untuk mendapatkan fitur-fitur penting seperti kontras, ketidaksamaan, homogenitas, energi, korelasi, ASM, dan entropi yang dapat digunakan oleh model pembelajaran mesin untuk membedakan antara kelas-kelas citra.
_3. Melakukan serangkaian tahap pre-processing, termasuk remove background, konversi ke grayscale untuk mengurangi kompleksitas warna, normalisasi untuk menyamakan skala piksel, ekualisasi histogram untuk meningkatkan kontras, dan mean filter untuk mengurangi noise.
_4. Menggunakan beberapa algoritma klasifikasi (seperti K-Nearest Neighbors (KNN), Support Vector Machine (SVM), dan Random Forest) untuk melatih model pada data yang telah diproses, kemudian mengevaluasi performa masing-masing model berdasarkan metrik seperti akurasi, precision, recall, dan F1-Score untuk menentukan model terbaik.