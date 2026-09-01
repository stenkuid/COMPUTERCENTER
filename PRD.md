# PRD — Website #5: Computer Center

### PC Parts, Accessories & Custom PC Assembly

**Platform:** Astro + Cloudflare  
**Project Type:** Local Computer Retail & Service Website  
**Status:** PRD v1.0  

---

# 1. Product Overview

**Computer Center** adalah perusahaan yang bergerak di bidang komputer dengan fokus pada:

* Sparepart PC.
* Accessory PC.
* Komponen untuk rakit PC.
* Jasa rakit PC.
* Konsultasi kebutuhan PC.

Website Computer Center berfungsi sebagai **digital catalog + lead generation website**.

Website tidak perlu menjadi marketplace atau e-commerce penuh pada tahap pertama.

Fokus utama:

> **Bantu pelanggan memilih komponen yang tepat dan membuat PC yang sesuai kebutuhan mereka.**

---

# 2. Business Goal

## Primary Goal

Meningkatkan penjualan produk PC parts/accessories dan mendapatkan pelanggan jasa rakit PC.

## Secondary Goals

* Menampilkan katalog produk.
* Membantu pelanggan menemukan komponen.
* Membangun kepercayaan.
* Mempromosikan jasa rakit PC.
* Mendapatkan inquiry melalui WhatsApp.
* Mendorong pelanggan datang ke toko.
* Mendukung Local SEO.

---

# 3. Target Customer

## Primary

### PC Builder

Orang yang ingin merakit PC sendiri.

### Beginner

Orang yang belum memahami komponen komputer dan membutuhkan bantuan.

### Gamer

Mencari komponen untuk gaming.

### Content Creator

Membutuhkan PC untuk editing, rendering, dan produksi konten.

### Student / Office User

Membutuhkan PC untuk belajar dan pekerjaan.

---

# 4. Customer Problems

Pelanggan sering menghadapi:

* Bingung memilih komponen.
* Takut salah kompatibilitas.
* Tidak tahu spesifikasi yang dibutuhkan.
* Tidak tahu budget ideal.
* Takut membeli komponen yang tidak cocok.
* Tidak bisa merakit sendiri.
* Tidak yakin toko dapat membantu setelah pembelian.

Website harus memposisikan Computer Center sebagai:

> **Tempat bertanya sebelum membeli.**

---

# 5. Brand Positioning

### Positioning

> **Computer Center — Build the PC that fits you.**

Bukan sekadar toko komputer.

Computer Center harus terasa seperti:

**Retailer + PC advisor + PC builder.**

---

# 6. Brand Personality

* Technical.
* Helpful.
* Reliable.
* Modern.
* Straightforward.
* Friendly.

Tone:

**Teknis tetapi mudah dipahami.**

Hindari bahasa yang terlalu jargon-heavy.

---

# 7. Unique Selling Proposition

### Component Selection

Pelanggan dapat memilih berbagai komponen PC.

### PC Assembly

Computer Center membantu merakit PC.

### Compatibility Guidance

Pelanggan dapat meminta bantuan menentukan komponen yang kompatibel.

### Local Support

Pelanggan dapat datang langsung atau menghubungi toko.

---

# 8. Website Objective

Dalam beberapa detik pengguna harus mengetahui:

1. Computer Center menjual PC parts.
2. Bisa rakit PC.
3. Bisa membantu memilih komponen.
4. Produk apa yang tersedia.
5. Bagaimana cara order.
6. Di mana lokasinya.

Primary CTA:

**Build Your PC**

Secondary:

**Browse Components**

---

# 9. Architecture Decision

## Recommended

**Astro Static + Cloudflare Pages**

Website versi pertama tidak membutuhkan database.

Produk disimpan sebagai static data.

Contoh:

```text
products.ts
```

Jika jumlah produk menjadi sangat banyak atau inventory harus real-time, architecture dapat berkembang.

---

# 10. Technology Stack

* Astro.
* TypeScript.
* Native CSS.
* Minimal JavaScript.
* Cloudflare Pages.

Optional:

* Cloudflare Web Analytics.
* Cloudflare R2/Images.

Tidak menggunakan:

* Full e-commerce framework.
* Heavy product filtering library.
* Complex shopping cart.
* Authentication.
* Database pada Phase 1.

