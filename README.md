# Laporan Tugas APBO - CafeEase: Sistem Pemesanan Meja Mandiri

Tugas Analisis Perancangan Berorientasi Objek - Kelas A
**Dosen:** Adi Wahyu Pribadi, S.T M.T

---

## Identitas Proyek

**Nama Proyek:**
CafeEase

**Deskripsi Proyek:**
CafeEase adalah aplikasi pemesanan makanan dan minuman berbasis digital yang dirancang untuk cafe yang masih menggunakan sistem konvensional (antre di kasir). Aplikasi ini memungkinkan pelanggan memesan langsung dari meja melalui pemindaian QR Code, meminimalisir antrean, serta memberikan kenyamanan bagi pengguna. Selain itu, CafeEase membantu pemilik cafe mengelola pesanan agar lebih cepat, rapi, dan efisien.

**Anggota Kelompok:**
1. [Shafiq Usman Nurhananto] - [4523210103]
2. [M Dhafa Fahlevie Hardiansyach] - [4523210071]
3. [Ciesha Fajar Ramadhan] - [4523210031]
4. [Fazril Fadilah ] - [4523210047]
5. [Ahmad Farid Akbar] - [4523210006]  
---

## Latar Belakang & Identifikasi Masalah

### Latar Belakang
Banyak cafe saat ini masih mewajibkan pelanggan untuk berdiri dan mengantre di kasir hanya untuk memesan, yang seringkali menciptakan penumpukan di area kasir. Sistem manual ini juga meningkatkan risiko kesalahan komunikasi antara pelanggan, kasir, dan bagian dapur.

### Identifikasi Masalah
1.  **Antrean Menumpuk:** Pelanggan harus menunggu lama di depan kasir untuk memesan.
2.  **Ketidakefisienan Pesanan Tambahan:** Pelanggan enggan memesan kembali karena malas harus beranjak ke kasir lagi.
3.  **Kesalahan Pencatatan:** Pesanan manual berisiko salah catat atau hilang jika kondisi cafe sedang sangat ramai.
4.  **Komunikasi Terhambat:** Pelayan sering kesulitan mengidentifikasi pesanan untuk nomor meja tertentu.
5.  **Monitoring Kurang Efisien:** Pemilik sulit memantau status pesanan (sedang dibuat/selesai) secara real-time.

---

## Analisis Kebutuhan Pengguna (Use Case)

### Empathy Map
| User | Says | Thinks | Does | Feels |
| :--- | :--- | :--- | :--- | :--- |
| **Pelanggan** | "Malas harus antre ke kasir cuma buat tambah pesanan." | "Kalau bisa pesan dari meja lewat HP pasti lebih praktis." | Berdiri dari meja, antre di kasir, menunggu struk manual. | Lelah, bosan, merasa tidak nyaman. |
| **Penjual/Kasir** | "Pusing kalau sudah ramai, pesanan suka numpuk dan salah input." | "Mau sistem yang otomatis masuk ke dapur biar tidak repot teriak." | Mencatat manual, mengecek ketersediaan menu secara berulang. | Kewalahan, stres saat jam sibuk. |

### Daftar Aktor
* **Actor 01 - Pelanggan:** Ingin sistem pemesanan yang cepat tanpa antre dan menu yang selalu update.
* **Actor 02 - Admin/Kasir:** Membutuhkan sistem yang mudah digunakan untuk memvalidasi pembayaran dan mengelola stok.
* **Actor 03 - Dapur/Bar:** Membutuhkan informasi pesanan yang jelas dan terorganisir per meja.

### Daftar Use Case
* **Use Case 01 - Scan QR & Meja:** Pengguna mengakses menu berdasarkan nomor meja yang ditempati.
* **Use Case 02 - Lihat Menu:** Menampilkan daftar menu, harga, dan foto produk secara real-time.
* **Use Case 03 - Pesan Menu:** Pelanggan memilih menu dan mengonfirmasi pesanan ke sistem.
* **Use Case 04 - Pembayaran:** Integrasi metode pembayaran digital dan update status transaksi.
* **Use Case 05 - Kelola Pesanan:** Pihak dapur/bar memperbarui status pesanan (diproses/selesai).
* **Use Case 06 - Manajemen Menu:** Admin melakukan update harga, deskripsi, atau ketersediaan menu.

---

## WORKFLOW!!

1. `git clone` (Clone repo ke local)
2. `git checkout -b NAMAKALIAN` (Membuat branch dengan nama sendiri)
3. `git checkout branch_tujuan` (Pindah branch kalian atau kalau ke main repo berarti checkout main)
4. `git add .` (Menambah yang ingin dicommit)
5. `git commit -m "fiks"` (commit yang ingin dipush)
6. `git push -u origin BRANCHKALIAN` (push ke BRANCH KALIAN, JANGAN KE MAIN!!)
7. `git pull main` (Posisi branch main, pull dari main. PULL KETIKA SUDAH MERGE FINAL)
8. `git merge main` (Posisi branch sendiri, merge dari main yang terupdate!)
