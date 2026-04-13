# CJC Photography — Website Guide

## 📁 File Structure
```
portfolio/
├── index.html       ← All pages
├── css/style.css    ← All styling
├── js/main.js       ← ✏️ Edit stats, bio, client data here
└── images/
    ├── logo.png      ← Already included
    ├── hero.jpg      ← Add your hero image
    ├── charlie.jpg   ← Add your portrait (About page)
    └── clients/      ← Add all client + service photos here
```

---

## 🚀 Publishing on GitHub Pages
1. Go to github.com → your `cjcphotography.github.io` repo
2. Delete old files or upload over them
3. Upload everything inside the `portfolio/` folder (not the folder itself)
4. Settings → Pages → main branch / (root) → Save
5. Live at: `https://cjcphotography.github.io`

---

## 📸 How to Add Photos (Google Drive → Website)

### Step 1 — Download from Google Drive
- Open Google Drive
- Right click the photo → **Download**
- It saves to your Downloads folder

### Step 2 — Rename simply (no spaces, no capitals)
| Photo | Rename to |
|---|---|
| Your hero/banner photo | `hero.jpg` |
| Your portrait | `charlie.jpg` |
| Pucks thumbnail | `pucks-thumb.jpg` |
| Pucks photo 1 | `pucks-1.jpg` |
| Pucks photo 2 | `pucks-2.jpg` |
| Pucks photo 3 | `pucks-3.jpg` |
| Women in Business thumbnail | `wib-thumb.jpg` |
| Women in Business photo 1 | `wib-1.jpg` |
| StFX thumbnail | `stfx-thumb.jpg` |
| Oliver Bray thumbnail | `oliver-thumb.jpg` |
| Photography service thumbnail | `service-photo.jpg` |
| Videography service thumbnail | `service-video.jpg` |
| Gallery photos | `photo1.jpg`, `photo2.jpg`, etc. |

### Step 3 — Upload to GitHub
- Go to your repo on GitHub
- For hero/charlie/gallery photos: click **Add file → Upload files** from root
- For client photos: click into `images/` → `clients/` folder first, then upload
- Drag photos in → **Commit changes**

### Step 4 — Connect photos to the website

**Hero image** — in `index.html` find the `hero-image-placeholder` div and replace the whole div with:
```html
<img src="images/hero.jpg" alt="CJC Photography">
```

**Gallery photos** — in `index.html` replace each placeholder div like:
```html
<div class="gallery-item img-reveal" style="background:var(--mist);...">photo 1</div>
```
With:
```html
<div class="gallery-item img-reveal"><img src="images/photo1.jpg" alt="Event photo"></div>
```

**Client thumbnails & photos** — open `js/main.js`, find each client and update:
```js
thumbnail: "images/clients/pucks-thumb.jpg",
photos: ["images/clients/pucks-1.jpg", "images/clients/pucks-2.jpg", "images/clients/pucks-3.jpg"]
```

**Service thumbnails** — in `js/main.js` find SERVICES and update:
```js
thumbnail: "images/clients/service-photo.jpg"
```

**Your portrait (About page)** — in `index.html` find `about-portrait-placeholder` div and replace with:
```html
<img src="images/charlie.jpg" alt="Charlie Caddick">
```

---

## ✏️ Quick Edits in js/main.js
| What | Where |
|---|---|
| Stats | `STATS` object at top |
| Contact info | `CONTACT` object |
| Client descriptions/stats | `CLIENTS` array |
| Service descriptions | `SERVICES` array |
| About bio | `ABOUT` object |
