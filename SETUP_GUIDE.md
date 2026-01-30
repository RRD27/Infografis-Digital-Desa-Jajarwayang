# 🚀 Panduan Setup GitHub Pages untuk Hosting PDF

Dokumen ini berisi langkah-langkah lengkap untuk mengaktifkan GitHub Pages pada repository ini.

## ✅ Langkah 1: Mengaktifkan GitHub Pages

### Melalui GitHub Web Interface:

1. **Buka Repository Settings**
   - Login ke GitHub
   - Buka repository: https://github.com/RRD27/Infografis-Digital-Desa-Jajarwayang
   - Klik tab **Settings** (pojok kanan atas)

2. **Navigasi ke Pages**
   - Di sidebar kiri, scroll ke bawah
   - Klik **Pages** di bagian "Code and automation"

3. **Konfigurasi Source**
   - Di bagian **Build and deployment**
   - **Source**: Pilih **GitHub Actions** (Recommended)
     - Alternatif: Pilih **Deploy from a branch**
     - Jika memilih branch:
       - Branch: `main` (atau nama branch default Anda)
       - Folder: `/ (root)`
   - Klik **Save**

4. **Tunggu Deployment**
   - GitHub akan memproses deployment
   - Biasanya memakan waktu 1-5 menit
   - Setelah selesai, URL akan muncul dengan pesan hijau:
     ```
     ✅ Your site is live at https://rrd27.github.io/Infografis-Digital-Desa-Jajarwayang/
     ```

## 🔍 Verifikasi Setup

Setelah deployment selesai, cek hal berikut:

### 1. Homepage
Buka: https://rrd27.github.io/Infografis-Digital-Desa-Jajarwayang/

Anda akan melihat halaman landing dengan:
- Header "Infografis Digital Desa Jajarwayang"
- Daftar contoh dokumen PDF
- Informasi cara menambahkan dokumen baru

### 2. Test URL PDF
Coba akses (akan 404 sampai Anda upload PDF pertama):
```
https://rrd27.github.io/Infografis-Digital-Desa-Jajarwayang/pdfs/test.pdf
```

## 📤 Menambahkan PDF Pertama Anda

### Metode 1: Upload via GitHub Web Interface (Termudah)

1. Buka repository di GitHub
2. Klik folder `pdfs/`
3. Klik **Add file** > **Upload files**
4. Drag & drop file PDF Anda
5. Beri commit message, contoh: "Menambahkan peta desa"
6. Klik **Commit changes**
7. Tunggu 1-2 menit untuk deployment otomatis

### Metode 2: Upload via Git Command Line

```bash
# Clone repository (jika belum)
git clone https://github.com/RRD27/Infografis-Digital-Desa-Jajarwayang.git
cd Infografis-Digital-Desa-Jajarwayang

# Copy file PDF ke folder pdfs/
cp /path/to/your/file.pdf pdfs/peta-desa.pdf

# Update index.html untuk menambahkan link
# (Edit file secara manual atau gunakan text editor)

# Commit dan push
git add pdfs/peta-desa.pdf index.html
git commit -m "Menambahkan peta desa"
git push origin main
```

### Metode 3: Upload via GitHub Desktop

1. Clone repository dengan GitHub Desktop
2. Copy file PDF ke folder `pdfs/`
3. File akan muncul di GitHub Desktop
4. Tulis commit message
5. Klik **Commit to main**
6. Klik **Push origin**

## 🎨 Kustomisasi Homepage

Edit file `index.html` untuk menambahkan link ke PDF baru Anda:

```html
<div class="pdf-item">
    <h3>🗺️ Peta Desa</h3>
    <p>Infografis peta wilayah Desa Jajarwayang</p>
    <a href="pdfs/peta-desa.pdf" target="_blank">Buka PDF</a>
</div>
```

Ganti:
- Emoji (🗺️) dengan icon yang sesuai
- Judul dokumen
- Deskripsi
- Nama file PDF

## 🔗 Format URL

Setelah setup, file PDF Anda dapat diakses dengan format:

```
https://rrd27.github.io/Infografis-Digital-Desa-Jajarwayang/pdfs/NAMA-FILE.pdf
```

Contoh:
- `https://rrd27.github.io/Infografis-Digital-Desa-Jajarwayang/pdfs/peta-desa.pdf`
- `https://rrd27.github.io/Infografis-Digital-Desa-Jajarwayang/pdfs/laporan-keuangan-2024.pdf`
- `https://rrd27.github.io/Infografis-Digital-Desa-Jajarwayang/pdfs/struktur-organisasi.pdf`

