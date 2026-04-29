# Laporan Analisis Perancangan Berorientasi Objek (APBO)
## Sistem Pemesanan Meja Mandiri (Self-Ordering System) - Coffee Shop Satukala

**Mata Kuliah:** Analisis Perancangan Berorientasi Objek  
**Dosen Pengampu:** Adi Wahyu Pribadi, S.Si., M.Kom  

---

### 1. Identitas Proyek
* **Nama Sistem:** Satukala Self-Ordering System
* **Studi Kasus:** Coffee Shop Satukala
* **Deskripsi Proyek:** Proyek ini bertujuan untuk merancang dan membangun sebuah sistem pemesanan mandiri (*self-ordering*) berbasis *web mobile* yang dikhususkan untuk operasional Coffee Shop Satukala. Melalui sistem ini, pelanggan tidak perlu lagi antre di kasir, melainkan cukup memindai QR Code yang tersedia di masing-masing meja untuk mengakses e-menu, memesan, hingga menyelesaikan transaksi pembayaran secara digital. Sistem ini juga terintegrasi langsung dengan dasbor karyawan untuk memproses pesanan serta dasbor pemilik (*owner*) untuk keperluan monitoring penjualan dan inventaris secara *real-time*.

* **Tim Pengembang (Anggota Kelompok):**
  1. Shafiq Usman Nurhananto - 4523210103
  2. M Dhafa Fahlevie Hardiansyach - 4523210071
  3. Ciesha Fajar Ramadhan - 4523210031
  4. Fazril Fadilah - 4523210047
  5. Ahmad Farid Akbar - 4523210006

---

### 2. Sasaran Pengguna
Pengembangan sistem pemesanan mandiri ini dirancang secara khusus untuk memfasilitasi tiga kelompok sasaran utama yang terlibat dalam ekosistem operasional Coffee Shop Satukala:
1. **Pelanggan (Customer):** Sebagai *end-user* (pengguna akhir) utama yang membutuhkan kemudahan, kecepatan, dan kenyamanan dalam melakukan pemesanan tanpa harus membuang waktu untuk berdiri dan mengantre panjang, terutama pada jam-jam sibuk.
2. **Kasir / Karyawan (Staff/Barista):** Sebagai pelaksana operasional harian yang membutuhkan sistem yang dapat mengurangi beban kerja pencatatan manual, meminimalisir miskomunikasi dengan pelanggan, dan menyajikan daftar pesanan secara sistematis agar proses pembuatan minuman/makanan menjadi lebih efisien.
3. **Pemilik (Owner):** Sebagai pengambil keputusan bisnis yang membutuhkan transparansi data tingkat tinggi. Pemilik membutuhkan alat untuk memantau performa penjualan, ketersediaan stok, dan menu terlaris kapan saja dan di mana saja tanpa harus bergantung pada rekap manual dari kasir.

---

### 3. Foto Dokumen Wawancara

*(foto dokumentasi saat melakukan observasi dan wawancara dengan pihak Coffee Shop Satukala di sini)*
<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/934acec0-ca8d-4542-9f83-3496dd962e5b" />

---

### 5. Latar Belakang & Alur Bisnis
**Latar Belakang:**
Coffee Shop Satukala merupakan salah satu destinasi yang sangat diminati oleh pelanggan, terutama pada akhir pekan (*weekend*) atau jam pulang kerja. Tingginya antusiasme pelanggan sayangnya tidak diimbangi dengan sistem pemesanan yang memadai. Sistem pelayanan di Satukala saat ini masih sangat konvensional dan terpusat pada satu titik, yaitu meja kasir. Hal ini kerap kali menciptakan *bottleneck* (penumpukan) yang tidak hanya mengurangi kenyamanan ruang dalam cafe, tetapi juga memicu berbagai masalah operasional seperti kesalahan pencatatan dan kelelahan staf.

**Alur Bisnis Saat Ini (Sistem Manual):**
Alur operasional yang berjalan saat ini mewajibkan proses yang cukup panjang dan tidak efisien:
1. Pelanggan yang baru datang harus langsung menuju meja kasir dan berdiri dalam antrean.
2. Saat tiba gilirannya, pelanggan menyebutkan pesanannya secara lisan, dan kasir akan menginputnya secara manual ke dalam sistem *Point of Sales* (POS).
3. Setelah menyelesaikan proses pembayaran (tunai atau kartu), kasir akan memberikan sebuah *stand* nomor meja fisik kepada pelanggan.
4. Pelanggan kemudian mencari meja yang kosong, duduk, dan meletakkan *stand* nomor tersebut di atas meja.
5. Di bagian belakang, barista meracik minuman berdasarkan struk cetak. Setelah selesai, pelayan (karyawan) harus membawa nampan dan berjalan mengelilingi area cafe untuk mencari di mana letak nomor meja pelanggan tersebut berada.