---

# 11. Sitemap

```text
/
├── /products
├── /products/[slug]
├── /pc-build
├── /services
├── /about
├── /location
├── /contact
├── /faq
├── /robots.txt
└── /sitemap-index.xml
```

---

# 12. Homepage Structure

1. Navbar.
2. Hero.
3. Product Categories.
4. Featured Components.
5. PC Build Service.
6. Build by Budget.
7. Why Computer Center.
8. Compatibility Guidance.
9. Customer Builds.
10. Location.
11. FAQ.
12. Final CTA.
13. Footer.

---

# 13. Navbar

Logo:

**COMPUTER CENTER**

Navigation:

* Products.
* PC Build.
* Services.
* About.
* Location.

CTA:

**Build Your PC**

Mobile menggunakan hamburger navigation.

---

# 14. Hero

### Headline

> **Build Your PC. Your Way.**

Supporting copy:

> Komponen PC, accessories, dan jasa rakit untuk membantu kamu membangun PC yang sesuai kebutuhan dan budget.

CTA:

**Start Your Build**

Secondary:

**Browse Components**

Visual:

* Modern gaming/workstation PC.
* Component close-ups.
* CPU/GPU/motherboard details.
* Clean technical composition.

---

# 15. Design Direction

## Concept

**Modern PC Workshop × Premium Tech Retail**

Visual harus terasa:

* Technical.
* Precise.
* Clean.
* Confident.
* Modern.

Tidak menggunakan cyberpunk berlebihan.

Avoid:

* Neon everywhere.
* Excessive RGB.
* Gaming clichés.
* Excessive glow.
* Heavy 3D animations.

---

# 16. Suggested Color Palette

### Deep Black

`#0B0D10`

### Graphite

`#171A1F`

### Electric Blue

`#3B82F6`

### Cyan

`#22D3EE`

### White

`#F8FAFC`

### Gray

`#94A3B8`

Dark theme dapat digunakan sebagai primary visual direction.

Accent blue digunakan untuk CTA.

---

# 17. Typography

Heading:

* Bold.
* Technical.
* Strong.

Body:

* Modern sans-serif.
* Excellent readability.

Optional:

Monospace hanya untuk specification/data visual.

Maksimal 2–3 font family, tetapi idealnya tetap 2.

---

# 18. Product Categories

Headline:

> **Everything You Need to Build**

Kategori:

### Processor

CPU.

### Graphics Card

GPU.

### Motherboard

Motherboard.

### RAM

Memory.

### Storage

SSD/HDD.

### Power Supply

PSU.

### Cooling

CPU cooler/fan.

### Case

PC case.

### Accessories

Keyboard, mouse, cable, adapter, etc.

Kategori final mengikuti inventory aktual.

---

# 19. Product Card

Setiap product card:

* Image.
* Brand.
* Product name.
* Category.
* Key specification.
* Price jika tersedia.
* Availability jika tersedia.
* CTA.

CTA:

**View Product**

Jika product tersedia untuk pembelian:

**Ask About This**

Tidak menampilkan inventory real-time jika data tidak real-time.

---

# 20. Product Detail

Route:

`/products/[slug]`

Structure:

1. Breadcrumb.
2. Product image.
3. Product name.
4. Brand.
5. Short description.
6. Price.
7. Availability.
8. Specifications.
9. Compatibility notes.
10. CTA.
11. Related components.

---

# 21. Product Specification

Contoh:

| Specification | Value   |
| ------------- | ------- |
| Brand         | Example |
| Model         | Example |
| Socket        | AM5     |
| Memory        | DDR5    |
| Power         | XX W    |
| Interface     | PCIe    |
| Warranty      | X Years |

Semua data harus berasal dari produk aktual.

---

# 22. Compatibility Section

Ini menjadi fitur edukasi utama.

Headline:

> **Not Sure If Your Parts Match?**

Copy:

> Komponen PC harus saling kompatibel. Kalau kamu belum yakin, tanyakan kepada Computer Center sebelum membeli.

CTA:

**Ask Our Team**

Tidak perlu membuat compatibility engine pada Phase 1.

---

# 23. PC Build Service

Section utama:

> **Don't Want to Build It Yourself?**

Copy:

