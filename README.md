# ADB Security Inspector

## 📋 Deskripsi Aplikasi

ADB Security Inspector adalah aplikasi desktop berbasis Delphi yang dirancang untuk membantu pengguna dalam mengelola dan mengamankan perangkat Android melalui koneksi ADB (Android Debug Bridge). Aplikasi ini menyediakan berbagai fitur keamanan dan pemeliharaan untuk perangkat Android dengan antarmuka yang intuitif dan responsif.

## ✨ Fitur Utama

### 🔍 **Pemindaian & Deteksi**
- **Scan Aplikasi**: Mendeteksi dan memindai semua aplikasi yang terinstal di perangkat
- **Deep Scan Ransomware**: Pemindaian mendalam untuk mendeteksi file mencurigakan terenkripsi
- **Deteksi Aplikasi Mencurigakan**: Otomatis mengidentifikasi aplikasi berpotensi berbahaya (ads, gift, cleaner)
- **Auto Device Detection**: Deteksi otomatis saat perangkat Android terhubung

### 🛠️ **Manajemen Aplikasi**
- **Uninstall dengan Backup**: Menghapus aplikasi dengan opsi backup terlebih dahulu
- **Instal APK**: Memudahkan instalasi aplikasi dari file APK
- **Detail Aplikasi**: Menampilkan informasi lengkap (ukuran, izin, dll.)
- **Filter & Pencarian**: Filter cepat untuk menemukan aplikasi tertentu

### 🧹 **Pemeliharaan Sistem**
- **Pembersihan Sampah Iklan**: Membersihkan folder sampah dan cache iklan
- **Device Health Report**: Laporan kesehatan perangkat (suhu baterai, penyimpanan)
- **Auto Export Log**: Ekspor otomatis log aktivitas ke file

### 🔒 **Fitur Keamanan**
- **Anti-Debug Protection**: Perlindungan terhadap debugging tidak sah
- **Thread-Safe Operations**: Operasi berat dijalankan di background thread
- **Skinable UI**: Antarmuka yang dapat dikustomisasi dengan skin

## 🚀 Persyaratan Sistem

### Sistem Operasi
- Windows 7/8/10/11 (64-bit recommended)

### Perangkat Lunak Pendukung
- **TIDAK PERLU INSTAL ADB TERPISAH**: Semua file ADB sudah termasuk dalam paket
- **Android Device**: Perangkat Android dengan USB Debugging diaktifkan

### Spesifikasi Hardware
- RAM: Minimum 2GB (4GB recommended)
- Storage: 100MB ruang kosong
- USB Port: Untuk koneksi ke perangkat Android

## 📦 Instalasi & Setup

### 📥 **Cara Instalasi (Pilih Salah Satu)**

