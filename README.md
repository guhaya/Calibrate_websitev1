# Calibrate — Official Website

**Precision Performance Coaching for High-Performing Professionals**
Built by [Guhayavarman](https://www.instagram.com/fitguhay) | Lakchinna Digitals

---

## Overview

Static single-page website for **Calibrate**, a 1:1 online performance coaching brand targeting engineers, product managers, consultants, and founders in Chennai and Bangalore. Built on a pure HTML/CSS/JS stack — zero dependencies, zero build step, deploys in under 60 seconds.

**Live URL:** `https://gvnfit.online` *(update after Vercel domain mapping)*

---

## Stack

| Layer | Technology |
|---|---|
| Markup | HTML5 |
| Styling | CSS3 — custom variables, `clamp()` fluid sizing, Grid, Flexbox |
| Scripting | Vanilla JavaScript (ES6+) |
| Fonts | Google Fonts — Barlow Condensed, Barlow 300, DM Mono |
| Hosting | Vercel (static) |
| Forms | WhatsForm — `https://whatsform.com/a8wbfq` |
| Analytics | *(add Vercel Analytics or Plausible — see below)* |

No npm. No build pipeline. No framework. One file.

---

## Design System

| Token | Value |
|---|---|
| Background | `#192230` |
| Deep BG | `#131d2a` |
| Card | `#2c2f38` |
| Lift | `#3d474e` |
| Accent | `#ffcd00` |
| White | `#F4F4F4` |
| Green | `#3DD68C` |
| Amber | `#FFB020` |
| Red | `#FF4C4C` |
| Heading Font | Barlow Condensed 700–900 |
| Body Font | Barlow 300 |
| Mono/Data Font | DM Mono |

---

## Project Structure

```
calibrate-site/
├── index.html          # Entire website — single file
├── vercel.json         # Vercel routing + headers config
├── .gitignore
└── README.md
```

---

## Local Development

No build step required. Just open the file:

```bash
# Option 1 — open directly
open index.html

# Option 2 — serve locally (recommended to test fonts/links)
npx serve .
# or
python3 -m http.server 8080
# then visit http://localhost:8080
```

---

## Deployment — Vercel

### First deploy (CLI)

```bash
# Install Vercel CLI if you haven't
npm i -g vercel

# From the project root
vercel

# Follow the prompts:
# - Link to existing project or create new
# - Framework: Other
# - Root directory: ./
# - Build command: (leave blank)
# - Output directory: ./
```

### Subsequent deploys

```bash
vercel --prod
```

### Deploy via GitHub (recommended)

1. Push this repo to GitHub
2. Go to [vercel.com/new](https://vercel.com/new)
3. Import the GitHub repo
4. Settings:
   - **Framework Preset:** Other
   - **Root Directory:** `./`
   - **Build Command:** *(leave blank)*
   - **Output Directory:** `./`
5. Click **Deploy**

Every `git push` to `main` auto-deploys to production.

---

## Custom Domain (gvnfit.online)

1. In Vercel dashboard → Project → Settings → Domains
2. Add `gvnfit.online` and `www.gvnfit.online`
3. In your DNS provider (wherever gvnfit.online is registered), add:

```
Type    Name    Value
A       @       76.76.21.21
CNAME   www     cname.vercel-dns.com
```

4. Vercel auto-provisions SSL. Done.

---

## Environment & Configuration

This site has no server-side environment variables. All configuration is hardcoded in `index.html`.

**Before going live, verify these values inside `index.html`:**

| Item | Current Value | Status |
|---|---|---|
| WhatsApp number | `+917200000000` | ⚠️ Replace with real number |
| WhatsForm link | `https://whatsform.com/a8wbfq` | ✅ Live |
| Instagram handle | `@fitguhay` | ✅ Confirmed |
| Email | `admin@gvnfit.online` | ✅ Confirmed |
| Slots available | `2 of 5` for Q3 2026 | Update each quarter |

To update the WhatsApp number, search for `917200000000` in `index.html` and replace with the real number in E.164 format (e.g., `919876543210`).

---

## Analytics (Optional — Recommended)

### Vercel Analytics (free with Vercel account)

Add this before `</body>` in `index.html`:

```html
<script>
window.va = window.va || function () { (window.vaq = window.vaq || []).push(arguments); };
</script>
<script defer src="/_vercel/insights/script.js"></script>
```

Then enable **Web Analytics** in your Vercel project dashboard.

### Plausible (privacy-first alternative)

```html
<script defer data-domain="gvnfit.online" src="https://plausible.io/js/script.js"></script>
```

---

## SEO Checklist

- [ ] Add `<meta name="description">` tag inside `<head>`
- [ ] Add Open Graph tags (`og:title`, `og:description`, `og:image`) for WhatsApp/LinkedIn previews
- [ ] Add a `favicon.ico` or SVG favicon
- [ ] Submit `sitemap.xml` to Google Search Console after launch
- [ ] Verify domain in Google Search Console

Basic meta tags to add in `<head>`:

```html
<meta name="description" content="Calibrate — Precision performance coaching for high-performing professionals in Chennai and Bangalore. The Calibration Protocol: DMAIC-based body recomposition for engineers, PMs, and founders.">
<meta property="og:title" content="Calibrate | Precision Performance Coaching">
<meta property="og:description" content="Built for professionals who think in systems. 1:1 coaching. Data-driven protocols. ₹25,000/month.">
<meta property="og:image" content="https://gvnfit.online/og-image.jpg">
<meta property="og:url" content="https://gvnfit.online">
<meta name="twitter:card" content="summary_large_image">
<link rel="icon" href="/favicon.svg" type="image/svg+xml">
```

---

## Maintenance

### Updating slot availability (every quarter)

Search for `2/5 slots` and `Q3 2026` in `index.html` and update the numbers and quarter.

### Updating pricing

Search for `25,000` and `65,000` in `index.html` to locate all pricing instances.

### Adding client results / testimonials

The stats band (Section after Hero) uses `data-target` attributes for the counter animation:

```html
<span class="stat-num" data-target="8.4" data-dec="1" data-suf="kg">0</span>
```

Update `data-target` values to reflect current real averages.

---

## Brand

- **Brand:** Calibrate
- **Parent Company:** Lakchinna Digitals
- **Methodology:** The Calibration Protocol (DMAIC)
- **Head Coach:** Guhayavarman
- **Instagram:** [@fitguhay](https://instagram.com/fitguhay)
- **Email:** admin@gvnfit.online
- **Domain:** gvnfit.online

---

*Built with zero dependencies. Deployed with one command. Designed to convert.*
