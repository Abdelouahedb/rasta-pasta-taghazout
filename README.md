# 🌊 Rasta Pasta Taghazout — Restaurant Website

> Live at **[www.rastapasta-taghazout.com](https://www.rastapasta-taghazout.com)**

A full-stack restaurant website built for **Rasta Pasta Fish** — a beachside seafood café & restaurant in Taghazout, Morocco. Since 2000.

---

## 🚀 Tech Stack

| Tool | Use |
|---|---|
| React 19 + Vite | Frontend framework |
| Tailwind CSS v4 | Styling |
| Framer Motion | Animations |
| React Router v7 | Page routing |
| Lucide React | Icons |

---

## ✨ Features

- 🇫🇷🇬🇧 **Bilingual** — Full French & English with auto language detection
- 📱 **Mobile first** — Custom bottom navigation bar, touch swipe gallery
- 🖼️ **Photo gallery** — 33 photos with fullscreen lightbox + swipe navigation
- 🎬 **Video gallery** — 6 real restaurant videos with poster thumbnails
- 🍽️ **Interactive menu** — 19 categories, collapse/expand, drag-to-scroll tabs
- 📄 **PDF menu** — View & download the real menu PDF
- 🟢 **Live open/closed badge** — Real-time based on Morocco timezone
- 💬 **WhatsApp booking** — Form that pre-fills a WhatsApp message to the restaurant
- 🗺️ **Google Maps** — Embedded map + directions link
- ⬆️ **Scroll to top** — Appears after 500px scroll
- ⚡ **Performance** — Removed GPU-heavy blur effects, lazy loading, video preload=none

---

## 🔍 SEO

- Full Schema.org structured data (Restaurant, FoodEstablishment, BreadcrumbList)
- Image sitemap submitted to Google Search Console
- Geo targeting for Taghazout, Agadir region
- Open Graph + Twitter Card for WhatsApp/social previews
- Bilingual hreflang tags (fr/en)
- Canonical URL set to production domain

---

## 📁 Project Structure

```
src/
  components/
    Navbar.jsx          — Sticky navbar, mobile overlay (pure CSS, no lag)
    Footer.jsx          — 4-column footer
    MobileBottomBar.jsx — Fixed bottom nav (Call, Map, WhatsApp, Menu)
    LoadingScreen.jsx   — Cinematic loading screen (sessionStorage skip)
    ScrollToTop.jsx     — Scroll to top button
    FadeIn.jsx          — Lightweight CSS fade-in (no Framer Motion)
  pages/
    Home.jsx            — Hero, marquee, stats, featured dishes, gallery preview
    Menu.jsx            — Collapsible categories, drag tabs, PDF viewer
    Gallery.jsx         — Photo grid + lightbox + video tab
    About.jsx           — Story, values, real reviews
    Contact.jsx         — Quick actions, map, WhatsApp form
  constants/
    data.js             — Menu data (19 categories, 100+ items), contact info
    images.js           — All image paths with alt text (EN + FR)
    lang.js             — All translations EN/FR
    LangContext.jsx     — Language context with localStorage persistence
  utils/
    lockScroll.js       — iOS-safe body scroll lock for lightbox
public/
  images/               — 37 optimised restaurant photos
  videos/               — 6 compressed restaurant videos (~2MB each)
  menu.pdf              — Real restaurant menu PDF
  sitemap.xml           — Image sitemap for Google
  .htaccess             — Apache SPA routing
```

---

## 🌍 Deployment

Deployed on **Orange Host** (cPanel/LiteSpeed) at:
**[www.rastapasta-taghazout.com](https://www.rastapasta-taghazout.com)**

```bash
npm install
npm run build
# Upload dist/ contents to public_html/
```

---


## 👨‍💻 Built by

**DEX** — Mobile security researcher & full-stack developer  
Taghazout, Morocco 🇲🇦

---

*Real client project — live production website*
