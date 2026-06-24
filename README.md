# Laporan Analisis Perancangan Berorientasi Objek (APBO)
## Sistem Pemesanan Meja Mandiri (Self-Ordering System) - Coffee Shop Satukala

**Mata Kuliah:** Analisis Perancangan Berorientasi Objek  
**Dosen Pengampu:** Adi Wahyu Pribadi, S.Si., M.Kom.  

---

### Identitas Proyek

* **Nama Sistem:** Satukala Self-Ordering System
* **Studi Kasus:** Coffee Shop Satukala
* **Deskripsi Proyek:** Proyek ini bertujuan untuk merancang dan membangun sebuah sistem pemesanan mandiri (self-ordering) berbasis web mobile yang dikhususkan untuk operasional Coffee Shop Satukala. Melalui sistem ini, pelanggan tidak perlu lagi antre di kasir. Pelanggan cukup memindai QR Code yang tersedia di masing-masing meja untuk mengakses katalog menu digital, melakukan pemesanan, hingga menyelesaikan transaksi pembayaran secara otonom. Sistem ini dirancang menggunakan pendekatan berorientasi objek agar terintegrasi langsung dengan dasbor karyawan untuk pemrosesan pesanan, serta dasbor pemilik (owner) untuk keperluan pemantauan penjualan dan manajemen inventaris secara real-time.
* **Tim Pengembang (Anggota Kelompok):**
  1. Shafiq Usman Nurhananto - 4523210103
  2. M Dhafa Fahlevie Hardiansyach - 4523210071
  3. Ciesha Fajar Ramadhan - 4523210031
  4. Fazril Fadilah - 4523210047
  5. Ahmad Farid Akbar - 4523210006

---

### Sasaran Pengguna

Pengembangan sistem pemesanan mandiri ini dirancang secara khusus untuk memfasilitasi tiga kelompok sasaran utama yang terlibat dalam ekosistem operasional Coffee Shop Satukala:

1. **Pelanggan (Customer):** Sebagai pengguna akhir (end-user) yang membutuhkan kemudahan, kecepatan, dan kenyamanan dalam melakukan pemesanan. Sistem ini mengeliminasi waktu tunggu antrean di kasir, terutama pada jam-jam operasional sibuk.
2. **Kasir / Karyawan (Staff/Barista):** Sebagai pelaksana operasional harian yang membutuhkan sistem untuk mengurangi beban kerja pencatatan manual. Sistem ini meminimalisasi miskomunikasi pesanan dengan pelanggan dan menyajikan daftar antrean pesanan secara sistematis agar proses pembuatan produk menjadi lebih terstruktur dan efisien.
3. **Pemilik (Owner):** Sebagai pengambil keputusan bisnis yang membutuhkan transparansi data tingkat tinggi. Pemilik memiliki akses penuh untuk memantau performa penjualan, ketersediaan stok bahan, dan pergerakan menu terlaris secara real-time dari mana saja, tanpa harus bergantung pada rekapitulasi manual pada akhir hari operasional.

---

### Dokumentasi Observasi dan Wawancara

Berikut adalah dokumentasi saat tim pengembang melakukan observasi lapangan dan wawancara dengan pihak pengelola Coffee Shop Satukala guna menggali kebutuhan sistem (requirements elicitation).

<img width="1200" height="1600" alt="Dokumentasi Wawancara" src="https://github.com/user-attachments/assets/934acec0-ca8d-4542-9f83-3496dd962e5b" />

---

### Latar Belakang dan Alur Bisnis

**Latar Belakang**
Coffee Shop Satukala merupakan salah satu destinasi komersial yang memiliki tingkat kunjungan tinggi, terutama pada akhir pekan atau jam pulang kerja. Namun, tingginya antusiasme pelanggan tidak diimbangi dengan arsitektur sistem pelayanan yang memadai. Sistem pelayanan di Satukala saat ini masih sangat konvensional dan tersentralisasi pada satu titik, yaitu meja kasir. Kondisi ini secara konsisten menciptakan penumpukan antrean (bottleneck) yang tidak hanya mengurangi kenyamanan spasial pelanggan, tetapi juga memicu berbagai masalah operasional sekunder seperti kesalahan pencatatan pesanan dan kelelahan staf.

