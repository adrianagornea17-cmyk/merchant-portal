# Merchant Portal — Project Guide

## What this is
A GitHub Pages site hosting Verifone UI prototypes/mockups.

- **Live URL:** https://adrianagornea17-cmyk.github.io/merchant-portal/
- **Local path:** `/Users/adrianagornea/portal/`
- **GitHub repo:** `adrianagornea17-cmyk/merchant-portal` (auto-deploys on push to main)

## How to add a new page / mockup

### Step 1 — Create the HTML file
Save the new mockup as a `.html` file directly in `/Users/adrianagornea/portal/`.
Name it descriptively in kebab-case, e.g. `payment-methods.html`.

### Step 2 — Add a card to `index.html`
Open `index.html` and insert a new `<a class="card">` block before the closing `</div>` at line ~535 (just after the last card). Follow this exact pattern:

```html
<!-- Short description of what this card is -->
<a class="card" href="YOUR-FILE.html">
  <div class="card-icon" style="background:#eff6ff;">
    <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#2563eb" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <!-- pick an appropriate SVG icon path -->
    </svg>
  </div>
  <span class="tag" style="background:#eff6ff;color:#1d4ed8;">Tag Label</span>
  <div class="card-title">Page Title</div>
  <div class="card-desc">One or two sentences describing what this mockup shows.</div>
  <div class="card-link">Open →</div>
</a>
```

**Icon background / color combos to pick from:**

| Theme        | Background | Stroke / Text color   |
|--------------|------------|-----------------------|
| Dark         | `#0f172a`  | `#38bdf8`             |
| Blue (light) | `#eff6ff`  | `#2563eb` / `#1d4ed8` |
| Green        | `#f0fdf4`  | `#16a34a` / `#166534` |
| Purple       | `#fdf4ff`  | `#9333ea` / `#7e22ce` |
| Sky blue     | `#f0f9ff`  | `#0284c7` / `#0369a1` |
| Orange       | `#fff7ed`  | `#ea580c` / `#c2410c` |
| Pink/Rose    | `#fff1f2`  | `#e11d48` / `#9f1239` |

### Step 3 — Deploy
```bash
git add YOUR-FILE.html index.html
git commit -m "Add [page name] mockup"
git push
```
GitHub Pages picks up the change automatically (usually within 1–2 min).

---

## Existing pages (as of 2026-06-04)

| File | Card title | Tag |
|------|-----------|-----|
| `merchant-portal.html` | Merchant Portal | Dark theme |
| `verifone-transactions.html` | Transactions — Base | Light theme |
| `index-v1-collapsible.html` | Collapsible Filters | Option 1 |
| `index-v2-sidepanel.html` | Filter Side Panel | Option 2 |
| `administration-organizations.html` | Administration · Organizations | Admin |
| `NEW organization-page-ui.html` | Organization Page Enhancement | Enhancement |
| `VC Template_builder.html` | Report Template Builder | Commerce |

## Files in the repo NOT yet on the index
These exist locally but have no card on `index.html` yet — add them if needed:
- `jira-reports.html`
- `3ds-authentications.html`
- `customer-catalog.html`
- `add-template.html`
- `releases-2026.html`
- `weekly-jira-status-q1-2026/` (subdirectory with its own `index.html`)
- `weekly-jira-status-q3-2026/` (subdirectory with its own `index.html`)
