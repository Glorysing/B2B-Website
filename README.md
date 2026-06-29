# B2B Cosmetic Manufacturer Websites

**Two production B2B websites built from scratch — custom WordPress themes, zero page builders.**

<div align="center">

[![JSY Live](https://img.shields.io/website?url=https%3A%2F%2Fjsybiotech.com&label=jsybiotech.com&up_message=online&down_message=offline&color=267A6D)](https://jsybiotech.com)
[![Nantong Live](https://img.shields.io/website?url=https%3A%2F%2Fnantong-plastic.com&label=nantong-plastic.com&up_message=online&down_message=offline&color=1A5A8A)](https://nantong-plastic.com)
[![WordPress](https://img.shields.io/badge/CMS-WordPress_6.9+-21759B?logo=wordpress&logoColor=white)](https://wordpress.org)
[![PHP](https://img.shields.io/badge/PHP-8.x-777BB4?logo=php&logoColor=white)](https://php.net)
[![Bilingual](https://img.shields.io/badge/Languages-ZH_%2F_EN-4caf50)](https://jsybiotech.com/en/)
[![Vibe Coding](https://img.shields.io/badge/Built_with-Vibe_Coding-FF6B35?logo=anthropic&logoColor=white)](https://www.anthropic.com)

</div>

---

Two independent corporate websites for Chinese B2B cosmetic manufacturers — each built on its own hand-written WordPress theme from scratch, covering bilingual product showcasing, SEO targeting 20+ export markets, and online inquiry workflows. No shared templates, no page builders, no plugin dependencies beyond WordPress core.

Built end-to-end using **Vibe Coding** — Claude AI as a full-time pair programming partner across product design, architecture decisions, and line-by-line implementation. A workflow that lets one developer ship production-grade full-stack work at team scale.

---

## Projects at a Glance

|  | [JSY Biotech](https://jsybiotech.com) | [Nantong Technology](https://nantong-plastic.com) |
|:---|:---|:---|
| **Full Name** | Guangzhou Jinshengye Biotechnology Co., Ltd. | Guangdong Nantong Technology Co., Ltd. |
| **Industry** | Cosmetics OEM / ODM Filling | Cosmetic Pump Dispenser Manufacturing |
| **Theme** | `jsy-biotech` | `pump-nantong` |
| **SEO Engine** | Fully custom `inc/seo.php` | AIOSEO + custom hreflang layer |
| **Product System** | Custom Post Type (`jsy_product`) | 119+ SKUs with full spec fields |
| **Deploy** | SSH direct upload | GitHub Actions → SFTP |
| **Languages** | EN / ZH (Polylang directory) | EN / ZH (Polylang directory) |
| **Certifications** | GMPC · ISO · FDA | ISO · SGS |

---

## JSY Biotech · [jsybiotech.com](https://jsybiotech.com)

<div align="center">

[![JSY](https://img.shields.io/badge/JSY_ENTERPRISE-jsybiotech.com-267A6D?style=for-the-badge)](https://jsybiotech.com)

</div>

Guangzhou Jinshengye Biotechnology Co., Ltd. is a cosmetics OEM/ODM contract manufacturer in Guangzhou targeting global beauty brands. The site is built as a **service-first B2B showcase** — there are no product SKUs to browse, only formulation categories and a capabilities-driven inquiry flow.

### Company at a Glance

| | |
|:---|:---|
| Experience | 15+ years |
| Factory Area | 10,800+ m² |
| Production Lines | 8 standard lines |
| Proven Formulas | 2,000+ |
| Brand Partners | 1,000+ |
| Certifications | GMPC · ISO · FDA |
| Ingredient Suppliers | Dow · Givaudan · BASF · CRODA |

### Product Categories

```
Cosmetics OEM / ODM
├── Facial Skincare       Serums, moisturizers, essences, eye care
├── Personal Care         Body lotion, cleanser, deodorant
├── Color Cosmetics       Foundation, lip, eye makeup
├── Hair Care             Shampoo, conditioner, hair treatment
└── Aroma & Essential     Essential oils, fragrance, aromatherapy
```

### Features

| Feature | Description |
|:---|:---|
| **Video Hero Carousel** | Full-screen 3-slide hero with looping background video + text overlay; slide content editable from WP settings panel |
| **Custom Product CPT** | `jsy_product` post type with `jsy_series` taxonomy (5 slugs: `facial` / `personal` / `color` / `hair` / `aroma`) |
| **Sticky Category Filter** | Products page: left sticky sidebar with category nav + count badges; JS filter + URL hash sync |
| **Custom SEO Engine** | `inc/seo.php` owns all 11 pages — title, description, canonical, hreflang, OG, Twitter Card, JSON-LD schema |
| **Auto Language Redirect** | `navigator.language` detection → ZH or EN with 30-day cookie; language switcher writes same cookie |
| **Bilingual Translation** | Custom `languages/translations.php` lookup table; `jsy_t()` / `jsy_et()` helpers — no gettext overhead |
| **Brand & Supplier Tickers** | Animated marquee of 18 partner brand logos + 16 ingredient supplier logos |
| **Schema.org** | Organization (global) · FAQPage (`/faq/`) · HowTo (`/process/`) · ContactPage (`/contact/`) |
| **WP Settings Panel** | Custom settings page to update hero slides, stats figures, and other editable copy without touching code |

### Design System

| Token | Value | Usage |
|:---|:---|:---|
| Primary | `#267A6D` | Buttons, links, icons |
| Deep | `#1A5548` | Inner page hero backgrounds |
| Hover | `#3AA697` | Interactive hover states |
| Gold Accent | `#B8965A` | Eyebrow lines, decorative accents |
| Background | `#FAFAF8` | Main page background (warm off-white) |
| Alt Background | `#F5F0E8` | Alternating section backgrounds |
| Heading | Cormorant Garamond 300 | Editorial serif, EN headings |
| Body | DM Sans | EN body copy |
| Chinese | Noto Serif SC / Noto Sans SC | ZH headings / body |

### Site Map

| Path | Page | Schema |
|:---|:---|:---|
| `/` · `/en/` | Homepage — video hero / stats / services / categories / factory / certs / brand tickers | Organization |
| `/about/` | About — history, culture, R&D capability, team | Organization |
| `/services/` | OEM / ODM / Custom Formulation / Semi-finished supply | — |
| `/products/` | Product center — 5 categories, sticky sidebar filter | — |
| `/process/` | Step-by-step cooperation workflow | HowTo |
| `/quality/` | QC center + lab + inspection process | — |
| `/certifications/` | GMPC · ISO · FDA · NMPA certificates | — |
| `/cases/` | Cooperation cases & client references | — |
| `/faq/` | Frequently asked questions | FAQPage |
| `/contact/` | Inquiry form — primary conversion page | ContactPage |
| `/news/` | Industry insights & updates | — |

### Tech Stack

| Layer | Technology |
|:---|:---|
| CMS | WordPress 6.9+ |
| Theme | Custom PHP (`jsy-biotech`) — handwritten, zero page builder |
| Routing | `inc/router.php` — virtual router at `template_redirect` priority 1 (fires before Polylang canonical) |
| Localization | Polylang — URL directory mode; `jsy_lang()` · `jsy_url()` · `jsy_t()` helpers |
| Frontend | Vanilla HTML5 · CSS3 custom properties · Vanilla JS |
| Fonts | Cormorant Garamond · DM Sans · Noto Serif SC · Noto Sans SC (Google Fonts) |
| SEO | Fully custom `inc/seo.php` — suppresses AIOSEO on all theme-owned pages |
| Cache | LiteSpeed + Cloudflare WAF |
| Deploy | SSH direct per-file upload + `wc -c` size verification |

---

## Nantong Technology · [nantong-plastic.com](https://nantong-plastic.com)

<div align="center">

[![Nantong](https://img.shields.io/badge/NANTONG_TECHNOLOGY-nantong--plastic.com-1A5A8A?style=for-the-badge)](https://nantong-plastic.com)
[![Deploy](https://img.shields.io/badge/Deploy-GitHub_Actions-2088FF?logo=github-actions&logoColor=white)](https://github.com/features/actions)

</div>

Guangdong Nantong Technology Co., Ltd. is a precision cosmetic pump dispenser manufacturer established in 2010, serving global personal care brands with OEM/ODM pump solutions across 20+ export markets, including North America, Europe, the Middle East, Southeast Asia, Japan, and Korea.

### Company at a Glance

| | |
|:---|:---|
| Founded | 2010 |
| Industry Experience | 15+ years |
| Injection Machines | 80+ units |
| Factory Area | 10,000+ m² |
| Monthly Output | 20M+ units |
| Export Markets | 20+ countries |
| Key Clients | P&G · Unilever · Kao · Liby · Chando |

### Product Lines

```
Cosmetic Pump Packaging
├── Foam Pump Series       38/410 · 43/410 neck — 0.4–2cc output volume
├── Lotion Pump Series     Precision metered dispensing for lotions, serums, body care
└── Airless Bottle Series  30ml / 50ml / 75ml — contamination-free delivery
```

### Features

| Feature | Description |
|:---|:---|
| **Product Database** | 119+ SKUs with neck size, output volume, material, MOQ, and lead time |
| **Smart Inquiry Form** | Auto-fills product name + specs when opened from a product page; supports up to 10 file attachments |
| **Product Detail Pages** | Fully server-side rendered — virtual routes under `/products/{sku}/` without individual WP pages |
| **Global Footprint Map** | Visual map highlighting 20+ export countries |
| **Client Brand Wall** | Reference logos: P&G, Unilever, Kao, and other household-name clients |
| **Certifications Page** | ISO, SGS, and product patent certificates |
| **News Section** | Industry insights and company updates |
| **Bilingual** | Full EN/ZH translation table; `ntp_t()` / `ntp_et()` helpers |

### Site Map

| Path | Page |
|:---|:---|
| `/` · `/en/` | Homepage |
| `/products/` | Full product catalog |
| `/products/foam-pumps/` | Foam pump category |
| `/products/lotion-pumps/` | Lotion pump category |
| `/products/cosmetic-packaging/` | Cosmetic packaging category |
| `/products/{sku}/` | Individual product detail pages (virtual route) |
| `/about/` | About us |
| `/service/` · `/custom-service/` | Standard / custom services |
| `/quality-control/` | QC process |
| `/certifications/` | Certifications |
| `/contact/` | Contact / RFQ form |
| `/news/` | News |
| `/stores/` | Alibaba · Made-in-China marketplaces |

### Tech Stack

| Layer | Technology |
|:---|:---|
| CMS | WordPress 6.9+ |
| Theme | Custom PHP (`pump-nantong`) — handwritten, zero page builder |
| Routing | `inc/router.php` — virtual router at `template_redirect` priority 1 |
| Localization | Polylang — URL directory mode; `ntp_lang()` · `ntp_url()` · `ntp_t()` helpers |
| Frontend | Vanilla HTML5 · CSS3 · Vanilla JS |
| Fonts | Google Fonts: Inter · Syne |
| SEO | AIOSEO (WP admin) + custom `inc/seo.php` for virtual routes (products / news) |
| Cache | LiteSpeed + Cloudflare WAF |
| Deploy | GitHub Actions → SFTP (checksum-based — uploads changed files only) |

---

## Shared Architecture

Both themes are built independently but follow the same structural conventions.

```
theme/
├── functions.php            Core: translation helpers, CPT/taxonomy, enqueue, settings
├── header.php               Responsive bilingual nav — scroll-aware header
├── footer.php               Footer with contact, social, language switcher
├── front-page.php           Homepage template
├── inc/
│   ├── router.php           Virtual URL router (priority 1 — before Polylang canonical)
│   ├── components.php       Shared UI: page banners, inquiry form, CTA strip
│   ├── seo.php              SEO engine: hreflang, canonical, OG, JSON-LD
│   └── data.php             Static data arrays (FAQ, etc.)
├── page-templates/          Per-route templates included by router.php
│   ├── products.php
│   ├── product-detail.php
│   ├── category.php
│   ├── about.php
│   ├── service.php  ·  custom-service.php
│   ├── contact.php
│   ├── quality-control.php
│   ├── certifications.php
│   ├── news.php  ·  news-detail.php
│   └── faq.php  (JSY only)
├── languages/
│   └── translations.php     Bilingual lookup table (ZH / EN key-value pairs)
└── assets/
    ├── css/main.css         Single stylesheet with CSS custom properties
    └── js/main.js           Single script file
```

### Key Engineering Patterns

**Virtual Routing** — Both themes intercept WordPress's template resolution at `template_redirect` (priority 1, before Polylang's canonical redirect at priority 2). This enables clean URL structures like `/products/foam-pumps/` and `/news/{slug}/` served from `page-templates/` files without creating a WP page record per URL. After interception, `$wp_query->is_404 = false` and `$wp_query->is_page = true` are set manually to keep title/body-class rendering correct.

**LiteSpeed JS Defer** — LiteSpeed converts all enqueued scripts to `type="litespeed/javascript"`, deferring execution until the first user interaction. Event listeners that must bind before any interaction (scroll-aware header, auto-init behaviours) use `data-no-optimize="1"` inline scripts injected at `wp_footer` priority 1 — bypassing LiteSpeed's bundler entirely.

**Bilingual without gettext** — Translation is handled by a custom `translations.php` lookup table with typed helpers (`jsy_t()` / `ntp_t()`), bypassing `.po`/`.mo` compilation while covering every string on the site.

**SEO without plugin lock-in** — JSY's `inc/seo.php` takes full ownership of all 11 pages: it suppresses AIOSEO on every theme-controlled route and outputs title, description, canonical, hreflang, OG, Twitter Card, and JSON-LD from a single function. Nantong uses AIOSEO for static WP pages but mirrors the same custom layer for virtual product and news routes.

---

### About Vibe Coding

Both sites were built entirely through **Vibe Coding** — using Claude AI as a continuous pair programming partner from day one. Not code generation followed by manual editing, but a genuine collaborative loop: Claude holds deep context of the codebase across sessions, weighs technical trade-offs, flags edge cases before they hit production, and iterates on real problems as they emerge.

This approach makes it practical for a single developer to deliver what would typically require a full team: a custom CMS theme architecture, international SEO infrastructure, bilingual routing, CI/CD automation, and ongoing feature work — across two independent production sites simultaneously.

---

<div align="center">

*© 2025 · Built by Glory with Vibe Coding · All Rights Reserved*

</div>
