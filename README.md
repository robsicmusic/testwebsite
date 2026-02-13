# Robsic Website - Setup Guide

Welcome! This guide will help you set up your music producer website on GitHub Pages.

## 📁 File Structure

```
your-repository/
│
├── index.html          (Main page with sample packs)
├── mastering.html      (Mastering services page)
├── images/             (Create this folder for your images)
│   ├── pack1.jpg
│   ├── pack2.jpg
│   └── pack3.jpg
│
└── audio/              (Create this folder for your audio demos)
    ├── demo1.mp3
    ├── demo2.mp3
    └── demo3.mp3
```

## 🚀 Quick Start - GitHub Pages Setup

### Step 1: Create a GitHub Account
1. Go to https://github.com
2. Sign up for a free account if you don't have one

### Step 2: Create a New Repository
1. Click the "+" icon in the top right → "New repository"
2. Name it: `your-username.github.io` (replace "your-username" with your actual GitHub username)
3. Make it **Public**
4. Check "Add a README file"
5. Click "Create repository"

### Step 3: Upload Your Files
1. Click "Add file" → "Upload files"
2. Drag and drop `index.html` and `mastering.html`
3. Click "Commit changes"

### Step 4: Enable GitHub Pages
1. Go to repository "Settings" (top menu)
2. Click "Pages" in the left sidebar
3. Under "Source", select "main" branch
4. Click "Save"
5. Your site will be live at: `https://your-username.github.io`

## ✏️ What You Need to Replace

### In `index.html`:

#### 1. **Product Images** (Lines ~200-250)
Replace the placeholder divs with your own images:

```html
<!-- BEFORE -->
<div class="card-image">Your Image Here</div>

<!-- AFTER -->
<div class="card-image" style="background: url('images/pack1.jpg') center/cover;"></div>
```

#### 2. **Audio Files** (Lines ~200-250)
Update the audio source paths:

```html
<!-- BEFORE -->
<audio id="audio1" src="demo1.mp3"></audio>

<!-- AFTER -->
<audio id="audio1" src="audio/demo1.mp3"></audio>
```

#### 3. **Product Details**
Update the pack names, descriptions, and prices to match your actual products.

#### 4. **Purchase Links**
Replace the `#` in the "Get This Pack" buttons with your actual purchase links:

```html
<!-- BEFORE -->
<a href="#" class="button primary">Get This Pack</a>

<!-- AFTER -->
<a href="https://gumroad.com/your-link" class="button primary">Get This Pack</a>
```

Popular platforms for selling:
- Gumroad: https://gumroad.com
- Sellfy: https://sellfy.com
- Payhip: https://payhip.com

#### 5. **Spotify Embed**
1. Go to your Spotify artist page
2. Click "..." → "Share" → "Embed artist"
3. Copy the embed code
4. Replace the iframe in the Spotify section (around line 280)

#### 6. **Social Media Links** (Footer section)
Replace `#` with your actual social media URLs:

```html
<a href="https://instagram.com/your-username" target="_blank">Instagram</a>
<a href="https://youtube.com/@your-channel" target="_blank">YouTube</a>
<a href="https://tiktok.com/@your-username" target="_blank">TikTok</a>
```

---

### In `mastering.html`:

#### 1. **Pricing**
Update the mastering package prices to match your actual rates (around lines 350-450).

#### 2. **FAQ Answers**
Customize the FAQ answers to reflect your specific process and policies.

#### 3. **Contact Form Setup**
You need to configure the form to actually send emails. Here are your options:

**Option A: Formspree (Easiest, Free tier available)**
1. Go to https://formspree.io
2. Sign up and create a new form
3. Get your form endpoint
4. Update the form code (around line 500):

```javascript
fetch('https://formspree.io/f/YOUR_FORM_ID', {
  method: 'POST',
  body: formData,
  headers: { 'Accept': 'application/json' }
}).then(response => {
  if (response.ok) {
    document.getElementById('successMessage').classList.add('show');
    this.reset();
  }
});
```

**Option B: Basin (Free, no signup needed)**
1. Go to https://usebasin.com
2. Create a form and get your endpoint
3. Similar setup to Formspree

