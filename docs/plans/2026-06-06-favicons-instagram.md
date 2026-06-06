# Favicons + Instagram Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Agregar favicons al sitio y el ícono de Instagram en navbar y sección Contact.

**Architecture:** Solo se modifica `index.html`. Los favicons ya existen en `favicon-final/`. El ícono de Instagram usa Font Awesome (`fa-brands fa-instagram`) y las clases CSS existentes (`nav-social-link`, `contact-btn`).

**Tech Stack:** HTML5 estático, Font Awesome 6.5 (ya cargado vía CDN), sin build process.

---

### Task 1: Agregar favicons en el `<head>`

**Files:**
- Modify: `index.html:8` (después de la línea `<title>`)

**Step 1: Abrir `index.html` y ubicar el bloque `<head>`**

Buscar la línea:
```html
<title>Santiago Marquez</title>
```
Está cerca de la línea 6.

**Step 2: Insertar los `<link>` de favicon justo después de `<title>`**

```html
<link rel="icon" type="image/x-icon" href="favicon-final/favicon.ico" />
<link rel="icon" type="image/png" sizes="16x16" href="favicon-final/favicon-16.png" />
<link rel="icon" type="image/png" sizes="32x32" href="favicon-final/favicon-32.png" />
<link rel="icon" type="image/png" sizes="48x48" href="favicon-final/favicon-48.png" />
<link rel="apple-touch-icon" sizes="180x180" href="favicon-final/apple-touch-icon-180.png" />
```

**Step 3: Verificar en el navegador**

Abrir `index.html` en el browser. La pestaña debe mostrar el ícono del favicon.

**Step 4: Commit**

```bash
git add index.html
git commit -m "feat: add favicons"
```

---

### Task 2: Agregar Instagram en la navbar

**Files:**
- Modify: `index.html` — sección `<div class="nav-social">`

**Step 1: Ubicar el bloque `.nav-social`**

Buscar en `index.html`:
```html
<div class="nav-social">
```
Contiene los enlaces de Email, LinkedIn y GitHub (líneas ~34-37).

**Step 2: Agregar el enlace de Instagram al final del bloque, antes del `</div>`**

```html
<a href="https://www.instagram.com/thiag.ssj/" target="_blank" class="nav-social-link" title="Instagram"><i class="fa-brands fa-instagram"></i></a>
```

El bloque quedará así:
```html
<div class="nav-social">
  <a href="mailto:santigomarquez777@gmail.com" class="nav-social-link" title="Email"><i class="fa-solid fa-envelope"></i></a>
  <a href="https://www.linkedin.com/in/santiago-marquez-oviedo26" target="_blank" class="nav-social-link" title="LinkedIn"><i class="fa-brands fa-linkedin"></i></a>
  <a href="https://github.com/thiagossj7" target="_blank" class="nav-social-link" title="GitHub"><i class="fa-brands fa-github"></i></a>
  <a href="https://www.instagram.com/thiag.ssj/" target="_blank" class="nav-social-link" title="Instagram"><i class="fa-brands fa-instagram"></i></a>
</div>
```

**Step 3: Verificar en el navegador**

Abrir `index.html`. El ícono de Instagram debe aparecer en la navbar junto a los otros íconos sociales, con el mismo estilo hover.

**Step 4: Commit**

```bash
git add index.html
git commit -m "feat: add Instagram link to navbar"
```

---

### Task 3: Agregar Instagram en la sección Contact

**Files:**
- Modify: `index.html` — sección `<div class="contact-links">`

**Step 1: Ubicar el bloque `.contact-links`**

Buscar en `index.html`:
```html
<div class="contact-links">
```
Contiene los botones de Email, LinkedIn y GitHub (líneas ~157-169).

**Step 2: Agregar el botón de Instagram al final del bloque, antes del `</div>`**

```html
<a href="https://www.instagram.com/thiag.ssj/" target="_blank" class="contact-btn">
  <i class="fa-brands fa-instagram"></i>
  <span>Instagram</span>
</a>
```

El bloque quedará así:
```html
<div class="contact-links">
  <a href="mailto:santigomarquez777@gmail.com" class="contact-btn">
    <i class="fa-solid fa-envelope"></i>
    <span>Email</span>
  </a>
  <a href="https://www.linkedin.com/in/santiago-marquez-oviedo26" target="_blank" class="contact-btn">
    <i class="fa-brands fa-linkedin"></i>
    <span>LinkedIn</span>
  </a>
  <a href="https://github.com/thiagossj7" target="_blank" class="contact-btn">
    <i class="fa-brands fa-github"></i>
    <span>GitHub</span>
  </a>
  <a href="https://www.instagram.com/thiag.ssj/" target="_blank" class="contact-btn">
    <i class="fa-brands fa-instagram"></i>
    <span>Instagram</span>
  </a>
</div>
```

**Step 3: Verificar en el navegador**

Bajar a la sección Contact. El botón Instagram debe aparecer con el mismo estilo que Email, LinkedIn y GitHub.

**Step 4: Commit final**

```bash
git add index.html
git commit -m "feat: add Instagram link to contact section"
```
