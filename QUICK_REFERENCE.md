# 📋 Quick Reference - GitHub Pages Setup

## 🌐 Your URLs

**Homepage:**
```
https://rrd27.github.io/Infografis-Digital-Desa-Jajarwayang/
```

**PDF Files:**
```
https://rrd27.github.io/Infografis-Digital-Desa-Jajarwayang/pdfs/YOUR-FILE-NAME.pdf
```

---

## 🚀 Activate GitHub Pages (Do This First!)

1. Go to: https://github.com/RRD27/Infografis-Digital-Desa-Jajarwayang/settings/pages
2. Under **Build and deployment**:
   - **Source**: Select **GitHub Actions** OR **Deploy from a branch**
   - If using branch: Select **main** and **/ (root)**
3. Click **Save**
4. Wait 2-5 minutes
5. Refresh page - you'll see: ✅ "Your site is live at..."

---

## 📤 Upload PDF Files - 3 Ways

### Method 1: GitHub Website (Easiest) ✨
1. Go to: https://github.com/RRD27/Infografis-Digital-Desa-Jajarwayang/tree/main/pdfs
2. Click **Add file** → **Upload files**
3. Drag & drop your PDF
4. Click **Commit changes**
5. Done! Wait 1-2 minutes

### Method 2: Git Command Line
```bash
git clone https://github.com/RRD27/Infografis-Digital-Desa-Jajarwayang.git
cd Infografis-Digital-Desa-Jajarwayang
cp /path/to/your-file.pdf pdfs/
git add pdfs/your-file.pdf
git commit -m "Add your-file.pdf"
git push
```

### Method 3: GitHub Desktop
1. Clone repo in GitHub Desktop
2. Copy PDF to `pdfs/` folder
3. Commit changes
4. Push to origin

---

## ✏️ Add Link to Homepage

Edit `index.html` and add this inside the `<div class="pdf-list">`:

```html
<div class="pdf-item">
    <h3>📄 Your Document Title</h3>
    <p>Brief description of the document</p>
    <a href="pdfs/your-file-name.pdf" target="_blank">Buka PDF</a>
</div>
```

---

## 📝 File Naming Rules

✅ **Good:**
- `peta-desa-2024.pdf`
- `laporan-keuangan.pdf`
- `struktur-organisasi.pdf`

❌ **Bad:**
- `Peta Desa.pdf` (has spaces)
- `file#1.pdf` (special characters)
- `doc.pdf` (not descriptive)

**Rules:**
- Use lowercase
- Use hyphens instead of spaces
- No special characters
- Be descriptive

---

## ✅ Checklist After Setup

- [ ] Activate GitHub Pages in Settings
- [ ] Wait for deployment (check green checkmark)
- [ ] Visit homepage URL
- [ ] Upload first PDF file
- [ ] Test PDF URL directly
- [ ] Update index.html with PDF link
- [ ] Share URL with team

---

## 🆘 Troubleshooting

**Site not loading?**
- Wait 5-10 minutes after activation
- Check Settings > Pages for errors
- Try incognito/private mode
- Clear browser cache (Ctrl + F5)

**PDF showing 404?**
- Verify file is in `pdfs/` folder
- Check file name (case-sensitive!)
- Wait 2-3 minutes after upload
- Check for typos in URL

**Changes not showing?**
- Wait 1-5 minutes for deployment
- Hard refresh (Ctrl + Shift + R)
- Check Actions tab for deployment status

---

## 📚 Documentation Files

- **README.md** - Overview and detailed instructions
- **SETUP_GUIDE.md** - Complete step-by-step setup guide
- **pdfs/README.md** - Instructions for PDF folder
- **QUICK_REFERENCE.md** - This file (quick tips)

---

## 📧 Share Your PDFs

Once uploaded, share using this format:
```
https://rrd27.github.io/Infografis-Digital-Desa-Jajarwayang/pdfs/FILE-NAME.pdf
```

Can be used in:
- WhatsApp messages
- Email
- Social media posts
- Documents
- QR codes

---

## 🎯 Next Steps

1. **Activate GitHub Pages** (if not done)
2. **Upload your first PDF**
3. **Test the URL**
4. **Customize index.html** with your content
5. **Share with your team**

---

## 💡 Pro Tips

- Keep file sizes under 10-20 MB
- Compress PDFs before uploading
- Use descriptive file names
- Update index.html for easy navigation
- Create subfolders for organization: `pdfs/2024/`, `pdfs/reports/`

---

**Need Help?** Read SETUP_GUIDE.md or create an issue on GitHub!