**Option C: Simple mailto (Basic, not recommended)**
```html
<form action="mailto:youremail@example.com" method="post" enctype="text/plain">
```

#### 4. **Social Media Links**
Same as in `index.html` - update footer links.

---

## 🎨 Customization Tips

### Change Colors
The main purple color is `#a855f7`. To change it:
1. Open the HTML file in a text editor
2. Press Ctrl+F (or Cmd+F on Mac)
3. Search for `#a855f7`
4. Replace with your preferred color (use a color picker like https://colorpicker.me)

### Add More Sample Packs
Copy one of the existing card blocks:

```html
<div class="card">
  <div class="card-image" style="background: url('images/pack4.jpg') center/cover;"></div>
  <h3>Your New Pack Name</h3>
  <p class="card-description">Pack description here</p>
  <div class="price">$29.99</div>
  <audio id="audio4" src="audio/demo4.mp3"></audio>
  <button class="audio-btn" onclick="toggleAudio('audio4', this)">▶ Preview Demo</button>
  <a href="https://your-link.com" class="button primary">Get This Pack</a>
</div>
```

---

## 📸 Image Guidelines

### Recommended Image Specs:
- **Product images**: 800x800px, JPG or PNG
- **File size**: Keep under 500KB for fast loading
- **Format**: JPG for photos, PNG for graphics with transparency

### Free Image Tools:
- **Canva**: https://canva.com (create product covers)
- **Remove.bg**: https://remove.bg (remove backgrounds)
- **TinyPNG**: https://tinypng.com (compress images)

---

## 🎵 Audio File Guidelines

### Recommended Audio Specs:
- **Format**: MP3
- **Bitrate**: 128-192 kbps (good quality, smaller file size)
- **Length**: 30-60 seconds max (keeps files small)
- **File size**: Aim for under 2MB per file

### Audio Editing:
- **Audacity** (Free): https://audacityteam.org
- Fade in/out your demos for a professional touch

---

## 🔧 Troubleshooting

### Images not showing?
- Make sure image paths are correct
- Check that files are in the right folders
- File names are case-sensitive on GitHub Pages

### Audio not playing?
- Verify audio files are uploaded to GitHub
- Check file paths in the code
- Try a different browser

### Form not working?
- You need to set up a form service (see Contact Form Setup above)
- Test the form after configuration

### Site not updating?
- GitHub Pages can take 5-10 minutes to update
- Clear your browser cache (Ctrl+Shift+Delete)
- Try incognito/private mode

---

## 📱 Mobile Optimization

Your site is already mobile-responsive! It will automatically adjust for:
- Desktop computers
- Tablets
- Smartphones

Test it on different devices to make sure everything looks good.

---

## 🚀 Going Further

### Custom Domain (Optional)
1. Buy a domain (GoDaddy, Namecheap, etc.)
2. In your repository settings → Pages
3. Add your custom domain
4. Update DNS settings (GitHub provides instructions)

### Analytics
Add Google Analytics to track visitors:
1. Create account at https://analytics.google.com
2. Get your tracking code
3. Add it before the closing `</head>` tag in both HTML files

### SEO (Search Engine Optimization)
Add these to the `<head>` section:

```html
<meta name="description" content="Professional sample packs and mastering services for electronic music producers">
<meta name="keywords" content="sample packs, mastering, electronic music, producer">
```

---

## 💡 Support

If you need help:
1. Check GitHub Pages documentation: https://pages.github.com
2. Search Stack Overflow for specific issues
3. GitHub community forum: https://github.community

---

## ✅ Checklist Before Launch

- [ ] All images replaced and displaying correctly
- [ ] Audio files working on all packs
- [ ] Purchase links updated
- [ ] Spotify embed updated
- [ ] Social media links added
- [ ] Contact form configured and tested
- [ ] Mastering prices updated
- [ ] FAQ answers customized
- [ ] Test on mobile devices
- [ ] Test on different browsers (Chrome, Firefox, Safari)

---

Good luck with your website! 🎵🚀