#### **Opsi 1: Portable (Rekomendasi)**
1. Download file ZIP dari [GitHub Releases](https://github.com/MichaelJorky/ADB-Security-Inspector/releases)
2. Ekstrak ke folder pilihan (contoh: `C:\ADB-Security-Inspector\`)
3. **Tidak perlu instalasi**, langsung jalankan `ADBSecurityInspector.exe`

#### **Opsi 2: Installer**
1. Download installer `.exe` atau `.msi`
2. Jalankan installer dan ikuti panduan
3. Aplikasi akan terinstal dengan semua komponen ADB

### ⚡ **Setup Cepat dalam 3 Langkah**

1. **Siapkan Perangkat Android**:
   - Aktifkan **Developer Options** (Tap Build Number 7x)
   - Aktifkan **USB Debugging** di Developer Options
   - Hubungkan via USB ke komputer

2. **Jalankan Aplikasi**:
   - Buka folder aplikasi
   - Jalankan `ADBSecurityInspector.exe`
   - **Izinkan akses** jika ada permintaan UAC/administrator

3. **Konfirmasi di Smartphone**:
   - Di smartphone, akan muncul popup "Allow USB debugging?"
   - Centang **Always allow from this computer**
   - Klik **OK**

## 🎯 Penggunaan Dasar

### 1. **Koneksi Perangkat (Pertama Kali)**
```
Status Bar: Menunggu perangkat terhubung...
→ Hubungkan Android via USB
→ Klik "Scan" atau tunggu auto-detect
→ Berhasil: "Sinkronisasi Selesai. Perangkat Sehat."
```

### 2. **Pemindaian & Analisis**
- **Quick Scan**: Klik `Scan` untuk deteksi aplikasi dasar
- **Deep Scan**: Klik `Scan Ransomware` untuk pemeriksaan ransomware
- **Filter**: Ketik di kotak pencarian untuk mencari aplikasi spesifik

### 3. **Manajemen Aplikasi**
```
Untuk menghapus aplikasi mencurigakan:
1. Pilih aplikasi dari list (warna merah = mencurigakan)
2. Klik "Uninstall"
3. Konfirmasi backup & hapus
```

### 4. **Pemeliharaan Rutin**
- **Bersihkan Cache**: `Optimasi Sistem` setiap minggu
- **Cek Kesehatan**: Health report otomatis setelah scan
- **Install APK**: `Install` → pilih file `.apk`

## 📁 **Struktur File & Penjelasan**

```
ADB-Security-Inspector/
├── 📄 ADBSecurityInspector.exe      # Aplikasi utama (JANGAN DIHAPUS)
├── 📄 adb.exe                       # Android Debug Bridge binary (PENTING)
├── 📄 AdbWinApi.dll                 # Windows API untuk ADB
├── 📄 AdbWinUsbApi.dll              # USB driver interface
├── 📂 Logs/                         # Auto-generated logs
│   ├── Log_2026-02-04.txt          # Log harian (auto-rotate)
│   └── Log_2026-02-05.txt          # Log berikutnya
├── 📂 Backups/                      # Backup APK sebelum uninstall
│   ├── com.suspicious.app1.apk     # Backup otomatis
│   └── com.suspicious.app2.apk
└── 📄 README.md                     # Dokumentasi ini
```

### 🛠️ **Fungsi File ADB**
| File | Fungsi | Penting? |
|------|--------|----------|
| `adb.exe` | Utilitas utama komunikasi Android | ✅ **WAJIB** |
| `AdbWinApi.dll` | Interface Windows API | ✅ **WAJIB** |
| `AdbWinUsbApi.dll` | Driver USB communication | ✅ **WAJIB** |
| `ADBSecurityInspector.exe` | Aplikasi GUI utama | ✅ **WAJIB** |

## ⚠️ **Peringatan Penting**

### ❗ **JANGAN HAPUS/MEMINDAH FILE**
- **Semua 4 file utama HARUS berada di folder yang sama**
- Jangan pindahkan `adb.exe` ke folder lain
- Jangan rename file-file tersebut
- Jika dihapus, aplikasi TIDAK AKAN BERFUNGSI

### 🔒 **Permission yang Diperlukan**
Aplikasi ini memerlukan:
- **Akses Administrator** (untuk menjalankan ADB)
- **Akses USB** (untuk komunikasi dengan device)
- **Akses File System** (untuk backup dan log)

## 🔧 **Troubleshooting**

### 🚫 **Masalah Umum & Solusi**

#### **1. Device Tidak Terdeteksi**
```
Gejala: "Perangkat tidak terdeteksi!" di log
Solusi:
1. Periksa kabel USB (coba port/kabel berbeda)
2. Pastikan USB Debugging AKTIF di smartphone
3. Restart ADB: Tutup aplikasi, buka ulang
4. Di smartphone: Cabut USB → Pasang kembali
```

#### **2. Popup "Allow USB Debugging?" Tidak Muncul**
```
Solusi:
1. Di smartphone: Settings → Developer Options
2. Nonaktifkan → Aktifkan kembali USB Debugging
3. Cabut dan pasang kembali USB
4. Restart smartphone jika perlu
```

#### **3. Aplikasi Crash atau Freeze**
```
Solusi:
1. Pastikan semua 4 file utama ada di folder yang sama
2. Run as Administrator (Klik kanan → Run as Administrator)
3. Cek Logs/ folder untuk error detail
4. Re-download aplikasi jika file corrupt
```

#### **4. "adb.exe is not recognized"**
```
Penyebab: File adb.exe hilang atau corrupt
Solusi:
1. Download ulang paket lengkap dari GitHub
2. Ekstrak ke folder baru
3. Jangan pindahkan file satu per satu
```

### 📋 **Checklist Sebelum Melapor Bug**
- [ ] Semua 4 file utama ada di folder yang sama
- [ ] USB Debugging AKTIF di smartphone
- [ ] Sudah mencoba port USB berbeda
- [ ] Sudah restart aplikasi sebagai Administrator
- [ ] Sudah cek file log terbaru di `Logs/` folder

## 🔗 **Tautan & Support**

### 📚 **Dokumentasi Lengkap**
- **GitHub**: [github.com/MichaelJorky/ADB-Security-Inspector](https://github.com/MichaelJorky/ADB-Security-Inspector)
  - Source code
  - Issue tracker
  - Release notes

### 🎥 **Video Tutorial**
- **YouTube**: [YouTube Channel](https://www.youtube.com/channel/UCubtSerA3uEv9IGVWOlgkcQ)
  - Installation guide
  - Feature tutorials
  - Troubleshooting videos

### 💰 **Support Developer**
- **Saweria**: [saweria.co/teknoxpert](https://saweria.co/teknoxpert)
  - Donasi untuk pengembangan
  - Request fitur premium
  - Priority support

## 📝 **FAQ (Frequently Asked Questions)**

### ❓ **Apakah aplikasi ini aman?**
✅ **YA**. Aplikasi ini open-source, tidak mengumpulkan data, dan semua operasi dilakukan lokal.

### ❓ **Apakah perlu install driver terpisah?**
❌ **TIDAK**. Semua komponen ADB sudah termasuk dalam paket.

### ❓ **Apakah bisa untuk non-root device?**
✅ **BISA**. Hampir semua fitur bekerja di device non-root.

### ❓ **Bagaimana cara update aplikasi?**
1. Download versi baru dari GitHub
2. Backup folder `Logs` dan `Backups` jika perlu
3. Ganti file-file di folder lama

### ❓ **Apakah data saya aman?**
✅ **AMAN**. Backup disimpan lokal, tidak ada upload ke cloud.

## ⚠️ **Disclaimer & Legal**

### **Penggunaan yang Bertanggung Jawab**
Aplikasi ini ditujukan untuk:
- Pengujian keamanan perangkat sendiri
- Maintenance perangkat pribadi
- Educational purposes

### **Larangan**
- ❌ Menggunakan untuk perangkat milik orang lain tanpa izin
- ❌ Aktivitas illegal atau malicious
- ❌ Reverse engineering untuk tujuan komersial

### **Tanggung Jawab**
Pengembang tidak bertanggung jawab atas:
- Kerusakan perangkat akibat misuse
- Kehilangan data
- Pelanggaran hukum oleh pengguna

---

> **Tip**: Selalu backup data penting sebelum melakukan operasi sistem!  
> **Support**: Jika aplikasi membantu, pertimbangkan untuk donasi di Saweria!
