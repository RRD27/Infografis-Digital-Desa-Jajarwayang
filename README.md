# Infografis Digital Desa Jajarwayang

Sebuah upaya digitalisasi informasi berupa desain grafis digital dan poster digital untuk Desa Jajarwayang yang di-hosting menggunakan GitHub Pages.

## 🌐 URL Akses

Website ini dapat diakses melalui:
- **Homepage**: https://rrd27.github.io/Infografis-Digital-Desa-Jajarwayang/
- **PDF Files**: https://rrd27.github.io/Infografis-Digital-Desa-Jajarwayang/pdfs/nama-file.pdf

## 📋 Tentang Proyek

Repository ini merupakan pusat dokumentasi digital untuk Desa Jajarwayang. Di sini tersedia berbagai infografis dan poster digital yang berisi informasi penting tentang desa dalam format PDF yang mudah diakses.

## 🚀 Cara Mengaktifkan GitHub Pages

Jika GitHub Pages belum aktif, ikuti langkah berikut:

1. **Buka Settings Repository**
   - Pergi ke repository di GitHub
   - Klik tab **Settings**

2. **Aktifkan GitHub Pages**
   - Scroll ke bagian **Pages** di sidebar kiri
   - Di bagian **Source**, pilih:
     - Branch: `main` (atau branch yang Anda gunakan)
     - Folder: `/ (root)`
   - Klik **Save**

3. **Tunggu Deployment**
   - GitHub akan memproses deployment (biasanya 1-5 menit)
   - URL akan muncul di bagian atas halaman Pages
   - Setelah selesai, Anda akan melihat: "Your site is published at https://rrd27.github.io/Infografis-Digital-Desa-Jajarwayang/"

## 📁 Struktur Folder

```
Infografis-Digital-Desa-Jajarwayang/
├── index.html          # Halaman utama website
├── pdfs/               # Folder untuk file PDF
│   ├── README.md       # Panduan untuk folder PDFs
│   └── *.pdf          # File-file PDF Anda
└── README.md          # File ini
```

## ➕ Cara Menambahkan PDF Baru

### Langkah 1: Upload File PDF

```bash
# Clone repository jika belum
git clone https://github.com/RRD27/Infografis-Digital-Desa-Jajarwayang.git
cd Infografis-Digital-Desa-Jajarwayang

# Tambahkan file PDF ke folder pdfs/
cp /path/to/your/file.pdf pdfs/nama-file-baru.pdf
```

### Langkah 2: Update index.html

Edit file `index.html` dan tambahkan item baru di bagian "Dokumen Tersedia":

```html
<div class="pdf-item">
    <h3>📄 Judul Dokumen</h3>
    <p>Deskripsi singkat dokumen</p>
    <a href="pdfs/nama-file-baru.pdf" target="_blank">Buka PDF</a>
</div>
```

### Langkah 3: Commit dan Push

```bash
git add pdfs/nama-file-baru.pdf index.html
git commit -m "Menambahkan dokumen baru: nama-file-baru.pdf"
git push origin main
```

### Langkah 4: Akses File

Setelah beberapa menit, file dapat diakses di:
```
https://rrd27.github.io/Infografis-Digital-Desa-Jajarwayang/pdfs/nama-file-baru.pdf
```

## 📝 Konvensi Penamaan File

Untuk URL yang profesional dan mudah diingat, gunakan konvensi berikut:

✅ **Yang Baik:**
- `peta-desa-jajarwayang.pdf`
- `laporan-keuangan-2024.pdf`
- `struktur-organisasi.pdf`

❌ **Yang Harus Dihindari:**
- `Laporan Keuangan.pdf` (ada spasi)
- `file#1.pdf` (karakter khusus)
- `doc.pdf` (tidak deskriptif)

## 🔗 Membagikan Link

Anda dapat membagikan link PDF dengan format:
```
https://rrd27.github.io/Infografis-Digital-Desa-Jajarwayang/pdfs/nama-file.pdf
```

Link ini dapat digunakan di:
- Media sosial
- Email
- Dokumen
- Website lain
- Dan platform lainnya

## ⚙️ Kustomisasi

### Mengubah Tampilan Website

Edit file `index.html` untuk:
- Mengubah warna tema
- Menambah/mengurangi section
- Mengubah teks dan konten
- Menambahkan logo atau gambar

### Menambahkan Subdomain Kustom (Opsional)

Jika Anda memiliki domain sendiri:

1. Beli domain dari registrar (Namecheap, GoDaddy, dll)
2. Di pengaturan DNS domain, tambahkan CNAME record:
   ```
   www -> rrd27.github.io
   ```
3. Di repository Settings > Pages, masukkan custom domain
4. Tunggu propagasi DNS (24-48 jam)

## 🛠️ Troubleshooting

### Website tidak muncul?
- Pastikan GitHub Pages sudah diaktifkan di Settings
- Cek bahwa file `index.html` ada di root repository
- Tunggu 5-10 menit setelah push untuk deployment

### PDF tidak bisa diakses?
- Pastikan file ada di folder `pdfs/`
- Cek nama file tidak ada spasi atau karakter khusus
- Pastikan path di link HTML benar (case-sensitive)

### Error 404?
- Periksa penulisan URL (case-sensitive)
- Pastikan branch yang dipilih di Pages settings benar
- Clear cache browser dan coba lagi

## 📞 Kontak

Untuk pertanyaan atau bantuan, silakan buka Issue di repository ini.

## 📄 Lisensi

Konten dalam repository ini digunakan untuk kepentingan dokumentasi publik Desa Jajarwayang.
