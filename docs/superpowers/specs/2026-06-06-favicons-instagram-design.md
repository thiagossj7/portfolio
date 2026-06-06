# Favicons + Instagram — Design Spec
**Date:** 2026-06-06
**Owner:** Santiago Marquez

---

## Overview

Add favicons to the portfolio site and integrate an Instagram social link in both the navbar and the contact section, matching the existing visual style.

---

## Changes

### 1. Favicons

Add `<link>` tags in the `<head>` of `index.html` pointing to the existing files in `favicon-final/`. No files need to be moved.

```html
<link rel="icon" type="image/x-icon" href="favicon-final/favicon.ico" />
<link rel="icon" type="image/png" sizes="16x16" href="favicon-final/favicon-16.png" />
<link rel="icon" type="image/png" sizes="32x32" href="favicon-final/favicon-32.png" />
<link rel="icon" type="image/png" sizes="48x48" href="favicon-final/favicon-48.png" />
<link rel="apple-touch-icon" sizes="180x180" href="favicon-final/apple-touch-icon-180.png" />
```

Files available in `favicon-final/`:
- `favicon.ico` — navegadores legacy y pestaña del browser
- `favicon-16.png` — pestaña estándar
- `favicon-32.png` — retina
- `favicon-48.png` — atajos de escritorio Windows
- `apple-touch-icon-180.png` — iPhone/iPad home screen icon
- `favicon-256.png` / `favicon-512.png` — disponibles para uso futuro (PWA)

### 2. Instagram — Navbar

Inside the `.nav-social` div (alongside Email, LinkedIn, GitHub), add:

```html
<a href="https://www.instagram.com/thiag.ssj/" target="_blank" class="nav-social-link" title="Instagram">
  <i class="fa-brands fa-instagram"></i>
</a>
```

### 3. Instagram — Contact Section

Inside the `.contact-links` div (alongside Email, LinkedIn, GitHub), add:

```html
<a href="https://www.instagram.com/thiag.ssj/" target="_blank" class="contact-btn">
  <i class="fa-brands fa-instagram"></i>
  <span>Instagram</span>
</a>
```

---

## Files Modified

| File | Change |
|---|---|
| `index.html` | Add favicon `<link>` tags in `<head>`; add Instagram link in `.nav-social` and `.contact-links` |

No changes required to `style.css` or `script.js` — all new elements reuse existing classes.

---

## Out of Scope

- PWA manifest file (`site.webmanifest`)
- Changes to mobile layout or responsive behavior