**Alur Bisnis Saat Ini (Sistem Manual)**
Proses bisnis yang berjalan saat ini memiliki rantai operasional yang panjang dan kurang efisien:
1. Pelanggan yang baru datang diwajibkan langsung menuju meja kasir dan berdiri dalam antrean fisik.
2. Saat giliran tiba, pelanggan menyebutkan pesanan secara lisan, dan kasir menginput data tersebut secara manual ke dalam sistem Point of Sales (POS).
3. Setelah menyelesaikan proses pembayaran (tunai atau kartu), kasir menyerahkan stand nomor meja fisik kepada pelanggan.
4. Pelanggan kemudian mencari meja kosong, duduk, dan meletakkan stand nomor tersebut di atas meja.
5. Di area produksi (dapur/bar), barista meracik pesanan berdasarkan struk cetak. Setelah selesai, pelayan harus berjalan berkeliling area kafe untuk mencari letak nomor meja pelanggan guna mengantarkan pesanan.

---

### Analisis Kebutuhan Sistem dan Identifikasi Masalah

**Identifikasi Masalah**
Melalui tahapan analisis, kelompok kami mengidentifikasi beberapa masalah fundamental dalam operasional kafe:
1. **Penumpukan Antrean (Bottleneck):** Terpusatnya jalur pemesanan di kasir menyebabkan antrean panjang yang merusak pengalaman pelanggan (customer experience).
2. **Risiko Human Error:** Tingkat kebisingan kafe seringkali memicu kesalahan pendengaran oleh kasir, berujung pada kesalahan pencatatan varian rasa, modifikasi pesanan, atau nomor meja.
3. **Kehilangan Potensi Pendapatan (Loss of Sales):** Pelanggan cenderung enggan untuk melakukan pemesanan tambahan (upselling) karena harus kembali mengantre dari awal.
4. **Keterbatasan Monitoring Manajerial:** Pemilik bisnis tidak memiliki kapabilitas untuk melihat omzet, laporan transaksi, atau pergerakan stok secara real-time.

**Kebutuhan Sistem (System Requirements)**
Untuk menyelesaikan permasalahan di atas, sistem dirancang dengan spesifikasi kebutuhan sebagai berikut:
1. Kemampuan mendeteksi lokasi atau nomor meja pelanggan secara presisi melalui pemindaian QR Code unik.
2. Penyediaan antarmuka Katalog Digital (E-Menu) yang interaktif, mencakup representasi visual produk, harga, deskripsi, dan status ketersediaan.
3. Integrasi modul keranjang pesanan dan gerbang pembayaran digital (Payment Gateway) yang memungkinkan checkout mandiri.
4. Fitur notifikasi seketika (real-time alert) pada perangkat operasional karyawan setiap kali transaksi pemesanan berhasil divalidasi.
5. Penyediaan dasbor analitik berbasis web bagi pemilik untuk manajemen data master dan pemantauan metrik penjualan.

---

### Analisis Aktor

Dalam memodelkan sistem berorientasi objek ini, diidentifikasi tiga entitas aktor dengan hak akses dan batasan fungsional yang spesifik:

1. **Aktor: Pelanggan**
Pengguna front-end yang berinteraksi dengan sistem tanpa memerlukan proses autentikasi (login) akun yang rumit. Pelanggan berinteraksi menggunakan perangkat pintar pribadi mereka. Fungsionalitas utama meliputi pemindaian QR, penelusuran katalog menu, manajemen keranjang pesanan, dan eksekusi pembayaran digital.

2. **Aktor: Kasir / Karyawan**
Pengguna operasional (back-end user) yang bertindak sebagai penerima instruksi sistem. Menggunakan perangkat keras di area produksi (dapur/bar). Fungsionalitas utama meliputi penerimaan pesanan tervalidasi, serta pembaruan status siklus pesanan (dari "Diproses" hingga "Selesai/Siap Diantar").