> Pilih komponen yang kamu butuhkan. Kami bantu merakitnya menjadi PC yang siap digunakan.

CTA:

**Request a Build**

Service dapat mencakup:

* Component consultation.
* Assembly.
* Cable management.
* Basic testing.

Hanya tampilkan layanan yang benar-benar tersedia.

---

# 24. Build by Budget

Section:

> **Start With Your Budget**

Contoh kategori:

### Entry

Untuk kebutuhan basic.

### Work

Untuk produktivitas.

### Gaming

Untuk gaming.

### Creator

Untuk editing/rendering.

### High Performance

Untuk workload berat.

Budget aktual jangan dibuat tanpa data.

Gunakan placeholder sampai pricing tersedia.

---

# 25. Build Recommendation

Setiap build card:

* Target use.
* Budget range.
* CPU.
* GPU.
* RAM.
* Storage.
* PSU.
* Estimated performance.
* CTA.

CTA:

**Customize This Build**

Phase 1 dapat berupa static recommendation.

Tidak perlu configurator interaktif.

---

# 26. Why Computer Center

Headline:

> **More Than Just Parts.**

Benefit:

### Helpful Advice

Bantu pelanggan memahami pilihan komponen.

### Build Service

PC dapat dirakit oleh tim.

### Component Variety

Berbagai kategori komponen.

### Local Support

Pelanggan dapat datang langsung.

---

# 27. Customer Builds

Tampilkan contoh PC yang pernah dibuat.

Format:

* Build image.
* Build name.
* Use case.
* Main specs.
* Budget range jika boleh dipublikasikan.

Contoh:

**Creator Build**

Ryzen / Core CPU
RTX GPU
32GB RAM
1TB SSD

Data harus berasal dari build nyata atau diberi label sebagai contoh.

---

# 28. Service Section

Services:

### PC Assembly

Rakit PC berdasarkan komponen pelanggan.

### PC Consultation

Bantu memilih komponen.

### Upgrade

Jika tersedia.

### Troubleshooting

Jika tersedia.

### Cleaning

Jika tersedia.

Jangan menambahkan service yang belum disediakan.

---

# 29. Location

Headline:

> **Come Build With Us.**

Tampilkan:

* Address.
* Opening hours.
* Phone.
* WhatsApp.
* Google Maps.

CTA:

**Get Directions**

---

# 30. Contact / Inquiry

Headline:

> **Have a Build in Mind?**

Copy:

> Kirim kebutuhan dan budget kamu. Tim Computer Center akan membantu menentukan komponen yang sesuai.

CTA:

**Chat With Computer Center**

---

# 31. WhatsApp Inquiry Flow

Pre-filled message:

> Halo Computer Center, saya ingin konsultasi rakit PC.

Optional:

> Budget saya sekitar Rp [budget]. PC akan digunakan untuk [kebutuhan].

Jangan meminta data pribadi yang tidak diperlukan.

---

# 32. FAQ

### Apakah Computer Center menyediakan jasa rakit PC?

Jawab berdasarkan service aktual.

### Apakah bisa membawa komponen sendiri?

Tentukan berdasarkan kebijakan toko.

### Bisa konsultasi sebelum membeli?

Ya, jika layanan tersedia.

### Apakah semua komponen kompatibel?

Tidak. Komponen harus dipilih berdasarkan compatibility.

### Apakah ada garansi?

Jelaskan sesuai brand/product warranty.

### Apakah bisa upgrade PC lama?

Jawab berdasarkan layanan aktual.

---

# 33. SEO Strategy

Keyword:

* toko komputer [kota].
* toko PC [kota].
* sparepart PC [kota].
* PC parts [kota].
* rakit PC [kota].
* jasa rakit PC [kota].
* komponen komputer [kota].
* accessories PC [kota].

---

# 34. Metadata

Homepage:

**Computer Center — PC Parts & Custom PC Build**

Local:

**Computer Center — Toko Komputer & Jasa Rakit PC [City]**

Description:

> Temukan PC parts, accessories, dan jasa rakit PC di Computer Center. Konsultasikan kebutuhan dan budget PC kamu bersama tim kami.

---

# 35. Structured Data

Homepage:

**Organization / LocalBusiness**

Product detail:

**Product**

Service pages:

