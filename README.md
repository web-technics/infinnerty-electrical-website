# Nfinnerty Electrical — Website Project

> Powering York with a digital spark. ⚡  
> Managed by [Web Technics](https://web-technics.services) · Built on WordPress + Divi

---

## 🌐 Live Sites

| Domain | Status |
|---|---|
| [nfinnertyelectrical.com](https://nfinnertyelectrical.com) | ✅ Live (primary / canonical apex) |
| [www.nfinnertyelectrical.com](https://www.nfinnertyelectrical.com) | ↩️ Redirects → apex (301) |
| [nfinnertyelectrical.co.uk](https://nfinnertyelectrical.co.uk) | ✅ Live (VPS hosted) |

### 🔁 Domain Setup

- **Canonical domain:** `nfinnertyelectrical.com` (apex, no www)
- `www.nfinnertyelectrical.com` performs a **301 permanent redirect** to `nfinnertyelectrical.com`
- Redirect rule is defined in `.htaccess` (Apache / WordPress VPS)
- `CNAME` file set to `nfinnertyelectrical.com` for GitHub Pages compatibility
- **Required DNS records:**

  | Type | Name | Value |
  |------|------|-------|
  | A | `@` | _(server IP — set in hosting control panel)_ |
  | CNAME | `www` | `nfinnertyelectrical.com` |

---

## 📊 Current Performance (as of 30 March 2026)

| Metric | Score | Target |
|---|---|---|
| Mobile Speed | 61 / 100 | 80+ |
| SEO Score | 92 / 100 | 95+ |

---

## ✅ Completed Work

| # | Task | Date |
|---|---|---|
| [#1](https://github.com/web-technics/infinnerty-electrical-website/issues/1) | Plugin cleanup, caching enabled, images improved | 26 Mar 2026 |
| [#2](https://github.com/web-technics/infinnerty-electrical-website/issues/2) | Administration email updated | 15-17 Mar 2026 |
| [#4](https://github.com/web-technics/infinnerty-electrical-website/issues/4) | Pages/Plugins: Improved Reviews, Images, About Page | 25 Mar 2026 |
| [#5](https://github.com/web-technics/infinnerty-electrical-website/issues/5) | Homepage Title and Meta Description Updated for SEO | 16 Mar 2026 |
| [#6](https://github.com/web-technics/infinnerty-electrical-website/issues/6) | Set up nfinnertyelectrical.co.uk hosting | 15-17 Mar 2026 |
| [#8](https://github.com/web-technics/infinnerty-electrical-website/issues/8) | Google Site Kit Analytics & Search Console connected | 16 Mar 2026 |

---

## 🔧 Open Tasks

| # | Task | Priority |
|---|---|---|
| [#3](https://github.com/web-technics/infinnerty-electrical-website/issues/3) | Enable Gzip compression & browser caching in .htaccess | 🔴 High |
| [#11](https://github.com/web-technics/infinnerty-electrical-website/issues/11) | Deploy working page caching (Docket Cache drop-in) | 🔴 High |
| [#12](https://github.com/web-technics/infinnerty-electrical-website/issues/12) | Fix Google Fonts loading — switch to inline or self-hosted | 🟠 Medium |
| [#13](https://github.com/web-technics/infinnerty-electrical-website/issues/13) | Remove unused WordPress themes | 🟠 Medium |
| [#14](https://github.com/web-technics/infinnerty-electrical-website/issues/14) | Clean up image backup bloat (.bk.* files in uploads) | 🟠 Medium |
| [#15](https://github.com/web-technics/infinnerty-electrical-website/issues/15) | Set up automated live review feed (Checkatrade / Google) | 🟠 Medium |
| [#16](https://github.com/web-technics/infinnerty-electrical-website/issues/16) | SEO: Research and optimise area service landing pages | 🟡 Ongoing |
| [#17](https://github.com/web-technics/infinnerty-electrical-website/issues/17) | Review ROI on paid services (Google Ads, Checkatrade) — JotForm removed | 🟡 Ongoing |

> 💡 **Next action:** Delete `hello.php` (zero-risk cleanup) — do manually via WP Admin > Plugins.

> 📋 **Subscription form:** Paste the new provider embed into `components/PremiumSubscriptionForm.html` (see TODO comment inside the file), then update the Divi Code Module / Custom HTML block on any page that previously showed the Jotform form.

---

## 📦 Key Files

| File | Purpose |
|---|---|
| `components/PremiumSubscriptionForm.html` | Drop-in subscription form placeholder — replace TODO section with new provider embed |
| `.htaccess` | Apache rewrite rules: www → apex redirect + HTTPS enforcement + WordPress permalinks |
| `CNAME` | Custom domain for GitHub Pages (`nfinnertyelectrical.com`) |

---

## 📁 Content Files

Page content, SEO metadata and shared components are version-controlled here for reference and deployment:

```
content/
  pages/
    services.md          ← /services page — SEO title, meta description, body copy
    about.md             ← /about page — body copy and SEO fields
  areas/
    _shared/
      testimonials.html  ← SHARED testimonials partial (used on all ~120 area pages)
    _template.md         ← Template for new area pages
    york.md              ← York area page (+ 122 other areas)
    ...
data/
  testimonials.json      ← Source-of-truth for all testimonials/reviews with links
  areas.json             ← Master list of ~120 service-area slugs and display names
```

> **To update testimonials sitewide:** edit `data/testimonials.json` and `content/areas/_shared/testimonials.html`, then paste the updated HTML into the Divi Code module on each area page (or implement via WordPress shortcode).

---

## 📁 Content Files

Page content, SEO metadata and shared components are version-controlled here for reference and deployment:

```
content/
  pages/
    services.md          ← /services page — SEO title, meta description, body copy
    about.md             ← /about page — body copy and SEO fields
  areas/
    _shared/
      testimonials.html  ← SHARED testimonials partial (used on all ~120 area pages)
    _template.md         ← Template for new area pages
    york.md              ← York area page (+ 122 other areas)
    ...
data/
  testimonials.json      ← Source-of-truth for all testimonials/reviews with links
  areas.json             ← Master list of ~120 service-area slugs and display names
```

> **To update testimonials sitewide:** edit `data/testimonials.json` and `content/areas/_shared/testimonials.html`, then paste the updated HTML into the Divi Code module on each area page (or implement via WordPress shortcode).

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| WordPress + Divi | CMS & page builder |
| Yoast SEO | On-page SEO management |
| Google Site Kit | Analytics & Search Console integration |
| Really Simple SSL | SSL/HTTPS management |
| WebP images | Image optimisation |
| VPS (web-technics) | Hosting for .co.uk domain |
| GitHub | Version control & project tracking |

---

## 🔐 Credentials & Access

All admin logins, hosting credentials and sensitive project documents are stored securely in Google Drive (access restricted):  
🔗 [Project Google Drive Folder](https://drive.google.com/drive/u/0/folders/1f3_U9Y-28DZicj2vcAgzB1LRcFEzbm0M)

> ⚠️ Never commit passwords or credentials to this repository.

---

## 📬 Contact

**Web Technics**  
📧 yves@web-technics.services  
🌐 [web-technics.services](https://web-technics.services)