3. **Aktor: Pemilik (Owner)**
Pengguna dengan hak akses administratif tertinggi (administrator). Tidak terlibat dalam siklus pemesanan individual, melainkan memegang kendali atas manajemen data secara keseluruhan. Fungsionalitas utama meliputi manipulasi data menu (Create, Read, Update, Delete), pembaruan status ketersediaan bahan, serta akses penuh terhadap visualisasi laporan penjualan.

---

### Analisis Perbandingan Sistem

| Parameter Evaluasi | Sistem Satukala Konvensional (Manual) | Satukala Self-Ordering System (Digital) |
| :--- | :--- | :--- |
| **Metode Pemesanan** | Tersentralisasi: Pelanggan wajib antre fisik di depan kasir. | Terdesentralisasi: Setiap meja berfungsi sebagai terminal pemesanan mandiri. |
| **Metode Pembayaran** | Transaksi langsung via kasir (Tunai atau EDC). | Terintegrasi otomatis melalui Payment Gateway (QRIS/E-Wallet). |
| **Tingkat Akurasi Data** | Rentan terhadap human error (salah dengar/salah ketik). | Akurasi tinggi karena data dimasukkan dan divalidasi langsung oleh pelanggan. |
| **Pemesanan Tambahan** | Mengharuskan pelanggan kembali ke antrean awal. | Dapat dieksekusi instan melalui perangkat pelanggan di meja. |
| **Pelaporan dan Evaluasi** | Rekapitulasi fisik yang baru diakses setelah tutup operasional. | Laporan berbasis data real-time, dapat diakses kapan saja oleh pemilik. |

---

### Daftar Use Case Sistem

Sistem ini diabstraksikan ke dalam enam fungsionalitas utama (Use Case) sebagai berikut:
1. **Use Case 01 - Scan QR Code:** Pelanggan memindai kode identifikasi meja untuk mendapatkan akses ke dalam sistem.
2. **Use Case 02 - Lihat Menu:** Sistem menampilkan daftar menu, harga, dan foto produk secara real-time kepada pelanggan.
3. **Use Case 03 - Pesan Menu:** Pelanggan mengelola pilihan menu ke dalam keranjang dan mengonfirmasi pesanan ke sistem.
4. **Use Case 04 - Pembayaran:** Pelanggan melakukan integrasi dengan metode pembayaran digital dan sistem memperbarui status transaksi.
5. **Use Case 05 - Kelola Pesanan:** Pihak operasional (dapur/bar) memantau pesanan masuk dan memperbarui status pesanan (diproses/selesai).
6. **Use Case 06 - Manajemen Menu:** Admin (Pemilik) melakukan pembaruan terkait data master seperti harga, deskripsi, atau ketersediaan menu operasional.

---

### Detail Spesifikasi Use Case

* **UC-01: Scan QR Code**
  * **Aktor:** Pelanggan
  * **Deskripsi:** Proses inisialisasi awal di mana pelanggan memindai QR Code di meja.
  * **Alur Utama:** Pelanggan memindai QR. Sistem membaca parameter nomor meja dari tautan tersebut dan mengarahkan pengguna ke halaman utama tanpa perlu login.
* **UC-02: Lihat Menu**
  * **Aktor:** Pelanggan
  * **Deskripsi:** Sistem menyajikan antarmuka katalog digital secara interaktif.
  * **Alur Utama:** Sistem melakukan query ke basis data dan menampilkan daftar menu, harga, foto produk berdasarkan kategori. Data ketersediaan (stok) disajikan secara real-time.
* **UC-03: Pesan Menu**
  * **Aktor:** Pelanggan
  * **Deskripsi:** Proses seleksi produk dan pengaturan kuantitas sebelum proses checkout.
  * **Alur Utama:** Pelanggan memilih menu, mengatur catatan khusus (misalnya: tingkat kemanisan), dan menambahkannya ke keranjang lalu menekan konfirmasi pesanan.
* **UC-04: Pembayaran**
  * **Aktor:** Pelanggan, Payment Gateway
  * **Deskripsi:** Proses penyelesaian transaksi finansial atas pesanan.
  * **Alur Utama:** Sistem menghasilkan total tagihan. Pelanggan memilih metode pembayaran (QRIS) dan mentransfer dana. API Payment Gateway memberikan respon sukses ke sistem, yang kemudian mengubah status transaksi menjadi "Lunas".
