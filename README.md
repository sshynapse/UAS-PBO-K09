# ⚡ Sistem Rental Sepeda Listrik & Skuter

**Project UAS Praktikum Pemrograman Berorientasi Objek — Kelas B**

Program Studi Informatika · FMIPA · Universitas Syiah Kuala  
Semester Ganjil 2026/2027

---

## Tentang Proyek

Sistem Rental Sepeda Listrik & Skuter merupakan aplikasi penyewaan kendaraan berbasis Java yang dikembangkan sebagai proyek Ujian Akhir Semester (UAS) Praktikum Pemrograman Berorientasi Objek.

Aplikasi ini menyediakan dua jenis pengguna, yaitu **Admin** dan **Penyewa**, dengan fitur pengelolaan barang, transaksi penyewaan, pembayaran, hingga pengembalian kendaraan. Program tersedia dalam versi Command Line Interface (CLI) dan Graphical User Interface (GUI) menggunakan Java Swing.

## Fitur Aplikasi

| Fitur | Deskripsi |
|---|---|
| 🔐 Login | Autentikasi Admin dan Penyewa |
| 📦 Kelola Barang | Tambah, edit, dan hapus barang |
| 🛒 Keranjang Sewa | Menambahkan dan menghapus barang dari keranjang |
| 🛴 Kategori Kendaraan | Sepeda Listrik, Skuter Listrik, dan Skuter Premium |
| 💳 Pembayaran | Transfer Bank, QRIS, dan Tunai |
| 🧾 Invoice | Membuat dan menampilkan invoice penyewaan |
| 📋 Riwayat Sewa | Menampilkan riwayat transaksi penyewa |
| ↩️ Pengembalian | Konfirmasi pengembalian kendaraan oleh Admin |
| ⚠️ Denda | Perhitungan denda keterlambatan Rp20.000 per hari per barang |

### Kategori Kendaraan

- **Sepeda Listrik**
- **Skuter Listrik** — biaya asuransi sebesar 5%.
- **Skuter Premium** — biaya helm dan baterai sebesar Rp10.000/hari.

Barang yang sedang disewa tidak dapat disewa oleh penyewa lain.

## Teknologi

- **Bahasa:** Java
- **GUI:** Java Swing
- **Version Control:** Git & GitHub

## Struktur Proyek

```text
UAS-PBO-K09/
├── docs/
│   └── class-diagram.png
│
├── src/
│   ├── Main.java
│   ├── MainGUI.java
│   │
│   ├── model/
│   │   ├── Akun.java
│   │   ├── Admin.java
│   │   ├── Penyewa.java
│   │   ├── Barang.java
│   │   ├── SepedaListrik.java
│   │   ├── SkuterListrik.java
│   │   ├── SkuterPremium.java
│   │   ├── Transaksi.java
│   │   └── Invoice.java
│   │
│   ├── payment/
│   │   ├── Pembayaran.java
│   │   ├── TransferBank.java
│   │   ├── QRIS.java
│   │   └── Tunai.java
│   │
│   ├── service/
│   │   ├── DataSistem.java
│   │   ├── KeranjangSewa.java
│   │   └── DaftarBarang.java
│   │
│   ├── exception/
│   │   ├── LoginGagalException.java
│   │   └── BarangTidakTersediaException.java
│   │
│   └── gui/
│       ├── LoginFrame.java
│       ├── PenyewaFrame.java
│       ├── AdminFrame.java
│       ├── Theme.java
│       └── Util.java
│
└── README.md
```

## Cara Menjalankan

### Persyaratan

- Java Development Kit (JDK)
- Terminal atau IDE yang mendukung Java

### 1. Clone Repository

```bash
git clone [LINK-REPOSITORY]
```

Masuk ke folder proyek:

```bash
cd UAS-PBO-K09
```

### 2. Compile Program

**Windows PowerShell:**

```powershell
javac -d out (Get-ChildItem -Path src -Recurse -Filter *.java | ForEach-Object { $_.FullName })
```

**Git Bash / macOS / Linux:**

```bash
javac -d out $(find src -name "*.java")
```

### 3. Jalankan Aplikasi

**Versi CLI:**

```bash
java -cp out Main
```

**Versi GUI:**

```bash
java -cp out MainGUI
```

## Akun Demo

| Role | Username | Password |
|---|---|---|
| Admin | `admin` | `admin123` |
| Penyewa | `budi` | `budi123` |
| Penyewa | `sari` | `sari123` |

## Anggota Kelompok 9

| No. | Nama Lengkap | NPM |
|:---:|---|:---:|
| 1 | Riski Maulidan | 250810701100004 |
| 2 | Shofy Suhaila Putri | 250810701100007 |
| 3 | Kania Ghaitsa Aqira | 250810701100035 |