**Service**

Jika price/availability tersedia secara akurat, dapat dimasukkan ke structured data.

---

# 36. Product SEO

Setiap product page memiliki:

* Unique title.
* Meta description.
* Canonical.
* Product schema.
* OG image.
* Product image alt.
* Specification content.

---

# 37. Image Strategy

Priority:

1. Hero PC.
2. Component photography.
3. PC builds.
4. Product detail.
5. Store/workshop.
6. Team assembling PC.

Image format:

* AVIF/WebP.
* Responsive.
* Proper dimensions.
* Lazy load non-critical.

---

# 38. Mobile UX

Mobile priority:

* Search/browse products.
* Category navigation.
* Product details.
* WhatsApp CTA.
* Build service.

Product cards harus tetap readable.

Technical specifications dapat menggunakan collapsible sections pada mobile.

---

# 39. Product Discovery

Jika jumlah produk sedikit:

Gunakan category cards.

Jika jumlah produk besar:

Implementasikan lightweight filtering:

* Category.
* Brand.
* Use case.

Jangan memasang search/filter framework besar hanya untuk kebutuhan sederhana.

---

# 40. Animation

Minimal.

Allowed:

* Hover.
* Image transitions.
* Button states.
* Small product reveal.

Avoid:

* Constant RGB animations.
* Heavy 3D.
* WebGL.
* Video backgrounds.
* Excessive glowing effects.

---

# 41. Accessibility

Requirements:

* Semantic HTML.
* Keyboard navigation.
* Focus states.
* Proper contrast.
* Alt text.
* Accessible product cards.
* Accessible mobile navigation.

Dark theme harus tetap memiliki contrast tinggi.

---

# 42. Performance

Target:

* Performance ≥90.
* SEO ≥95.
* Accessibility ≥90.

Core Web Vitals:

* LCP ≤2.5s.
* CLS ≤0.1.
* INP ≤200ms.

Product images harus dioptimalkan.

---

# 43. Cloudflare Architecture

```text
Astro
 ↓
Static Build
 ↓
Cloudflare Pages
```

Tidak menggunakan database Phase 1.

Tidak menggunakan Worker runtime untuk halaman statis.

---

# 44. Bundle Policy

Mandatory:

* Minimal JS.
* No heavy UI framework.
* No unnecessary product libraries.
* No large animation packages.
* No client state management unless required.
* Remove unused dependencies.

Production build harus dianalisis sebelum deployment.

Jika Worker digunakan di masa depan, compressed server bundle harus tetap berada di bawah batas Cloudflare deployment yang ditargetkan.

---

# 45. Recommended Project Structure

```text
src/
├── components/
│   ├── Navbar.astro
│   ├── Button.astro
│   ├── ProductCard.astro
│   ├── ProductSpecTable.astro
│   ├── CategoryCard.astro
│   ├── BuildCard.astro
│   ├── ServiceCard.astro
│   └── Footer.astro
│
├── sections/
│   ├── Hero.astro
│   ├── ProductCategories.astro
│   ├── FeaturedProducts.astro
│   ├── PCBuildService.astro
│   ├── BuildByBudget.astro
│   ├── WhyComputerCenter.astro
│   ├── Compatibility.astro
│   ├── CustomerBuilds.astro
│   ├── Services.astro
│   ├── Location.astro
│   ├── FAQ.astro
│   └── FinalCTA.astro
│
├── layouts/
│   └── BaseLayout.astro
│
├── pages/
│   ├── index.astro
│   ├── products/
│   │   ├── index.astro
│   │   └── [slug].astro
│   ├── pc-build.astro
│   ├── services.astro
│   ├── about.astro
│   ├── location.astro
│   ├── contact.astro
│   ├── faq.astro
│   ├── robots.txt.ts
│   └── sitemap-index.xml.ts
│
├── data/
│   ├── business.ts
│   ├── products.ts
│   ├── builds.ts
│   ├── services.ts
│   └── faq.ts
│
├── styles/
│   └── global.css
│
└── assets/
```

---

# 46. Data Architecture

### Product

```text
product
├── slug
├── brand
├── name
├── category
├── description
├── price
├── availability
├── images
├── specifications
├── compatibility
└── featured
```

### Build