* **UC-05: Kelola Pesanan**
  * **Aktor:** Kasir / Karyawan
  * **Deskripsi:** Manajemen siklus hidup pesanan di area dapur.
  * **Alur Utama:** Sistem membunyikan notifikasi saat pesanan lunas masuk. Karyawan meracik minuman, lalu memperbarui status menjadi "Selesai" dan mengantarkan pesanan ke nomor meja.
* **UC-06: Manajemen Menu (Admin)**
  * **Aktor:** Pemilik (Owner)
  * **Deskripsi:** Pemeliharaan data master terkait produk yang dijual.
  * **Alur Utama:** Pemilik mengakses panel manajemen untuk menambah menu baru, mengedit harga, atau menonaktifkan tampilan menu yang bahan bakunya habis.

---

### Rancangan Analisis dan Pemodelan Berorientasi Objek (UML Diagrams)

Pendekatan Analisis dan Perancangan Berorientasi Objek (APBO) pada proyek Satukala Self-Ordering System diwujudkan melalui lima jenis pemodelan diagram Unified Modeling Language (UML).

#### 1. Diagram Use Case
Diagram ini memodelkan interaksi fungsionalitas sistem dengan para aktor yang terlibat.

![Diagram Use Case]( Masukkan Link atau Drag & Drop Gambar Diagram Use Case Di Sini )

**Poin Analisis Use Case:**
* **Aktor Utama dan Eksternal:** Menempatkan Pelanggan, Karyawan, dan Pemilik sebagai aktor manusia, serta Payment Gateway sebagai aktor sistem eksternal pendukung transaksi.
* **Relasi Include:** Menghubungkan fungsi Pesan Menu dengan Pembayaran, mengartikan pesanan tidak valid tanpa adanya pembayaran berhasil.
* **Relasi Extend:** Kustomisasi pesanan bersifat opsional (tambahan) saat pelanggan melakukan pemesanan.

#### 2. Diagram Class
Diagram ini merepresentasikan struktur statis dan cetak biru dari objek-objek penyusun sistem.

![Diagram Class]( Masukkan Link atau Drag & Drop Gambar Diagram Class Di Sini )

**Poin Analisis Class Diagram:**
* **Konsep Pewarisan (Inheritance):** Karyawan dan Pemilik mewarisi atribut dari abstract class Pengguna untuk menghindari redundansi kode.
* **Relasi Komposisi:** Kelas `Pesanan` memiliki relasi komposisi kuat dengan `DetailPesanan`, menunjukkan bahwa detail item tidak akan eksis tanpa adanya data transaksi utama.
* **Visibilitas dan Enkapsulasi:** Atribut dilindungi dengan modifier private (-) dan hanya dapat diakses melalui metode public (+).

#### 3. Diagram State
Diagram ini memodelkan siklus hidup (lifecycle) dinamis dari satu objek tunggal, yaitu entitas **Pesanan**.

![Diagram State]( Masukkan Link atau Drag & Drop Gambar Diagram State Di Sini )

**Poin Analisis State Diagram:**
* **Siklus Hidup Terpusat:** Memantau satu objek spesifik secara ketat mulai dari `KeranjangBelanja` hingga `SelesaiDiterima`.
* **Composite State:** Terdapat status bersarang (sub-state) seperti proses `PersiapanBahan` dan `Peracikan` yang terjadi di dalam status utama `SedangDiproses`.
* **Penanganan Exception:** Terdapat jalur alternatif `BatalKadaluarsa` jika pembayaran tidak diselesaikan dalam batas waktu.

#### 4. Diagram Sequence
Diagram ini memetakan komunikasi data dan pemanggilan fungsi antar komponen berdasarkan urutan waktu operasional (alur Checkout & Pembayaran).

![Diagram Sequence]( Masukkan Link atau Drag & Drop Gambar Diagram Sequence Di Sini )