---

### 6. Analisis Kebutuhan Sistem & Identifikasi Masalah
Berdasarkan observasi dan wawancara, kelompok kami mengidentifikasi beberapa masalah krusial yang harus segera diselesaikan:

**Identifikasi Masalah:**
* **Penumpukan Antrean (Bottleneck):** Satu-satunya jalur pemesanan adalah kasir, sehingga pada saat ramai, antrean bisa mengular hingga ke pintu masuk, merusak kenyamanan visual dan spasial cafe.
* **Risiko Human Error Tinggi:** Kebisingan di dalam cafe seringkali membuat kasir salah mendengar pesanan pelanggan (misalnya salah mencatat varian rasa, tingkat kemanisan, atau nomor meja).
* **Kehilangan Potensi Pendapatan (Loss of Sales):** Pelanggan yang sudah duduk nyaman sangat enggan untuk memesan menu tambahan (*upselling* seperti *snack* atau minuman kedua) karena mereka malas jika harus mengantre dari awal lagi.
* **Keterbatasan Monitoring Manajerial:** Pemilik tidak memiliki akses langsung untuk melihat omzet atau pergerakan stok secara *real-time* di pertengahan hari operasional.

**Kebutuhan Sistem (System Requirements):**
Untuk mengatasi permasalahan di atas, sistem yang dirancang harus memiliki kemampuan berikut:
* Mampu mendeteksi lokasi atau nomor meja pelanggan secara otomatis melalui pemindaian QR Code yang unik di setiap meja.
* Menyediakan antarmuka Katalog Digital (E-Menu) yang interaktif, menampilkan gambar produk, harga, deskripsi, serta label ketersediaan stok.
* Mengintegrasikan modul keranjang belanja dan gerbang pembayaran digital (*Payment Gateway* seperti QRIS atau E-Wallet) agar pelanggan bisa melakukan *checkout* mandiri.
* Memiliki sistem notifikasi seketika (*real-time pop-up/alert*) di perangkat kasir atau dapur setiap kali ada pesanan baru yang masuk dan sudah lunas.
* Menyediakan dasbor analitik berbasis *web* khusus untuk pemilik guna melacak histori transaksi dan performa penjualan secara instan.

---

### 7. Analisis Aktor
Dalam arsitektur sistem ini, terdapat tiga entitas aktor yang memiliki hak akses dan fungsionalitas yang berbeda-beda:

1. **Aktor: Pelanggan (Customer)**
   * **Deskripsi Peran:** Pengguna yang berada di garis depan sistem. Mereka menggunakan *smartphone* pribadi mereka untuk berinteraksi dengan aplikasi tanpa perlu mengunduh aplikasi khusus di PlayStore/AppStore atau melakukan *login* yang rumit. Tugas utama aktor ini adalah memindai QR, mengeksplorasi menu, menyesuaikan jumlah pesanan, dan menyelesaikan pembayaran secara otonom.
   
2. **Aktor: Kasir / Karyawan (Staff)**
   * **Deskripsi Peran:** Pengguna operasional yang menggunakan perangkat tablet atau komputer di area *bar/kitchen*. Aktor ini bertugas sebagai penerima informasi. Saat pesanan masuk, mereka memvalidasi pesanan tersebut, meracik pesanan, dan memperbarui status pesanan di sistem dari "Pesanan Baru" menjadi "Sedang Diproses", hingga akhirnya "Selesai/Siap Diantar".

3. **Aktor: Pemilik (Owner)**
   * **Deskripsi Peran:** Pengguna tingkat *Administrator* yang memiliki kendali penuh terhadap basis data (*database*) sistem. Aktor ini tidak menangani pesanan harian secara langsung, melainkan fokus pada manajemen data seperti menambahkan varian menu baru, memperbarui harga, mematikan status menu yang bahan bakunya sedang kosong, serta menganalisis laporan grafik penjualan harian atau bulanan.

---

### 8. Analisis Perbandingan Sistem
Untuk memperjelas nilai tambah (*value proposition*) dari proyek ini, berikut adalah perbandingan antara sistem manual yang saat ini digunakan dengan sistem digital yang kami usulkan:

| Indikator Perbandingan | Sistem Satukala Saat Ini (Manual Konvensional) | Sistem Baru (Self-Ordering System via QR) |
| :--- | :--- | :--- |
| **Metode Pemesanan** | Tersentralisasi: Pelanggan wajib mengantre fisik di depan kasir. | Terdesentralisasi: Setiap meja berfungsi sebagai "kasir virtual" mandiri. |
| **Metode Pembayaran** | Mengandalkan transaksi langsung dengan kasir (Tunai, EDC/Debit). | Terintegrasi dan mandiri melalui perangkat pelanggan (QRIS/E-Wallet). |
| **Tingkat Akurasi (Error)** | Rentan *human error* (salah dengar, salah input ke POS). | Sangat presisi (data diinput dan dikonfirmasi langsung oleh pelanggan). |
| **Pemesanan Tambahan** | Pelanggan harus kembali berdiri dan ikut antrean dari awal. | Cukup membuka *smartphone* di meja, tambah pesanan hanya dalam hitungan detik. |
| **Pelaporan Data (Report)** | Rekapitulasi fisik yang baru bisa dilihat setelah *close shift*. | Data komprehensif, otomatis, dan dapat dipantau detik itu juga oleh Owner. |

---

### 9. Skenario Sistem (Use Case Utama)
Skenario ini menggambarkan alur perjalanan utama ( *Happy Path* / *Normal Flow* ) yang terjadi ketika sistem berjalan dengan sempurna tanpa ada hambatan:

1. Pelanggan tiba di Coffee Shop Satukala dan langsung diarahkan untuk duduk di meja mana saja yang kosong.
2. Di atas meja tersebut terdapat *standee* atau stiker QR Code. Pelanggan membuka kamera *smartphone* dan memindainya.
3. *Browser* di *smartphone* pelanggan secara otomatis terbuka dan menampilkan halaman E-Menu dari sistem Satukala, lengkap dengan informasi bahwa mereka sedang berada di "Meja No. X".
4. Pelanggan asyik menelusuri kategori menu (misal: *Signature Coffee*, *Non-Coffee*, *Pastry*), memilih tingkat kemanisan, dan menekan tombol tambah ke keranjang.
5. Setelah selesai memilih, pelanggan menekan tombol *Checkout* dan memilih untuk membayar menggunakan QRIS (Gopay/OVO/Dana, dll).
6. Segera setelah pembayaran berhasil diverifikasi oleh sistem, data pesanan langsung ditembakkan ke layar monitor di area dapur/bar.
7. Karyawan yang melihat pesanan tersebut segera meraciknya. Setelah selesai, karyawan menekan tombol "Pesanan Selesai" di monitor.
8. Karyawan membawa minuman tersebut dan mengantarkannya langsung ke Meja No. X secara akurat. Seluruh proses transaksi ini otomatis tersimpan di Dasbor Laporan milik Owner.

---

### 10. Detail Use Case
Bagian ini menjabarkan rincian spesifikasi dari aktivitas utama yang dilakukan oleh para aktor di dalam sistem.

**A. UC-01: Melakukan Pemesanan Mandiri**
* **Aktor Utama:** Pelanggan
* **Pre-condition (Kondisi Awal):** Pelanggan telah berhasil memindai QR Code dan halaman E-Menu terbuka di peramban gawai mereka.
* **Main Flow (Alur Utama):**
  1. Sistem menampilkan antarmuka katalog menu beserta rincian harga.
  2. Pelanggan memilih satu atau beberapa menu dan menempatkannya ke dalam keranjang virtual.
  3. Sistem mengkalkulasi total harga, termasuk pajak (jika ada), dan menampilkan ringkasan pesanan.
  4. Pelanggan melakukan konfirmasi dan diarahkan ke gerbang pembayaran.
  5. Pelanggan menyelesaikan proses pembayaran.
* **Post-condition (Kondisi Akhir):** Sistem menerbitkan nomor resi digital, merubah status keranjang menjadi pesanan aktif, dan meneruskan data tersebut ke *database* operasional toko.

**B. UC-02: Mengelola Pesanan Masuk**
* **Aktor Utama:** Kasir / Karyawan
* **Pre-condition:** Karyawan telah melakukan proses autentikasi (login) dan halaman *Live Dashboard* sedang aktif di layar mereka.
* **Main Flow (Alur Utama):**
  1. Sistem memicu bunyi notifikasi visual dan audio saat pesanan baru dari UC-01 masuk.
  2. Karyawan meninjau detail pesanan (jenis minuman, *custom request*, dan nomor meja).
  3. Karyawan mengubah status pesanan dari "Menunggu" menjadi "Sedang Diramu/Diproses".
  4. Setelah produk fisik siap disajikan, Karyawan mengeklik tombol "Selesai" atau "Siap Diantar".
* **Post-condition:** Antrean pesanan di layar karyawan menjadi bersih, dan notifikasi bahwa pesanan sedang diantar dapat dilihat di layar gawai pelanggan.

