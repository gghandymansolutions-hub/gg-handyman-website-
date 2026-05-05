# GG Handyman Solutions — Website

Landing page for GG Operations LLC, Houston TX.

## 📂 Project Structure

```
gg-handyman-website/
├── index.html          ← The whole site (HTML + CSS + JS in one file)
├── assets/
│   ├── logo.png        ← Company logo
│   └── team.jpg        ← Team photo (used in hero morph)
└── README.md
```

## 🚀 Quick Start

### Open and preview locally

1. Open this folder in **VS Code**:
   ```
   File → Open Folder → select gg-handyman-website
   ```

2. Install the **Live Server** extension (by Ritwick Dey) if you don't have it.
   - Go to Extensions tab (Ctrl+Shift+X) → search "Live Server" → install

3. Right-click on `index.html` → **"Open with Live Server"**
   - The site opens in your browser at `http://127.0.0.1:5500`
   - Any changes you save will auto-refresh the browser

---

## ✏️ How to edit common things

### Change the form's destination email
1. Open `index.html`
2. Press `Ctrl+F` (or `Cmd+F`) and search for: `YOUR_WEB3FORMS_ACCESS_KEY_HERE`
3. Replace it with your real Web3Forms access key
   - Get yours free at https://web3forms.com (takes 30 seconds)

### Add your own photos to "About Us"
1. Drop your image files into the `assets/` folder
2. Search in `index.html` for: `data-src=""`
3. Fill in the path:
   ```html
   <div class="about-photo" data-src="assets/your-photo.jpg">
   ```

### Add your own photo to "Our Mission"
Same as above — find:
```html
<div class="mission-img" data-src="">
```
And replace with your image path.

### Replace the sample Google Reviews
Search for: `Maria R.`, `James K.`, `Ashley P.`
Each is a `<div class="review-card">` block — edit the name, text, and avatar letter to match real reviews from your Google Business Profile.

### Change the company info
- **Phone / address / hours** → Currently not on the page; let me know if you want them in the footer or a "Contact" block
- **Social links** → Look for `<div class="social">` near the bottom and replace `href="#"` with your real URLs

---

## 🌐 Deploy

### Option 1: Netlify Drop (easiest, ~2 min)
1. Go to https://app.netlify.com/drop
2. Drag-and-drop the **entire project folder** onto the page
3. Done — you'll get a URL like `https://random-name.netlify.app`

### Option 2: Push to GitHub + Netlify (recommended for ongoing edits)
1. Create a new repo on GitHub
2. From VS Code terminal:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/gg-handyman.git
   git push -u origin main
   ```
3. On Netlify, click **"Add new site" → "Import from Git"** and connect your repo
4. From now on, every time you `git push`, Netlify will auto-deploy

---

## 🛠️ What's inside the site

- **Hero with scroll-driven logo morph** — logo transforms into team photo as you scroll
- **Services grid** (Handyman, Drywall, Plumbing, Electrical, HVAC, Subcontracting)
- **About Us** with photo grid + Book Now CTA
- **Our Mission** with image-and-text layout
- **Google Reviews** with Google logo, badge, and 3 sample reviews
- **Service Area** with embedded interactive Google Map (zoomable)
- **Multi-step Contact Form** (5 steps: Service → Contact → Address → Details → Review)
- **Footer** with Quick Links and social icons

---

## 🎨 Design System

| Element | Value |
|---|---|
| Primary background | `#0a0a0c` (almost-black) |
| Accent / Brand | `#f5c518` (gold) |
| Text | `#e8e8ea` |
| Muted text | `#8a8a93` |
| Display font | Bebas Neue |
| Body font | Manrope |

All colors live as CSS variables at the top of `<style>` in `index.html` — change once, updates everywhere.

---

## 🐛 Common issues

**Map doesn't load**: That's a Google Maps quota thing — it usually works for small traffic. For a real production site, you may want a proper Google Maps API key.

**Form doesn't send emails**: Check that you replaced `YOUR_WEB3FORMS_ACCESS_KEY_HERE` with your real Web3Forms key.

**Logo morph doesn't animate**: Make sure the file is being served by Live Server, not opened directly with `file://` — some browsers block animations on local files.

---

## 📞 Contact / Help

When you have:
- A new feature to add
- The Sedance morph video ready to integrate
- Real reviews to swap in
- Any error or bug

…just bring the project back into a chat and we keep building.