**Poin Analisis Sequence Diagram:**
* **Pemisahan Lapisan Arsitektur (MVC):** Memisahkan interaksi antara antarmuka (UI), logika pengendali (Controller), dan penyimpanan (Database).
* **Asynchronous Call (Webhook):** Menggambarkan penggunaan webhook callback dari Payment Gateway untuk mengonfirmasi status pembayaran tanpa membuat sistem hang/menunggu.
* **Kondisional (Alt Block):** Menyediakan skenario percabangan secara teknis jika pembayaran disetujui atau ditolak oleh API eksternal.

#### 5. Diagram Activity
Diagram ini memvisualisasikan Standar Operasional Prosedur (SOP) dan aliran kerja end-to-end secara makro.

![Diagram Activity]( Masukkan Link atau Drag & Drop Gambar Diagram Activity Di Sini )

**Poin Analisis Activity Diagram:**
* **Pembagian Swimlane:** Membedakan jalur tanggung jawab antara aksi fisik Pelanggan, proses komputasi Sistem Satukala, dan tugas operasional Karyawan Dapur.
* **Titik Keputusan (Decision Node):** Memodelkan logika percabangan saat validasi finansial berlangsung.
* **Sinkronisasi Lintas Batas:** Menunjukkan aliran paralel di mana pesanan yang sukses dibayar oleh pelanggan langsung dikirimkan sebagai notifikasi kerja ke layar dapur.

---

### Rincian Alur Sistem (Proses Eksekusi)

Alur aktivitas berikut menggambarkan transisi kontrol dari aktor menuju sistem hingga transaksi bisnis selesai:
1. **Inisiasi:** Pelanggan memulai sesi dengan memindai stiker QR Code di meja.
2. **Identifikasi:** Sistem menerima URL, mengekstrak nomor meja, dan merender UI Katalog Menu.
3. **Seleksi:** Pelanggan menambahkan produk ke dalam keranjang lalu mengeksekusi tombol Checkout.
4. **Pembuatan Tagihan:** Sistem mengkalkulasi total pembayaran dan mengonstruksi kode pembayaran QRIS di layar.
5. **Otorisasi Pembayaran:** Pelanggan memindai kode transaksi melalui aplikasi E-Wallet.
6. **Validasi Sistem:** Backend Satukala menerima callback respons sukses dari perbankan, lalu menerbitkan resi digital.
7. **Distribusi Tugas:** Sistem secara real-time mengirimkan rincian pesanan ke Dasbor Karyawan di dapur.
8. **Produksi:** Karyawan memvalidasi pesanan, memperbarui status menjadi "Sedang Diproses", dan mulai meracik hidangan.
9. **Penyelesaian:** Karyawan menekan tombol "Pesanan Selesai" dan mengantarkannya secara akurat ke meja pelanggan.
10. **Pencatatan & Monitoring:** Sistem merekam seluruh metrik transaksi secara permanen ke basis data yang kemudian divisualisasikan dalam Dasbor Pemilik.

---

### Kesimpulan dan Solusi

Berdasarkan analisis pemodelan proses bisnis yang telah dilakukan, dapat disimpulkan bahwa hambatan operasional utama pada Coffee Shop Satukala bersumber dari sistem pemesanan konvensional yang berpusat pada area kasir. Pola operasional ini terbukti menurunkan efisiensi waktu kerja staf, memperbesar peluang kesalahan manusia (human error), dan membatasi kapabilitas kafe dalam memaksimalkan volume penjualan pada jam sibuk.

**Solusi Terintegrasi:**
Proyek ini mengusulkan implementasi "Satukala Self-Ordering System", sebuah perangkat lunak berbasis arsitektur pemesanan terdesentralisasi. Melalui integrasi teknologi QR Code, sistem mengubah setiap meja pelanggan menjadi terminal Point of Sales (POS) mandiri. Perancangan sistem berorientasi objek ini secara efektif mengeliminasi antrean fisik, menjamin akurasi aliran data pesanan dari pelanggan ke dapur, dan mendigitalkan arus kas. Lebih jauh, kapabilitas administratif yang tertanam di dalam sistem memberikan kemampuan manajerial yang transparan bagi pemilik bisnis. Solusi teknologi ini diproyeksikan mampu meningkatkan efisiensi operasional kafe sekaligus mendorong pertumbuhan profitabilitas melalui pengalaman pelanggan yang modern dan terpadu.