## ⚙️ GitHub Actions (Opsional)

Repository ini sudah dilengkapi dengan GitHub Actions workflow (`.github/workflows/deploy.yml`) yang akan:
- Otomatis deploy setiap kali ada push ke branch main
- Dapat di-trigger manual dari tab Actions

### Menggunakan GitHub Actions untuk Deployment:

1. Di Settings > Pages, pilih **Source: GitHub Actions**
2. Workflow akan berjalan otomatis setiap push
3. Lihat progress di tab **Actions**

## 📱 Fitur Tambahan

### 1. Custom Domain (Opsional)

Jika Anda memiliki domain sendiri (contoh: `desajajarwayang.com`):

1. Beli domain dari registrar (Namecheap, GoDaddy, dll)
2. Di pengaturan DNS domain, tambahkan record:
   ```
   Type: CNAME
   Name: www
   Value: rrd27.github.io
   ```
3. Buat file `CNAME` di root repository dengan isi: `www.desajajarwayang.com`
4. Di Settings > Pages, masukkan custom domain
5. Tunggu propagasi DNS (bisa 24-48 jam)

### 2. Redirect dari Root ke www

Tambahkan A record di DNS:
```
Type: A
Name: @
Value: 185.199.108.153
Value: 185.199.109.153
Value: 185.199.110.153
Value: 185.199.111.153
```

## 🛠️ Troubleshooting

### Problem: Website tidak muncul setelah 10 menit

**Solusi:**
1. Cek di Settings > Pages apakah ada error message
2. Pastikan file `index.html` ada di root repository
3. Cek tab Actions untuk melihat apakah ada workflow yang gagal
4. Clear cache browser (Ctrl + F5)
5. Coba akses di incognito/private mode

### Problem: PDF menampilkan 404 Not Found

**Solusi:**
1. Pastikan file PDF benar-benar ada di folder `pdfs/`
2. Cek nama file (case-sensitive: `File.pdf` ≠ `file.pdf`)
3. Pastikan tidak ada spasi dalam nama file
4. Tunggu beberapa menit untuk cache GitHub
5. Coba force refresh (Ctrl + Shift + R)

### Problem: GitHub Actions workflow gagal

**Solusi:**
1. Cek tab Actions untuk error message
2. Pastikan permissions sudah di-set dengan benar
3. Di Settings > Actions > General, pastikan:
   - Workflow permissions: "Read and write permissions"
   - Allow GitHub Actions to create and approve pull requests: Checked

### Problem: Changes tidak muncul setelah push

**Solusi:**
1. Tunggu 1-5 menit untuk deployment
2. Hard refresh browser (Ctrl + F5)
3. Clear browser cache
4. Coba di browser lain atau incognito mode

## 📞 Bantuan Lebih Lanjut

- **GitHub Pages Documentation**: https://docs.github.com/en/pages
- **GitHub Actions Documentation**: https://docs.github.com/en/actions
- **Buat Issue**: https://github.com/RRD27/Infografis-Digital-Desa-Jajarwayang/issues

## ✨ Tips & Best Practices

1. **Ukuran File**: Batasi ukuran PDF maksimal 10-20 MB untuk loading cepat
2. **Kompresi**: Gunakan tools seperti Ghostscript (offline/open source) atau SmallPDF (online) untuk kompresi. **Perhatian:** Untuk dokumen sensitif, gunakan tools offline untuk menjaga privasi data.
3. **Penamaan**: Gunakan nama yang deskriptif dan SEO-friendly
4. **Organisasi**: Gunakan subfolder di `pdfs/` jika punya banyak kategori:
   - `pdfs/2024/laporan-januari.pdf`
   - `pdfs/peta/peta-wilayah.pdf`
   - `pdfs/demografi/data-penduduk.pdf`
5. **Backup**: Selalu backup file PDF di tempat lain juga
6. **Version Control**: Gunakan nama dengan versi: `laporan-keuangan-v2.pdf`

## 🎉 Selamat!

Setup Anda sudah selesai! Sekarang Anda memiliki hosting PDF profesional dengan URL yang mudah dibagikan.

**Next Steps:**
1. Upload PDF pertama Anda
2. Update `index.html` dengan informasi yang sesuai
3. Bagikan URL ke rekan-rekan Anda
4. Pantau penggunaan di GitHub Insights

Selamat menggunakan GitHub Pages! 🚀