```text
build
├── slug
├── name
├── useCase
├── budget
├── components
├── image
└── featured
```

### Service

```text
service
├── slug
├── name
├── description
├── price
├── turnaround
└── available
```

---

# 47. Analytics

Cloudflare Web Analytics.

Track:

```text
view_product
click_product
click_build
click_build_service
click_whatsapp
click_direction
```

Primary conversion:

**WhatsApp inquiry**

Secondary:

**Build service inquiry**

---

# 48. Security

Static website tidak menyimpan customer data.

Jika inquiry form ditambahkan:

* Input validation.
* Rate limiting.
* Spam protection.
* Cloudflare Turnstile bila diperlukan.

Tidak membutuhkan database pada Phase 1.

---

# 49. Out of Scope

Tidak termasuk:

* Shopping cart.
* Online payment.
* User account.
* Inventory management.
* Real-time stock.
* Automated compatibility engine.
* Admin dashboard.
* Customer dashboard.
* Order tracking.
* Dealer portal.
* Database.

---

# 50. Future Expansion

## Phase 2

* Online catalog.
* Build request form.
* Product comparison.
* Compatibility assistant.
* Stock status.

## Phase 3

Jika inventory/order sudah kompleks:

* Cloudflare Workers.
* D1.
* R2.
* Admin dashboard.
* Order management.

---

# 51. Acceptance Criteria

## Brand

* [ ] Computer Center terlihat professional.
* [ ] Visual technical tetapi approachable.
* [ ] Tidak terlihat seperti generic gaming website.

## Product

* [ ] Product categories mudah ditemukan.
* [ ] Product details jelas.
* [ ] Specifications readable.
* [ ] CTA inquiry jelas.

## PC Build

* [ ] Jasa rakit terlihat prominent.
* [ ] Build recommendations tersedia.
* [ ] Customer dapat menghubungi tim.

## UX

* [ ] Mobile-first.
* [ ] Product discovery cepat.
* [ ] WhatsApp CTA mudah ditemukan.
* [ ] Location mudah diakses.

## SEO

* [ ] LocalBusiness schema.
* [ ] Product schema.
* [ ] Service schema.
* [ ] Metadata.
* [ ] Canonical.
* [ ] Sitemap.
* [ ] Robots.
* [ ] Open Graph.

## Performance

* [ ] Performance ≥90.
* [ ] SEO ≥95.
* [ ] Accessibility ≥90.
* [ ] Images optimized.
* [ ] Minimal JS.

## Technical

* [ ] Astro production build berhasil.
* [ ] Cloudflare Pages compatible.
* [ ] No unnecessary dependencies.
* [ ] No broken links.
* [ ] No console errors.

---

# 52. Implementation Blueprint

## Website Goal

Membangun website Computer Center sebagai **digital catalog + PC consultation funnel**.

Core journey:

**Discover Parts → Understand Options → Choose Build → Ask Team → Visit/Buy**

## Architecture

**Astro Static + Cloudflare Pages**

## Sitemap

```text
/
├── /products
├── /products/[slug]
├── /pc-build
├── /services
├── /about
├── /location
├── /contact
├── /faq
├── /robots.txt
└── /sitemap-index.xml
```

## Design Direction

**Modern PC Workshop × Premium Tech Retail**

## Core Components

* Navbar.
* Hero.
* Product Category.
* Product Card.
* Product Specification.
* Build Card.
* Service Card.
* Compatibility section.
* Customer Builds.
* Location.
* FAQ.
* CTA.
* Footer.

## Technical Requirements

* Astro.
* TypeScript.
* Static generation.
* Data-driven products.
* Data-driven builds.
* Minimal JS.
* Responsive images.
* Product SEO.
* Local SEO.
* Structured data.
* Cloudflare Pages.

---

# 53. Antigravity Execution Plan

## Prompt 1 — Analysis

> You are a senior full-stack engineer. Analyze the Computer Center website PRD before coding. Determine the Astro static architecture, product data model, build recommendation data model, reusable components, SEO structure, image strategy, responsive behavior, and implementation checklist. Do not invent e-commerce, inventory, authentication, or backend functionality.

Output:

* Architecture.
* Component plan.
* Product model.
* Build model.
* SEO plan.
* Implementation checklist.

---

