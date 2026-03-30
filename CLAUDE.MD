
# CLAUDE.md — Accounting Firm Website Builder

> 👋 **Before we get started — this file has three placeholders that need to be filled in with your details:**
>
> - `{{FIRM_NAME}}` — the name of your accounting firm (e.g. *Smith & Associates CPA*)
> - `{{WEBSITE_URL}}` — your intended domain, used for display purposes only (e.g. *www.smithcpa.com*)
> - `{{STORY}}` — a short description of your firm's background, personality, or what makes it different (e.g. *"We started as a small family practice in Austin in 2008 and now specialise in serving e-commerce businesses and freelancers. We're known for being straight-talking and genuinely proactive — our clients hear from us before tax season, not during it."*)
>
> The `{{STORY}}` placeholder is what makes your site feel like *yours* rather than a generic template. The more honest and specific you are, the better the result.
>
> **To personalise this project, simply tell Claude:**
> *"My firm is called [name], my website is [URL], and here's our story: [your story]"*
>
> Claude will use those details to build a website tailored to your firm.

---

## Project Overview

This project builds a professional marketing website for **{{FIRM_NAME}}**, an American accounting firm. The goal is a polished, trustworthy, conversion-focused site that communicates expertise and builds client confidence.

The site's copy, tone, and personality should be informed by the firm's story:

> *{{STORY}}*

**Intended domain:** `{{WEBSITE_URL}}` *(for display purposes — this site runs locally)*

> ⚠️ **Local hosting note:** All links, CTAs, and navigation must use relative paths or anchor links (e.g. `#contact`, `#services`). Do not use absolute URLs. The site must work correctly when opened directly as a local `index.html` file in a browser — no server required.

---

## Brand Assets

Check the `images/` folder for any brand assets before building. These may include:

- **Logo** — use in the nav header and footer if present (e.g. `images/logo.png`)
- **Banners or hero images** — use as background or feature imagery in the Hero section if available
- **Other assets** — photos, icons, or graphics that should be incorporated into the design

Reference these using relative paths (e.g. `<img src="images/logo.png">`). If the `images/` folder is empty or an asset is missing, design around it gracefully — use a text-based logo treatment or CSS-generated visuals rather than broken image placeholders.

---

## Skills Available

This repo includes two skills Claude should use when building or styling the site. Always read the relevant `SKILL.md` before starting work.

| Skill | Location | Purpose |
|---|---|---|
| `frontend-design` | `skills/frontend-design/SKILL.md` | Build distinctive, production-grade web pages and components |
| `theme-factory` | `skills/theme-factory/SKILL.md` | Apply a cohesive color palette and font system to the site |

---

## How to Build the Site

### Step 1 — Read the Skills
Before writing any code, read both skill files:
- `skills/frontend-design/SKILL.md`
- `skills/theme-factory/SKILL.md`

### Step 2 — Select a Theme
Follow the `theme-factory` skill instructions:
1. Display `skills/theme-factory/theme-showcase.pdf` so the user can browse available themes
2. Ask the user to choose a theme (or describe a custom look)
3. Wait for confirmation before proceeding

### Step 3 — Build the Website
Using the `frontend-design` skill, build a single-page marketing website for **{{FIRM_NAME}}** as a single `index.html` file. Apply the chosen theme's colors and fonts throughout.

---

## Site Structure

Build the following sections in order:

### 1. Hero
- Firm name: **{{FIRM_NAME}}**
- A confident headline — draw from `{{STORY}}` to make this feel specific and earned, not generic
- A short subheading (1–2 sentences) describing who the firm serves and what makes it different
- Primary CTA button: *"Book a Free Consultation"* — anchor link to `#contact`
- Secondary CTA: *"See Our Services"* — smooth-scrolls to `#services`

### 2. Services
Highlight the firm's core offerings with short descriptions. Suggested services for an American accounting firm:
- Tax Preparation & Planning (Individual and Business)
- Bookkeeping & Payroll
- CFO Advisory Services
- Business Formation & Entity Structuring
- IRS Representation & Audit Support
- Financial Reporting & Compliance

Use an icon-based card grid layout. Keep copy tight — one sentence per service.

### 3. Why Choose Us
Three to four trust-building differentiators. Where possible, draw these from `{{STORY}}` — specific, real differentiators land better than generic ones. If the story doesn't provide enough detail, fall back to sensible defaults like:
- *Proactive, year-round tax strategy* (not just April advice)
- *Certified CPAs with [X]+ years of experience*
- *Dedicated point of contact for every client*
- *Technology-forward — secure client portal, real-time reporting*

### 4. About
Use `{{STORY}}` as the foundation for this section. Expand it into a short paragraph or two that communicates the firm's mission, its history, and the kind of clients it serves best. Keep the tone warm and human — write it the way the firm would actually talk about itself, not how a marketing agency would.

### 5. Testimonials
Three fictional-but-realistic client testimonials. Include:
- A short quote (2–3 sentences)
- Client first name and last initial
- Their business type (e.g. *"Owner, retail small business"*, *"Freelance consultant"*)

### 6. Contact / CTA Banner
- Add `id="contact"` to this section so the Hero CTA links correctly
- A full-width banner with a clear call to action: *"Ready to take the stress out of your finances?"*
- CTA button: *"Schedule a Call"* — can be a `mailto:` link or `tel:` link using placeholder values
- Display the firm's email, phone, and address as placeholder text (to be updated by the user)

### 7. Footer
- Firm name: **{{FIRM_NAME}}**
- Navigation links mirroring the section structure
- Disclaimer: *"{{FIRM_NAME}} is a licensed CPA firm. This website is for informational purposes only."*
- Copyright line: *"© 2025 {{FIRM_NAME}}. All rights reserved."*

---

## Design Direction

Follow the `frontend-design` skill for all aesthetic decisions. Key guidance for this project:

- **Tone:** Authoritative but approachable. Think refined professional, not sterile corporate.
- **Typography:** Choose a distinctive, trustworthy pairing — a strong serif or slab display font paired with a clean, legible body font. Avoid generic system fonts.
- **Color:** Apply the chosen theme faithfully. Ensure strong contrast and accessibility (WCAG AA minimum).
- **Motion:** Subtle entrance animations on scroll for section reveals. Avoid anything that feels flashy or distracting — this is a financial services site.
- **Layout:** Clean grid structure. Generous white space. The site should feel considered and premium, not crowded.
- **Avoid:** Purple gradients, stock-photo aesthetics, generic SaaS-style design, or anything that looks like it could be any business in any industry.

---

## Output

Deliver a single `index.html` file with all CSS and JavaScript inline. The file must work when opened directly in a browser as a local file — no web server, no external dependencies that require network access. Google Fonts may be used via CDN link (these load fine from a local file given internet access), but all layout, styles, and scripts must be self-contained.

Save the output to: `output/index.html`

---

## Reminder

If `{{FIRM_NAME}}`, `{{WEBSITE_URL}}`, or `{{STORY}}` still appear as literal placeholders when you read this, **stop and ask the user to provide their firm name, website URL, and a brief description of their firm's story** before proceeding. Do not generate a site using the placeholder text as content.