**C. UC-03: Manajemen Katalog dan Laporan**
* **Aktor Utama:** Owner (Pemilik)
* **Pre-condition:** Pemilik telah *login* ke *Admin Dashboard* menggunakan kredensial khusus tingkat atas.
* **Main Flow (Alur Utama):**
  1. Pemilik masuk ke modul "Laporan Penjualan" dan sistem merender grafik statistik pendapatan serta produk paling populer pada rentang waktu yang dipilih.
  2. Pemilik masuk ke modul "Katalog Menu" untuk menonaktifkan (*hide*) menu "Ice Caramel Macchiato" karena stok sirup karamel terpantau habis di gudang.
  3. Pemilik menyimpan perubahan tersebut.
* **Post-condition:** Data E-Menu pada sisi pelanggan otomatis diperbarui secara *real-time* tanpa perlu me-*refresh* server secara manual.

---

### 11. Diagram Use Case

*(Masukin hasil diagram use case nya)*

---

### 12. Rincian Alur Sistem (Activity Sequence)
Alur aktivitas (*Activity*) ini mengilustrasikan perpindahan kontrol dari satu aktor ke sistem, hingga selesai dari awal pertemuan pelanggan dengan sistem sampai produk akhir disajikan:

1. **[Pelanggan]** Menginisiasi proses dengan memindai QR Code yang berada di permukaan meja.
2. **[Sistem]** Menerima permintaan *URL*, membaca parameter nomor meja (misal: `?table=12`), dan merender halaman utama UI Pemesanan.
3. **[Pelanggan]** Menambahkan produk yang diinginkan ke dalam *cart* (keranjang) dan menekan tombol *Checkout*.
4. **[Sistem]** Mengunci pesanan, menghasilkan *QRIS dinamis* atau tautan *E-Wallet*, dan menampilkannya di layar *smartphone* pelanggan.
5. **[Pelanggan]** Melakukan *scan* QRIS dan memasukkan PIN untuk menyetujui pemotongan saldo.
6. **[Sistem]** Melakukan komunikasi dengan API perbankan pihak ketiga untuk memverifikasi dana masuk. Setelah *callback* berstatus *Success* diterima, sistem menerbitkan struk elektronik.
7. **[Sistem]** Mengirimkan beban kerja (data pesanan) tersebut ke tampilan Dasbor Pesanan Aktif milik karyawan.
8. **[Kasir/Karyawan]** Mengamati layar, melihat pesanan dari Meja 12, dan memulai proses pembuatan secara fisik (*brewing* / *cooking*).
9. **[Kasir/Karyawan]** Menekan tombol aksi "Selesaikan Pesanan" di dalam dasbor setelah produk fisik siap.
10. **[Kasir/Karyawan]** Membawa nampan berisi produk dan langsung menuju Meja 12 karena lokasinya sudah teridentifikasi dengan jelas.
11. **[Sistem]** Memasukkan data transaksi yang telah berstatus "Selesai" tersebut ke dalam log riwayat transaksi (Buku Besar Digital).
12. **[Owner]** Dapat melihat riwayat tersebut secara agregat dalam bentuk grafik visual di Dasbor Manajemen kapan pun diperlukan.
13. **Proses Berakhir.**

---

### 13. Kesimpulan & Solusi yang Ditawarkan
Berdasarkan seluruh proses analisis dan observasi yang kelompok kami lakukan, dapat ditarik kesimpulan bahwa titik lemah (*pain point*) terbesar pada Coffee Shop Satukala adalah sistem operasional berbasis sentralisasi di area kasir. Sistem manual ini menghambat efisiensi waktu kerja karyawan dan berpotensi menurunkan tingkat kepuasan serta keinginan pelanggan untuk berbelanja lebih banyak.

**Solusi Terintegrasi:** Kelompok kami mengusulkan pengembangan **"Satukala Self-Ordering System"**. Solusi inovatif ini secara fundamental mengubah setiap meja pelanggan menjadi terminal kasir mandiri (*virtual point-of-sale*). Dengan mendigitalisasi proses pemesanan melalui QR Code, sistem ini tidak hanya mengeliminasi antrean panjang secara efektif, tetapi juga memastikan akurasi data pesanan, merampingkan komunikasi antara pelanggan dan area dapur, serta memberikan kapabilitas manajerial yang transparan bagi pemilik bisnis. Implementasi sistem ini diyakini akan mendongkrak efisiensi operasional sekaligus meningkatkan margin keuntungan bisnis secara signifikan melalui *customer experience* yang modern dan prima.* **Use Case 02 - Lihat Menu:** Menampilkan daftar menu, harga, dan foto produk secara real-time.
* **Use Case 03 - Pesan Menu:** Pelanggan memilih menu dan mengonfirmasi pesanan ke sistem.
* **Use Case 04 - Pembayaran:** Integrasi metode pembayaran digital dan update status transaksi.
* **Use Case 05 - Kelola Pesanan:** Pihak dapur/bar memperbarui status pesanan (diproses/selesai).
* **Use Case 06 - Manajemen Menu:** Admin melakukan update harga, deskripsi, atau ketersediaan menu.