## Prompt 2 — Build

> You are a senior full-stack engineer. Build the Computer Center website according to the provided PRD. Use Astro static generation, reusable components, data-driven product and PC build content, semantic HTML, optimized responsive images, minimal client-side JavaScript, and Cloudflare Pages compatibility. The visual style should feel like a premium modern PC workshop rather than a generic gaming website. Do not add unnecessary dependencies or features.

Implement:

* Homepage.
* Product catalog.
* Product detail.
* PC build service.
* Build recommendations.
* Services.
* About.
* Location.
* FAQ.
* Contact.
* Product SEO.
* Local SEO.
* Structured data.

---

## Prompt 3 — Optimization

> You are a senior full-stack engineer preparing the Computer Center website for production. Audit and optimize the project for build reliability, performance, accessibility, SEO, responsive behavior, image delivery, JavaScript payload, dependency size, broken links, and Cloudflare Pages compatibility. Fix issues without changing requirements or adding unnecessary architecture.

Check:

### Build

* Production build.
* Type checking.
* Broken links.
* Console errors.

### Product

* Product data.
* Product detail routes.
* Specification rendering.
* Image loading.

### Performance

* LCP.
* CLS.
* INP.
* JS payload.
* CSS payload.
* Bundle size.

### SEO

* Metadata.
* Canonical.
* Product schema.
* LocalBusiness schema.
* Sitemap.
* Robots.
* Open Graph.

### Cloudflare

* Static output.
* Pages compatibility.
* Dependency audit.
* No unnecessary Worker runtime.

Output:

**Deployment-ready Astro project.**

---

# 54. Final Product Definition

Computer Center v1 harus terasa seperti:

> **Tempat di mana pelanggan bisa membeli komponen dan mendapatkan bantuan untuk membangun PC yang tepat.**

Bukan sekadar:

> **"Toko komputer online."**

Customer journey:

**Need → Learn → Browse → Compare → Consult → Build → Buy**

Prioritas:

**Product Discovery > Trust > PC Build Service > Consultation > CTA > SEO > Performance**

**Database:** Tidak diperlukan.

**Backend:** Tidak diperlukan.

**Framework:** Astro.

**Hosting:** Cloudflare Pages.

**Primary CTA:** Build Your PC.

**Secondary CTA:** Browse Components.

**Core Message:**
**"Build the PC that fits you."**

---

# AI DEVELOPMENT & DESIGN CONTROL PROTOCOL

## Project Protocol

This document defines the mandatory operating rules for all AI agents working on this project.

All instructions in this file must be read and followed before modifying any project file.

The primary purpose of this protocol is to preserve approved design states, prevent unintended redesigns, control AI modifications, and provide a predictable command system for development.

---

# 1. CORE PRINCIPLE

The AI agent must treat the existing approved project state as valuable and protected.

The AI must NEVER assume that an existing implementation should be improved, modernized, refactored, redesigned, simplified, or replaced unless the user explicitly requests it.

When the user's request is narrow, the modification must remain narrow.

The AI must preserve:

- Existing approved layouts
- Existing visual hierarchy
- Existing typography
- Existing spacing
- Existing colors
- Existing images
- Existing responsive behavior
- Existing interactions
- Existing functionality

unless explicitly instructed otherwise.

---

# 2. PROTOCOL PRIORITY

When interpreting instructions, use the following priority order:

1. Explicit user instruction
2. Active protocol command
3. Locked component rules
4. Approved checkpoint rules
5. Existing project implementation
6. General design or coding preferences

The AI must not override a higher-priority instruction with a lower-priority assumption.

---

# 3. BEFORE EVERY MODIFICATION

Before modifying any file, the AI must:

1. Read this `PROTOCOL.md`.
2. Identify the active protocol command.
3. Identify the exact component or files that need modification.
4. Check whether the target component is locked.
5. Preserve all unrelated components.
6. Avoid modifying files that are outside the requested scope.

The AI must NOT begin a broad redesign simply because a requested change affects part of the page.

---

# 4. MINIMAL CHANGE PRINCIPLE

The AI must make the smallest reasonable modification necessary to fulfill the user's request.

The AI must NOT:

- Rewrite unrelated components.
- Refactor unrelated code.
- Change the design system.
- Replace existing layouts without permission.
- Change typography without permission.
- Change spacing without permission.
- Replace images without permission.
- Change colors without permission.
- Modify responsive behavior outside the requested scope.
- Remove functionality unless explicitly requested.

If a requested modification can be completed by changing one component, the AI must not rewrite the entire page.

---

# 5. DESIGN PRESERVATION RULE

Existing design is considered protected by default.

The AI must NOT interpret requests such as:

- "Improve this"
- "Make this better"
- "Fix this"
- "Add this feature"

as permission to redesign unrelated sections.

If the request does not explicitly request redesign, preserve the existing visual appearance.

---

# 6. EXACT RESTORATION RULE

When restoring a previous state, the AI must restore the exact known implementation.

The AI must NOT:

- Recreate the design from memory.
- Generate a similar design.
- Approximate the previous layout.
- Improve the previous version.
- Modernize the previous version.
- Combine the previous design with the current design.

Restoration means restoring the previous code state as accurately as possible.

The AI must always prefer:

1. Git history
2. Git commit
3. Git diff
4. Existing backup
5. Explicit checkpoint reference

The AI must never guess the previous implementation if an exact source is available.

---

# 7. PROTOCOL COMMAND SYSTEM

Commands beginning with `/` are protocol commands.

Protocol commands must be interpreted according to this document.

The AI must execute the command according to its definition.

The AI must not reinterpret the meaning of a protocol command.

---

# 8. /REVERSE

## Purpose

Undo the latest unapproved modification.

## Execution Rules

When `/REVERSE` is activated:

1. Identify the latest modification made for the current task.
2. Identify all files affected by that modification.
3. Restore those files to their exact state before that modification.
4. Preserve all older approved changes.
5. Do not redesign anything.
6. Do not generate an alternative implementation.
7. Do not improve the restored version.
8. Do not modify unrelated files.

The AI must treat `/REVERSE` as:

"Restore the exact previous state."

The AI must NOT interpret `/REVERSE` as:

"Create something similar to the previous design."

After restoration, stop modifying the project unless the user provides another instruction.

---

# 9. /CHECKPOINT [NAME]

## Purpose

Create a named approved state.

Example:

`/CHECKPOINT homepage-v1`

When activated:

1. Identify the current project state.
2. Record the checkpoint name.
3. Record the relevant files associated with the checkpoint.
4. Record the purpose of the checkpoint.
5. Treat this state as an approved reference.

A checkpoint should preferably correspond to a Git commit whenever possible.

---

# 10. /RESTORE [NAME]

## Purpose

Restore a previously approved checkpoint.

Example:

`/RESTORE homepage-v1`

When activated:

1. Locate the exact checkpoint.
2. Identify its associated files or Git commit.
3. Restore the exact code state.
4. Do not reinterpret the design.
5. Do not merge the checkpoint with experimental changes unless explicitly requested.

The checkpoint is the source of truth.

---

# 11. /LOCK [COMPONENT]

## Purpose

Protect an approved component from modification.

Example:

`/LOCK HERO`

When a component is locked, the AI must NOT modify:

- Layout
- HTML structure
- CSS styling
- Typography
- Spacing
- Colors
- Images
- Animations
- Responsive behavior
- Component logic

unless explicitly instructed.

Example:

`/LOCK HERO`

means the Hero section must remain unchanged.

---

# 12. /UNLOCK [COMPONENT]

## Purpose

Remove protection from a previously locked component.

Example:

`/UNLOCK HERO`

Only after this command may the AI freely modify the specified component according to the user's instructions.

Unlocking one component does not unlock other components.

---

# 13. /STRICT

## Purpose

Enable strict modification mode.

When `/STRICT` is active:

- Modify only explicitly requested components.
- Modify only files required to complete the request.
- Do not refactor unrelated code.
- Do not redesign unrelated sections.
- Do not optimize unrelated components.
- Do not modify the design system.
- Do not make "helpful" visual changes.
- Preserve all existing behavior unless explicitly instructed otherwise.

The AI must prioritize precision over creativity.

---

# 14. /DESIGN-ONLY

## Purpose

Allow visual modifications while protecting application functionality.

The AI may modify:

- Layout
- Typography
- Spacing
- Colors
- Visual hierarchy
- Animation
- Responsive styling

