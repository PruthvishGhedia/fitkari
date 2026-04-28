# FitKari Website Documentation

## For the Owner: Complete Guide to Managing Your Website

---

## Table of Contents
1. [What is FitKari?](#what-is-fitkari)
2. [How the Website Works](#how-the-website-works)
3. [How to Update Products](#how-to-update-products)
4. [How to Add/Change Images](#how-to-addchange-images)
5. [How to Change Prices or Text](#how-to-change-prices-or-text)
6. [Managing the GitHub Repository](#managing-the-github-repository)
7. [Cloudflare Pages - Making Your Site Live](#cloudflare-pages---making-your-site-live)
8. [Troubleshooting](#troubleshooting)

---

## What is FitKari?

FitKari is your fashion brand that sells adaptive-size dresses. Each dress fits 3 sizes (like L-XL-XXL), making it perfect for real bodies with real changes.

**Your Products:**
- **Soft-stretch bloom** — Pink dress (XS-S-M) — ₹1,499
- **The Grey Grace** — Grey dress (L-XL-XXL) — ₹1,499

**Contact:** WhatsApp — 9428913529

---

## How the Website Works

Your website is built with simple **HTML, CSS, and JavaScript**. Everything is in one file called `index.html`.

### Structure:
```
FitKari/
├── index.html          ← The main website file (all code is here)
├── assets/             ← All images go here
│   ├── hero.jpg        ← Main hero image
│   ├── story.jpg       ← Story section image
│   ├── logo.jpg        ← Your brand logo
│   ├── Product-1-1.jpeg
│   ├── Product-1-2.jpeg
│   ├── Product-1-3.jpeg
│   ├── product-2-1.jpg
│   ├── product-2-2.jpg
│   └── product-2-3.jpg
```

### How Customers Buy:
1. They visit your website
2. They see product images and click to view more (gallery opens)
3. They click "Order via WhatsApp"
4. It opens WhatsApp with a pre-filled message
5. You chat and complete the sale

---

## How to Update Products

### To Change Product Name, Price, or Description:

1. Open `index.html` in any text editor (Notepad, VS Code, etc.)
2. Find the product section (look for "Soft-stretch bloom" or "The Grey Grace")
3. Change the text between the tags:

**Example - Change Price:**
```html
<!-- Find this: -->
<span class="product-price">₹1,499</span>

<!-- Change to: -->
<span class="product-price">₹1,599</span>
```

**Example - Change Product Name:**
```html
<!-- Find this: -->
<h3>Soft-stretch bloom</h3>

<!-- Change to: -->
<h3>New Product Name</h3>
```

### To Update WhatsApp Message:
```html
<!-- Find: -->
onclick="window.open('https://wa.me/919428913529?text=Hi! I am interested in...'

<!-- Change the text after 'text=' to what you want -->
```

---

## How to Add/Change Images

### Step 1: Add Image to Assets Folder
1. Put your new image in the `assets/` folder
2. Use these naming rules:
   - Product 1: `Product-1-1.jpeg`, `Product-1-2.jpeg`, etc.
   - Product 2: `product-2-1.jpg`, `product-2-2.jpg`, etc.
   - Hero: `hero.jpg`
   - Story: `story.jpg`
   - Logo: `logo.jpg`

### Step 2: Update the Code
Open `index.html` and find the image path:

```html
<!-- Product Image Example: -->
<img src="assets/Product-1-1.jpeg" alt="Pink dress">

<!-- Change to your new file: -->
<img src="assets/YourNewImage.jpeg" alt="Your Product">
```

### Important Image Tips:
- Use **.jpg** or **.jpeg** for product images
- Keep images reasonably sized (under 500KB is best)
- Name files simply (no spaces, use - or _)

---

## How to Change Prices or Text

### Common Changes:

**Change Price:**
```html
<span class="product-price">₹1,499</span>
```

**Change Tag (New/Bestseller):**
```html
<span class="product-tag-img">New</span>
<!-- Can change to "Bestseller" or "Sale" -->
```

**Change Description:**
```html
<p>Your description here...</p>
```

**Change WhatsApp Number:**
Find and replace all instances of `919428913529` with your new number.

---

## Managing the GitHub Repository

Your website code is stored on GitHub. Here's how to update it:

### Using GitHub Desktop (Easiest):

1. **Download GitHub Desktop** from https://desktop.github.com
2. Open it and sign in with your GitHub account
3. Click "Clone a Repository" → Select "fitkari"
4. The files will download to your computer

### To Update Your Site:

1. Make changes to `index.html` or add new images in `assets/`
2. Open GitHub Desktop
3. You'll see your changes listed
4. Type a "commit message" (like "Updated prices")
5. Click "Commit to main"
6. Click "Push origin"

Your site will auto-update on Cloudflare Pages in 1-2 minutes!

### Without GitHub Desktop (Manual):

1. Go to https://github.com/PruthvishGhedia/fitkari
2. Click on the file you want to edit
3. Click the "Edit" (pencil) icon
4. Make changes and click "Commit changes"

---

## Cloudflare Pages - Making Your Site Live

Cloudflare Pages hosts your website for free. Here's how it works:

### How Updates Deploy:
1. You push changes to GitHub
2. Cloudflare automatically detects the change
3. Within 1-2 minutes, your live site updates

### To Access Cloudflare:
1. Go to https://pages.cloudflare.com
2. Sign in
3. Select "fitkari" project
4. You can see deployment status here

### To Change Your Domain (Optional):
If you want a custom domain like `fitkari.com`:
1. Go to Cloudflare Dashboard → Pages → fitkari
2. Click "Custom domains"
3. Add your domain name

---

## Troubleshooting

### Site Not Updating?
- Wait 2 minutes for Cloudflare to deploy
- Hard refresh: Press `Ctrl + Shift + R` (Windows) or `Cmd + Shift + R` (Mac)
- Go to Cloudflare Pages → fitkari → Settings → Clear Cache

### Images Not Showing?
- Check the file path is correct (e.g., `assets/hero.jpg`)
- Make sure file extension matches (.jpg vs .jpeg)
- Try a hard refresh

### WhatsApp Not Working?
- Check the phone number in the code
- Make sure it starts with country code (91 for India)

### Want to Add More Products?
1. Copy the product card section
2. Paste below existing products
3. Update images, name, price, description
4. Add a new modal for the gallery

---

## Quick Reference

| Task | Where to Look in Code |
|------|----------------------|
| Change logo | Nav section, `logo.jpg` |
| Change hero image | Hero section, `hero.jpg` |
| Change story image | Story section, `story.jpg` |
| Change Product 1 | Products section, first `.product-card` |
| Change Product 2 | Products section, second `.product-card` |
| Change prices | Look for `<span class="product-price">` |
| Change WhatsApp number | Look for `wa.me/919428913529` |
| Change footer text | Look for `<footer>` section |

---

## Need Help?

If something breaks or you need to make major changes:
1. Don't panic - your code is safely saved on GitHub
2. Try to identify what changed
3. You can always revert to an earlier version via GitHub

**Your GitHub Repo:** https://github.com/PruthvishGhedia/fitkari

---

*Made with ❤️ for FitKari*