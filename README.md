========================================================================
PROJECT UAS PRAKTIKUM PEMROGRAMAN BERORIENTASI OBJEK - KELAS B
PROGRAM STUDI INFORMATIKA, FMIPA UNIVERSITAS SYIAH KUALA
SEMESTER GANJIL 2026/2027
========================================================================

JUDUL PROGRAM
Sistem rental sepeda listrik dan skuter berbasis GUI dengan Java

------------------------------------------------------------------------
1. IDENTITAS KELOMPOK 9
------------------------------------------------------------------------
No.   Nama Lengkap            NPM
1.    Riski Maulidan          250810701100004
2.    Shofy Suhaila Putri     250810701100007
3     Kania Ghaitsa Aqira     250810701100035


------------------------------------------------------------------------
2. DESKRIPSI
------------------------------------------------------------------------
Sistem penyewaan sepeda listrik dan skuter berbasis GUI menggunakan
bahasa Java, dibuat untuk UAS Praktikum Pemrograman Berorientasi Objek.
Penyewa memasukkan barang ke keranjang, lalu membuat transaksi sewa
dengan lama sewa dan metode pembayaran pilihan. Admin mengelola barang,
menerima transaksi, dan mengonfirmasi pengembalian beserta denda
keterlambatan. Tersedia juga versi GUI (Swing) sebagai tambahan opsional.


------------------------------------------------------------------------
3. FITUR
------------------------------------------------------------------------
- Login Admin dan Penyewa
- Kelola barang (tambah, edit, hapus) dan keranjang sewa
- 3 kategori barang: Sepeda Listrik, Skuter Listrik (+ asuransi 5%),
  Skuter Premium (+ helm dan baterai Rp10.000/hari)
- 3 metode pembayaran: Transfer Bank, QRIS, Tunai
- Invoice, riwayat sewa, dan denda keterlambatan Rp20.000 per hari per barang
- Barang yang sedang disewa tidak bisa disewa penyewa lain


------------------------------------------------------------------------
4. STRUKTUR PROYEK
------------------------------------------------------------------------
UAS-PBO-K09/
├── README.txt
├── docs/
│   └── class-diagram.png
└── src/
    ├── Main.java                 (CLI)
    ├── MainGUI.java              (GUI)
    ├── model/                    Akun, Admin, Penyewa, Barang, SepedaListrik,
    │                             SkuterListrik, SkuterPremium, Transaksi, Invoice
    ├── payment/                  Pembayaran (interface), TransferBank, QRIS, Tunai
    ├── service/                  DataSistem, KeranjangSewa, DaftarBarang
    ├── exception/                LoginGagalException, BarangTidakTersediaException
    └── gui/                      LoginFrame, PenyewaFrame, AdminFrame, Theme, Util


------------------------------------------------------------------------
5. CARA MENJALANKAN
------------------------------------------------------------------------

Compile dari folder utama proyek (PowerShell), lalu jalankan:
  javac -d out (Get-ChildItem -Path src -Recurse -Filter *.java | ForEach-Object { $_.FullName })
  java -cp out Main

Untuk Git Bash / Mac / Linux, compile dengan:
  javac -d out $(find src -name "*.java")

Versi GUI: java -cp out MainGUI

------------------------------------------------------------------------
6. AKUN DEMO
------------------------------------------------------------------------
- Admin   : admin / admin123
- Penyewa : budi / budi123
- Penyewa : sari / sari123