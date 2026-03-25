# 🌊 Rasta Pasta Taghazout — Official Restaurant Website

<div align="center">

![Rasta Pasta]((https://www.rastapasta-taghazout.com/images/logo-lion.jpg))

**A full production restaurant website — built, deployed & live**

[![Live Site](https://img.shields.io/badge/🌐_Live_Site-rastapasta--taghazout.com-0A1F18?style=for-the-badge)](https://www.rastapasta-taghazout.com)
[![React](https://img.shields.io/badge/React_19-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev)
[![Vite](https://img.shields.io/badge/Vite_8-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_v4-38BDF8?style=for-the-badge&logo=tailwindcss&logoColor=white)](https://tailwindcss.com)

</div>

---

## 📌 Overview

A client project for **Rasta Pasta Fish Taghazout** — a beachside seafood café & restaurant in **Taghazout, Morocco**, open since 2000.

Built from scratch: design, development, SEO, deployment, and domain setup on production hosting.

> 🔗 **[www.rastapasta-taghazout.com](https://www.rastapasta-taghazout.com)**

---

## ⚡ Tech Stack

```
React 19        — UI framework
Vite 8          — Build tool & dev server
Tailwind CSS v4 — Utility-first styling
Framer Motion   — Page & element animations
React Router v7 — Client-side routing
Lucide React    — Icon library
```

---

## 🎯 Key Features

### 🌍 Bilingual (FR / EN)
- Auto-detects browser language on first visit
- Full French & English translations across all pages
- Language saved to localStorage
- WhatsApp messages pre-filled in correct language

### 📱 Mobile First
- Custom fixed bottom navigation bar (Call · Map · WhatsApp · Menu)
- Touch swipe navigation in photo gallery
- Drag-to-scroll category tabs in menu
- iOS-safe scroll locking for lightbox
- No lag — removed all GPU-heavy blur effects

### 🖼️ Gallery
- 33 real restaurant photos in a responsive grid
- Fullscreen lightbox using `createPortal` (escapes CSS stacking context)
- Swipe left/right on mobile, arrow keys on desktop
- Tap outside photo to close
- Smooth CSS opacity swap (no React re-mount flickering)

### 🎬 Video Tab
- 6 compressed restaurant videos (~2MB each, H264)
- Poster thumbnails — no black cards on load
- `preload="none"` — zero network cost until tapped
- Auto-pauses when scrolled out of viewport

### 🍽️ Interactive Menu
- 19 categories, 100+ dishes extracted from real PDF menu
- Collapse / expand per category with animated height
- Drag-to-scroll tab bar (mouse + touch)
- PDF opens in new tab for download

### 💬 WhatsApp Booking
- Contact form builds a pre-filled WhatsApp message
- Sends directly to restaurant's WhatsApp
- Bilingual message based on active language

### 🟢 Live Open/Closed Badge
- Real-time status based on Morocco timezone (UTC+1)
- Green pulse "Open Now" or red "Closed · Opens 8am"

### 🔍 SEO
- Schema.org structured data: Restaurant, FoodEstablishment, BreadcrumbList
- Image sitemap submitted to Google Search Console
- Open Graph + Twitter Card for social/WhatsApp previews
- Bilingual hreflang tags (fr/en)
- Geo targeting for Taghazout, Agadir region
- Canonical URL pointing to production domain

### ⚡ Performance
- Removed 7 `blur-3xl` GPU blobs (biggest mobile lag cause)
- IntersectionObserver pauses marquee animation off-screen
- CSS-only FadeIn component (no Framer Motion on scroll)
- Images compressed & resized to max 1200px
- Videos compressed from 20MB+ to ~2MB each
- sessionStorage skip on loading screen after first visit

---

## 📁 Structure

```
src/
├── components/
│   ├── Navbar.jsx           Pure CSS mobile overlay (no Framer = no jank)
│   ├── MobileBottomBar.jsx  Fixed bottom nav bar
│   ├── Footer.jsx
│   ├── LoadingScreen.jsx    Cinematic intro with sessionStorage skip
│   ├── ScrollToTop.jsx
│   └── FadeIn.jsx           Lightweight IntersectionObserver fade
├── pages/
│   ├── Home.jsx             Hero · Stats · Featured dishes · Gallery preview
│   ├── Menu.jsx             Collapsible categories · Drag tabs · PDF
│   ├── Gallery.jsx          Photo lightbox · Video tab
│   ├── About.jsx            Story · Values · Real reviews
│   └── Contact.jsx          Quick actions · Map · WhatsApp form
├── constants/
│   ├── data.js              Full menu data + contact info
│   ├── images.js            All image paths + EN/FR alt text
│   ├── lang.js              All UI translations EN/FR
│   └── LangContext.jsx      Language context + localStorage
└── utils/
    └── lockScroll.js        iOS-safe body scroll lock
public/
├── images/                  37 optimised photos
├── videos/                  6 compressed videos + poster thumbnails
├── menu.pdf                 Real restaurant menu
├── sitemap.xml              Image sitemap for Google
└── .htaccess                Apache SPA routing
```

---

## 🚀 Deployment

- **Hosting:** Orange Host (cPanel / LiteSpeed)
- **Domain:** www.rastapasta-taghazout.com
- **HTTPS:** Force redirect enabled
- **Google Search Console:** Verified + sitemap submitted

```bash
npm install
npm run build
# Upload contents of dist/ to public_html/ on cPanel
```

---

## 🛠️ Technical Challenges Solved

| Problem | Solution |
|---|---|
| Gallery lightbox trapped by CSS stacking context | `createPortal` renders directly into `document.body` |
| Double-tap needed on mobile | `onPointerUp` instead of `onClick` — eliminates 300ms delay |
| iOS Safari scroll behind lightbox | `document.body.style.position = 'fixed'` trick |
| Mobile navbar lag | Pure CSS `opacity` transition instead of Framer Motion |
| Videos showing black before load | `ffmpeg` poster thumbnails + `preload="none"` |
| Browser auto-translating to Arabic | `<html translate="no">` + notranslate meta |
| Image oversized in lightbox | `calc(100vw - 128px)` / `calc(100dvh - 134px)` |

---

<div align="center">

**Built by DEX** · DEX, Morocco 🇲🇦


</div>
