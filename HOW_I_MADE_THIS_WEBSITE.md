# How I Made the FitKari Website

## A Step-by-Step Guide to Creating This Project

---

## Overview

This document explains how I conceptualized, designed, and built the FitKari website from scratch. This project demonstrates practical application of business concepts (market research, product development, customer targeting) combined with digital skills (web development, UX design, deployment).

---

## 1. Market Research & Problem Identification

### The Survey Process

I conducted primary research using Google Forms to understand:
- How people feel about their body image
- Experiences with body shaming
- What they want from clothing brands
- Interest in size-inclusive fashion

**Survey Stats (40 Respondents):**
- 77.5% want breathable fabric
- 65% say size-inclusive designs influence purchases
- 50% would wear a size-inclusive dress
- 45% face body shaming weekly

### Key Findings

The research revealed:
1. **Problem**: Traditional sizing doesn't accommodate real body changes
2. **Gap**: Most brands design for "ideal" bodies, not real ones
3. **Opportunity**: 65% want better size options
4. **Solution**: Create adaptive clothing that fits multiple sizes

---

## 2. Brand Concept: FitKari

### What is FitKari?

FitKari is a size-inclusive fashion brand with one core belief: **"Your body is not a problem to solve."**

### Brand Values

| Value | Description |
|-------|-------------|
| **Adaptive Sizing** | One dress fits 3 sizes (e.g., L-XL-XXL) |
| **Body Positivity** | Fashion that celebrates every body |
| **Comfort First** | Soft, breathable Mul cotton fabric |
| **Sustainability** | Reduce clothing waste by reducing size-based repurchasing |

### Target Audience

- Women aged 18-35
- People who experience body changes (weight fluctuation, pregnancy)
- Those seeking comfortable, inclusive clothing
- Budget-conscious but quality-focused buyers

---

## 3. Product Development

### The Adaptive Dress Concept

Each FitKari dress is designed to:
- Fit 3 consecutive sizes (e.g., S-M-L or L-XL-XXL)
- Adjust through drawstrings and elastic panels
- Accommodate body changes over time
- Provide comfort with Mul cotton fabric

### Product Line

| Product | Sizes | Price | Fabric |
|---------|-------|-------|--------|
| Soft-stretch bloom (Pink dress) | XS-S-M | ₹1,499 | Mul Cotton |
| The Grey Grace (Grey dress) | L-XL-XXL | ₹1,499 | Mul Cotton |

---

## 4. Website Design Process

### Design Decisions

#### Color Palette
| Color | Hex Code | Usage |
|-------|----------|-------|
| Terracotta | #D4704A | Primary accent, CTAs |
| Sand | #F5EFE0 | Backgrounds |
| Clay | #C4956A | Secondary accents |
| Cream | #FDFAF4 | Main background |
| Deep Brown | #1C1209 | Text, contrast |

**Why these colors?**
- Warm, earthy tones reflect the natural/comfortable brand identity
- Terracotta stands out but isn't aggressive
- Cream/Sand backgrounds are easy on the eyes

#### Typography
- **Playfair Display** (serif) — Elegant headings, brand identity
- **DM Sans** (sans-serif) — Clean body text, readability

#### Layout Principles
- **Two-column grids** for balance (hero, story sections)
- **Card-based design** for products
- **Consistent spacing** (2rem gaps, 16px+ padding)
- **Mobile-first responsive** design

---

## 5. Technical Implementation

### Technologies Used

| Technology | Purpose | Why I Used It |
|------------|---------|---------------|
| HTML5 | Page structure | Foundation of all websites |
| CSS3 | Styling & layout | Controls look and feel |
| JavaScript | Interactivity | Modals, slideshows |
| GitHub | Version control | Track changes, collaboration |
| Cloudflare Pages | Hosting | Free, fast, reliable |

### No External Frameworks

I built this with **plain HTML, CSS, and JavaScript** because:
- Lightweight (fast loading)
- No dependencies to maintain
- Easy to understand and modify
- Demonstrates core web development skills

---

## 6. Website Structure

```
index.html (Main file - everything is here)
├── <head> — Meta tags, title, fonts, CSS styles
├── <body>
│   ├── <nav> — Navigation bar
│   ├── <section.hero> — Hero with slideshow
│   ├── <section.story> — Brand story with slideshow
│   ├── <section.stats> — Body shaming statistics
│   ├── <section.survey> — Survey insights
│   ├── <section.products> — Product cards
│   ├── <section.values> — Brand values
│   ├── <section.insta> — Social proof
│   ├── <section.newsletter> — Email capture
│   ├── <footer> — Links, social, copyright
│   ├── <div.modal> — Product image modals
│   └── <script> — JavaScript functions
```

---

## 7. Key Features Explained

### Feature 1: Image Slideshows

**How it works:**
```javascript
// Change slide every 5 seconds
setInterval(showHeroSlide, 5000);

// Toggle active class on slides
heroSlides.forEach((slide, index) => {
  slide.classList.toggle('active', index === heroSlideIndex);
});
```

**CSS for fade effect:**
```css
.hero-slide {
  opacity: 0;
  transition: opacity 3s ease-in-out;
}
.hero-slide.active {
  opacity: 1;
}
```

### Feature 2: Product Image Modal (Gallery)

