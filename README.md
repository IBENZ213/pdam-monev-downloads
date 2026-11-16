# PDAM Monev - Windows Installer Distribution

Repository ini menyediakan installer Windows untuk aplikasi PDAM Monev.

## ⚠️ Penting

- Repository ini **HANYA** berisi binary installer untuk distribusi publik
- Source code aplikasi tersedia di repository terpisah (private)
- Jangan upload source code, credential, atau data sensitif ke repository ini

## 📦 Download Installer

### Versi Terbaru: v1.0.0

| File | Size | SHA256 |
|------|------|--------|
| [PDAM Monev Setup 1.0.0.exe](https://github.com/IBENZ213/pdam-monev-downloads/releases/download/v1.0.0/PDAM.Monev.Setup.1.0.0.exe) | 73.1 MB | `99942762d3b27e5b24c5e060078396934c55be466c887914d9738fc35b22a830` |
| [PDAM Monev Setup 1.0.0.exe.blockmap](https://github.com/IBENZ213/pdam-monev-downloads/releases/download/v1.0.0/PDAM.Monev.Setup.1.0.0.exe.blockmap) | 79.8 KB | - |

## 🔧 Spesifikasi Teknis

### Arsitektur
- **Platform:** Windows 64-bit (x86-64)
- **Executable Type:** PE32+ (64-bit)
- **Installer Type:** NSIS (Nullsoft Scriptable Install System)

### Persyaratan Sistem
- **OS:** Windows 10/11 (64-bit)
- **RAM:** Minimal 2 GB
- **Disk Space:** Minimal 200 MB (untuk instalasi)
- **Permissions:** Administrator rights (untuk instalasi)

### Teknologi
- **Framework:** Electron 28.3.3
- **Build Tool:** electron-builder 24.13.3
- **Node.js Runtime:** Embedded (tidak perlu install terpisah)

## 📥 Cara Instalasi

1. Download installer dari link di atas
2. Verifikasi SHA256 checksum:
   ```powershell
   # PowerShell
   Get-FileHash "PDAM Monev Setup 1.0.0.exe" -Algorithm SHA256
   ```
   ```bash
   # Linux/macOS
   sha256sum "PDAM Monev Setup 1.0.0.exe"
   ```
3. Jalankan installer sebagai Administrator
4. Ikuti wizard instalasi
5. Pilih direktori instalasi (default: `C:\Program Files\PDAM Monev`)
6. Tunggu proses instalasi selesai
7. Klik Finish

## ✅ Verifikasi Instalasi

Setelah instalasi, verifikasi:
- Aplikasi dapat dibuka dari Start Menu atau Desktop shortcut
- Dashboard muncul dengan benar
- Dapat input data dan formula terhitung otomatis
- Dapat create backup dan export PDF/XLSX

## 🔄 Upgrade dari Versi Lama

Jika sudah memiliki versi lama PDAM Monev:

1. **Backup data terlebih dahulu** (Dashboard → Backup → Create)
2. Jalankan installer versi baru
3. Pilih direktori instalasi yang **SAMA** dengan versi lama
4. Installer akan otomatis upgrade tanpa menghapus data
5. Verifikasi data lama tetap terbaca setelah upgrade

## 🐛 Troubleshooting

### Installer tidak bisa dijalankan
- Pastikan download lengkap (cek ukuran file: 73.1 MB)
- Verifikasi SHA256 checksum
- Jalankan sebagai Administrator
- Temporarily disable antivirus jika memblokir

### Data hilang setelah upgrade
- Cek folder backup: `%APPDATA%\PDAM Monev\backups`
- Restore dari backup yang dibuat sebelum upgrade
- Hubungi support jika butuh bantuan

### Aplikasi tidak bisa dibuka
- Cek log di: `%APPDATA%\PDAM Monev\logs`
- Pastikan Windows 10/11 64-bit
- Reinstall jika perlu

## 📋 Release Notes

### v1.0.0 (2026-11-16)
- Initial public release
- Windows NSIS installer (73.1 MB)
- PE32+ x86-64 architecture
- Electron 28.3.3
- electron-builder 24.13.3
- Data preservation on upgrade
- Automatic backup system
- PDF and XLSX export
- Formula calculation engine

## 🔒 Security

- Installer ditandatangani digital
- SHA256 checksum tersedia untuk verifikasi
- Tidak ada data sensitif dalam installer
- Aplikasi berjalan lokal (tidak ada cloud sync)
- Data pengguna tersimpan di `%APPDATA%\PDAM Monev\`

## 📞 Support

Untuk pertanyaan atau masalah:
- GitLab (source of truth): https://gitlab.com/ibenzaieng-group/pdam-monev
- GitHub (mirror): https://github.com/IBENZ213/pdam-monev-mirror

## 📄 License

Proprietary - All rights reserved

---

**Last Updated:** 2026-11-16  
**Repository Purpose:** Public binary distribution only  
**Source Code:** Private repository (not included here)