The AI must NOT modify:

- Business logic
- API integrations
- Routing
- Data structures
- Application logic

unless explicitly requested.

---

# 15. /CODE-ONLY

## Purpose

Modify functionality while preserving the visual design.

When `/CODE-ONLY` is active, the existing visual design must remain unchanged.

The AI must NOT modify:

- Layout
- Typography
- Colors
- Spacing
- Images
- Animation
- Visual hierarchy

unless explicitly requested.

---

# 16. /WA

## Purpose

Activate the WhatsApp Floating Action Button protocol.

When `/WA` is activated:

1. Add a floating WhatsApp contact button.
2. Position it appropriately without obstructing important UI.
3. Use fixed positioning.
4. Ensure responsive behavior.
5. Ensure mobile safe-area compatibility.
6. Ensure the button is touch-friendly.
7. Use the existing design language.
8. Do not redesign the page.
9. Do not modify unrelated sections.
10. Do not change existing layout structure.

The WhatsApp button must be implemented as an isolated component whenever practical.

---

# 17. /REMOVE-WA

Remove the WhatsApp floating button and all directly associated implementation.

Do not modify unrelated components.

---

# 18. /SCOPE [COMPONENT OR FILE]

## Purpose

Restrict all modifications to a specific scope.

Example:

`/SCOPE HERO`

or:

`/SCOPE src/components/Hero.astro`

When active:

The AI may only modify the specified component or file.

Any required modification outside the scope must first be identified and explained.

The AI must not silently modify files outside the active scope.

---

# 19. /FREEZE-DESIGN

## Purpose

Freeze the entire visual design.

When active, the AI may modify functionality but must preserve the exact visual appearance.

The AI must NOT change:

- Layout
- Typography
- Spacing
- Colors
- Images
- Animations
- Component positioning

unless explicitly instructed.

---

# 20. /EXPERIMENT

## Purpose

Allow experimental changes without treating them as approved.

Experimental changes must be considered temporary.

The AI must:

1. Avoid modifying locked components.
2. Avoid modifying unrelated files.
3. Keep changes isolated whenever possible.
4. Clearly identify experimental files.
5. Preserve the ability to reverse the experiment.

Experimental work must not automatically replace an approved checkpoint.

---

# 21. APPROVAL SYSTEM

A modification becomes an approved reference only when the user explicitly approves it.

Examples:

- `APPROVED`
- `/CHECKPOINT homepage-v2`
- "This version is approved."
- "Keep this design."

Until explicit approval is given, major design modifications should be considered experimental.

---

# 22. DO NOT GUESS RULE

If the AI does not know which previous version the user means, the AI must NOT invent or recreate a design.

The AI must:

1. Inspect Git history.
2. Inspect recent changes.
3. Inspect checkpoints.
4. Inspect available project history.

Only if no previous state exists should the AI ask the user for clarification.

The AI must never silently guess.

---

# 23. CHANGE REPORT

After completing a modification, the AI must provide a concise report containing:

### Modified

List modified files.

### Preserved

List important components intentionally left unchanged.

### Protocol

State which protocol commands were active.

### Reversal

Explain how the change can be reversed.

The report should remain concise.

---

# 24. STOP CONDITION

After successfully completing the requested task, the AI must stop.

The AI must NOT continue with:

- Additional redesign
- Optional improvements
- Unrequested refactoring
- Additional feature development
- Visual experimentation

unless explicitly requested.

Completion means completion.

---

# 25. DEFAULT SAFE MODE

If no explicit protocol command is provided, the AI must operate in:

`SAFE MODE`

SAFE MODE rules:

- Preserve existing design.
- Preserve existing functionality.
- Make minimal modifications.
- Do not redesign unrelated components.
- Do not refactor unrelated code.
- Do not replace approved implementation.
- Prefer isolated changes.
- Treat ambiguity as a reason to inspect project history, not as permission to guess.

---

# 26. FINAL OPERATING INSTRUCTION

The AI agent must follow this principle:

"Preserve first. Modify second. Never redesign without permission. Never guess a previous state when an exact state can be restored."

The existing project is the source of truth.

User-approved checkpoints are protected states.

Protocol commands must be followed literally.

Precision is more important than creativity.