**User flow:**
1. Click product image → Modal opens
2. Scroll horizontally to see more images
3. Click thumbnails to jump to specific image
4. Click X or outside modal or press Escape to close

**JavaScript structure:**
```javascript
function openModal() {
  document.getElementById('productModal').classList.add('active');
}

function closeModal() {
  document.getElementById('productModal').classList.remove('active');
}

function selectImage(index) {
  // Scroll gallery to specific position
  gallery.scrollTo({ left: scrollPosition, behavior: 'smooth' });
}
```

### Feature 3: WhatsApp Integration

**Purpose:** Direct customer communication for orders

```html
<button onclick="window.open('https://wa.me/919428913529?text=Hi! I am interested in...','_blank')">
  Order via WhatsApp
</button>
```

### Feature 4: Responsive Design

**How it adapts:**
```css
/* Desktop: 2 columns */
.product-grid { grid-template-columns: 1fr 1fr; }

/* Tablet/Mobile: 1 column */
@media (max-width: 768px) {
  .product-grid { grid-template-columns: 1fr; }
}
```

---

## 8. Deployment Process

### Step 1: Upload to GitHub

1. Created repository at `github.com/PruthvishGhedia/fitkari`
2. Initialized git in project folder
3. Committed all files
4. Pushed to remote repository

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/PruthvishGhedia/fitkari.git
git push -u origin main
```

### Step 2: Connect to Cloudflare Pages

1. Went to [pages.cloudflare.com](https://pages.cloudflare.com)
2. Connected GitHub account
3. Selected the `fitkari` repository
4. Cloudflare auto-detected it's a static HTML site
5. Deploy completed in ~1 minute

### Live URL: fitkari.pages.dev

---

## 9. Design Principles Applied

### Visual Hierarchy

1. **Hero** — Biggest impact, clear value proposition
2. **Stats** — Immediate credibility with data
3. **Products** — Clear call-to-action
4. **Values** — Reinforce brand beliefs

### User Experience (UX)

| Principle | Implementation |
|-----------|---------------|
| **Clarity** | Simple navigation, clear labels |
| **Accessibility** | Good contrast, readable fonts |
| **Speed** | No heavy frameworks, optimized images |
| **Mobile-friendly** | Responsive at all screen sizes |
| **Direct contact** | WhatsApp integration |

### Conversion Optimization

- **CTA buttons** prominently placed
- **WhatsApp** for instant communication
- **Product galleries** for better product view
- **Social proof** via Instagram section

---

## 10. What I Learned (Skills Demonstrated)

### Technical Skills
- HTML5 semantic markup
- CSS3 Flexbox and Grid layouts
- JavaScript DOM manipulation
- Git version control
- Cloud deployment

### Business Skills
- Market research & survey design
- Data analysis (interpreting survey results)
- Brand positioning
- Target audience identification
- Product differentiation

### Design Skills
- Color theory application
- Typography selection
- Layout composition
- Responsive design
- User experience considerations

---

## 11. How to Recreate This Project

### Quick Start

1. **Create index.html** — Basic HTML structure
2. **Add CSS in `<style>` tag** — All styling inline for simplicity
3. **Add JavaScript in `<script>` tag** — All interactivity inline
4. **Create assets folder** — Store images there
5. **Link images** — Use relative paths (`assets/image.jpg`)

### File Naming Conventions

| Purpose | Naming | Example |
|---------|--------|---------|
| Product images | Product-1-1.jpeg | Product-1-1.jpeg |
| Product 2 images | product-2-1.jpg | product-2-1.jpg |
| Hero images | hero-1.jpg, hero-2.jpg | hero-1.jpg |
| Story images | story-1.jpg | story-1.jpg |
| Logo | logo.jpg | logo.jpg |

### Tips for Beginners

1. **Start simple** — Get the structure right first
2. **Test frequently** — Check changes in browser often
3. **Use browser inspector** — Right-click → Inspect to debug
4. **Google fonts** — Use Google Fonts for professional typography
5. **Color variables** — Define colors in CSS variables for easy changes

---

## 12. For the Jury: Why This Project Matters

### Demonstrates Business Understanding

- **Research-driven**: Decisions based on actual survey data
- **Problem-solution**: Clear market gap identified
- **Differentiated**: Unique value proposition (adaptive sizing)

### Demonstrates Technical Skills

- **Full-stack thinking**: From design to deployment
- **Modern tools**: GitHub, Cloudflare Pages
- **Clean code**: Well-organized, commented HTML/CSS/JS

### Demonstrates Presentation Skills

- **Clear narrative**: Problem → Research → Solution → Product
- **Data-backed**: Real survey results support claims
- **Professional output**: Live website proves capability

### Future Enhancements (Scalability)

If I had more time, I would add:
- Shopping cart functionality
- Payment gateway integration
- User accounts and order tracking
- Blog for content marketing
- Email newsletter automation

---

## Conclusion

This website represents the intersection of business insight and technical implementation. It's not just a pretty page — it's a proof-of-concept backed by real market research, designed to solve a real problem, and built with professional-grade tools.

**Live Website:** fitkari.pages.dev
**Repository:** github.com/PruthvishGhedia/fitkari

---

*This document was created to explain the FitKari website development process for academic presentation purposes.*