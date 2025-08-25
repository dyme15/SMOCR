# 📌 SMOCR - Surat Masuk OCR Organizer
**Lisensi: (C) Dodyk Fahlome 2025**

---

## 📖 Deskripsi
SMOCR adalah aplikasi desktop berbasis **Python + Tkinter** untuk membantu mengelola arsip surat masuk.  
Fitur utamanya:
- OCR otomatis dari file PDF / gambar menggunakan **Tesseract**.
- Deteksi metadata surat (tanggal, bulan, tahun, jenis surat, asal surat, nomor, dan hal).
- Struktur folder otomatis sesuai tahun → bulan → tanggal → jenis surat.
- Rename file surat dengan format konsisten menggunakan poppler.
- Validasi input (ukuran file, karakter terlarang, tanggal valid, dll).
- Antarmuka sederhana dengan GUI Tkinter.

---

## ⚙️ Alur Kerja Program
1. **Pilih File**  
   Pilih file PDF hasil scan → OCR otomatis dijalankan.  
2. **Ekstraksi Metadata**  
   Program mendeteksi tanggal, jenis surat, asal surat, nomor agenda, hal.  
3. **Isi Formulir**  
   Hasil OCR otomatis masuk ke form, bisa diperbaiki manual.  
4. **Validasi**  
   Cek ukuran file, tanggal, karakter terlarang.  
5. **Struktur Folder Otomatis**  
   Dibuat sesuai format: D:\SURAT MASUK <TAHUN><Nomor. BULAN><Tanggal BULAN_SUFFIX>\SURAT MASUK <Jenis Surat>
6. **Rename File**  
   Format: <ASAL_SURAT> - <NOMOR_SURAT>.<JENIS_SURAT> <HAL>.pdf
7. **Pindah File**  
   File dipindahkan ke folder tujuan.

---

## 📂 Struktur Folder
assets/ → ikon & logo aplikasi
   surat.ico → icon aplikasi
   logo_surat.png → logo header
   main.py → kode utama aplikasi

---

## ▶️ Cara Penggunaan
1. Install dependensi: pip install pytesseract pdf2image pillow
> Note:
- Install **Tesseract OCR** lalu sesuaikan path di kode:
  ```
  pytesseract.pytesseract.tesseract_cmd = "C:\Program Files\Tesseract-OCR\tesseract.exe"
  ```
- Install **Poppler** untuk pdf2image lalu sesuaikan `poppler_path`.

2. Jalankan aplikasi: python main.py

3. Pilih file PDF hasil scan.  
4. Periksa hasil OCR, perbaiki bila salah.  
5. Klik **INPUT** untuk memindahkan & rename file.  

---

## 🖼️ Tampilan Aplikasi
- Header: Logo + Judul instansi
- Form Input: Asal Surat, Tanggal, Bulan, Tahun, Jenis Surat, Nomor Agenda, Hal
- Tombol: Cari file & Input
- Validasi: Error bubble / messagebox jika salah input

---

## 📜 Lisensi
**(C) Dodyk Fahlome 2025**  
Aplikasi ini dibuat khusus untuk kebutuhan pengarsipan surat masuk khususnya instansi
tempat saya melakukan kegiatan kerja praktik yaitu Inspektorat Sumatera Utara.
Dilarang memperjualbelikan tanpa izin pemilik.

---

## ✅ To-Do (Pengembangan Lanjutan)
- Tambahkan export Excel daftar surat masuk.
- Fitur searching & indexing arsip.
- Dukungan multi-bahasa (OCR eng+ind).
- Preview PDF sebelum dipindahkan.
