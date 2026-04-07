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
| — | **Jotform Premium subscription form removed** from all pages; replaced with provider-agnostic placeholder component (`components/PremiumSubscriptionForm.html`) | 3-4 Apr 2026 |
| — | **www DNS added** — `www.nfinnertyelectrical.com` redirects → apex (`nfinnertyelectrical.com`) via `.htaccess` 301 | 3-4 Apr 2026 |
| — | **Accessibility: descriptive alt text added** to all images sitewide — image inventory in `data/images.json`; `featured_image_alt` field added to all page/area content templates | 4 Apr 2026 |
| — | **SEO: `/commercial-electrician-in-york`** — title updated to *Electrician Services \| Nfinnerty Electrical*, meta description updated; "in york" copy adjustments applied | 4 Apr 2026 |
| — | **Content writers onboarded** (started 4 Apr 2026) — image alt text guidelines added to README and `data/images.json` | 4 Apr 2026 |
| — | **Content: Services page updated** — transition-word copy improvements on `/services` + clearly marked `Last updated: 2026-04-07` (`content/pages/services.md`) | 7 Apr 2026 |
| — | **Documentation consistency: “Last updated” applied across key customer pages** — homepage (`index.html`), York area page (`content/areas/york.md`), About page (`content/pages/about.md`) | 7 Apr 2026 |
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

> 📋 **Subscription form:** Paste the new provider embed into `components/PremiumSubscriptionForm.html` (see TODO comment inside the file), then update the Divi Code Module / Custom HTML block on any page that previously showed the Jotform form.

---

## 📦 Key Files

| File | Purpose |
|---|---|
| `components/PremiumSubscriptionForm.html` | Drop-in subscription form placeholder — replace TODO section with new provider embed |
| `.htaccess` | Apache rewrite rules: www → apex redirect + HTTPS enforcement + WordPress permalinks |
| `CNAME` | Custom domain for GitHub Pages (`nfinnertyelectrical.com`) |
| `data/images.json` | Image inventory — all sitewide images with descriptive alt text (accessibility reference) |

---

## 📁 Content Files

Page content, SEO metadata and shared components are version-controlled here for reference and deployment:

```
content/
  pages/
    services.md                       ← /services page — SEO title, meta description, body copy
    about.md                          ← /about page — body copy and SEO fields
    commercial-electrician-in-york.md ← /commercial-electrician-in-york — SEO title, description, body copy
  areas/
    _shared/
      testimonials.html  ← SHARED testimonials partial (used on all ~120 area pages)
    _template.md         ← Template for new area pages (includes featured_image_alt field)
    york.md              ← York area page (+ 122 other areas)
    ...
data/
  testimonials.json      ← Source-of-truth for all testimonials/reviews with links
  areas.json             ← Master list of ~120 service-area slugs and display names
  images.json            ← Image inventory — all site images with descriptive alt text
```

> **To update testimonials sitewide:** edit `data/testimonials.json` and `content/areas/_shared/testimonials.html`, then paste the updated HTML into the Divi Code module on each area page (or implement via WordPress shortcode).

> **To update image alt text:** edit `data/images.json`, then apply the updated alt text in the WordPress Media Library or Divi module for the relevant image.

---

## 🖼️ Image Alt Text Guidelines

> **Applies from: 4 April 2026** — Content writers must follow these guidelines for all images added or edited on the website.

All images on the website **must** have a descriptive `alt` attribute set. This is required for:
- **Accessibility** — screen readers rely on alt text to describe images to visually impaired users
- **SEO** — search engines use alt text to understand image content

### Rules

| Image type | Alt text rule |
|---|---|
| Informational / content images | Write a concise description of what is visible in the image (e.g. `"Electrician fitting a consumer unit in a kitchen"`) |
| Logo | Use the business name + "logo" (e.g. `"Nfinnerty Electrical logo"`) |
| Trust badges / accreditation | Name the badge (e.g. `"NICEIC Approved Contractor badge"`) |
| Decorative images (purely visual, no meaning) | Use an empty alt attribute: `alt=""` |

### Do not

- Keyword-stuff alt text (e.g. `"electrician york rewire consumer unit york north yorkshire"` ❌)
- Repeat the same alt text for different images unless they are truly identical
- Leave alt text blank on informational images

### Reference

The full image inventory with approved alt text for all known site images is in **`data/images.json`**.

For area pages, the `featured_image_alt` frontmatter field in each page's `.md` file (e.g. `content/areas/york.md`) defines the alt text for that page's featured image. The pattern is:

```
Nfinnerty Electrical electrician serving {Area Name} and the surrounding area
```

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

## 📬 Contact

**Web Technics**  
📧 yves@web-technics.services  
🌐 [web-technics.services](https://web-technics.services)
