# codexlog – Brand & Style Guide (EN)

> **Version 1.0** · Effective: 01.05.2025
> This document combines the former **BRAND\_GUIDELINES.md** and **styleguide.md** into a single, authoritative guide.
>
> **Goal:** Define a consistent, minimalist, and disciplined visual and UI language across all codexlog touchpoints: code repos, web app, documentation, and marketing.

---

## 1 · Naming

* Always written as **codexlog** (lowercase)
* Never use CamelCase, ALLCAPS, or abbreviations
* Use consistently in code, URLs, UI, and communication

---

## 2 · Logo System

### 2.1 Primary Icon

* Red square (`#D33838`) with centered white slit
* Corner radius ≈ 12%
* Clear space: **½ icon width** around all edges

### 2.2 Lockup (Icon + Wordmark)

* Wordmark in **Satoshi Bold** (fallback: system sans-serif)
* Icon height = x-height of the wordmark

### 2.3 Scaling

| Asset            | Size   | Usage               |
| ---------------- | ------ | ------------------- |
| `icon-16.png`    | 16 px  | Favicon             |
| `icon-32.png`    | 32 px  | Browser tab @2×     |
| `icon-128.png`   | 128 px | Desktop app, social |
| `splash-512.png` | 512 px | PWA splash screen   |

**Don’ts:** Change the red · Mirror, skew, distort · Add letters (e.g. "n") · Close the slit

---

## 3 · Color Palette

### 3.1 Design Tokens

```css
:root {
  --cl-primary: #D33838;     /* Monolith red */
  --cl-ink: #021B36;         /* Blue-black ink */
  --cl-bg: #FAFAFA;          /* Light background */
  --cl-bg-dark: #0F172A;     /* Dark background */
  --cl-accent-1: #FF5757;    /* Hover red */
  --cl-accent-2: #D6D3D1;    /* Sand gray */
  --cl-text-dark: #1E293B;
  --cl-text-light: #CBD5E1;
}
```

### 3.2 Contrast Compliance

All color combinations meet **WCAG AA** (contrast ratio ≥ 4.5) in both light and dark mode.

---

## 4 · Typography

| Usage                | Font          | Weight      | Notes                   |
| -------------------- | ------------- | ----------- | ----------------------- |
| Headlines / Wordmark | **Satoshi**   | Bold 700    | Modern and minimalistic |
| Body text            | Inter         | Regular 400 | Fallback-safe           |
| Code & log entries   | IBM Plex Mono | Regular 400 | Technical aesthetic     |

> Use a maximum of 2 font families simultaneously.

---

## 5 · UI Components (Tailwind Snippets)

### 5.1 Primary Button

```jsx
<button className="bg-[#D33838] text-white font-medium px-4 py-2 rounded hover:bg-[#bb2f2f] dark:hover:bg-[#a72a2a] focus:outline-none">
  {t("cta.start")}
</button>
```

### 5.2 Secondary Button

```jsx
<button className="border border-[#D33838] text-[#D33838] px-4 py-2 rounded hover:bg-[#fef2f2] dark:hover:bg-[#3b0d0d]">
  {t("cta.secondary")}
</button>
```

### 5.3 Input Field

```jsx
<input className="bg-white dark:bg-slate-800 border border-gray-300 dark:border-slate-600 rounded px-3 py-2 text-sm text-gray-900 dark:text-gray-100 placeholder:text-gray-400 dark:placeholder:text-gray-500 focus:outline-none focus:ring-2 focus:ring-[#D33838]" />
```

---

## 6 · Dark Mode Guidelines

* Use Tailwind’s `dark:` classes (no auto-inversion)
* Icons/logos use `fill="currentColor"`
* Maintain layering and transparency
* Focus: clarity and contrast

---

## 7 · Internationalization (i18n)

* Supported languages: **de**, **en**
* Translations stored in `frontend/src/locales/{lang}/*.json`
* Use `useTranslation()` in React components
* Persist language via `localStorage` or user setting

---

## 8 · Asset & Repo Structure

```
/docs/
  BRAND_STYLE_GUIDE.md   ← this file
/assets/
  /logo/
    icon.svg
    icon-16.png
    icon-32.png
    icon-128.png
    lockup-horizontal.svg
    splash-512.png
  /fonts/
    satoshi-*.woff2
    inter-*.woff2
    ibm-plex-mono-*.woff2
```

---

## 9 · Legal / Trademark

* Icon and wordmark will be registered as a word/image trademark "codexlog" (DPMA / EUIPO)
* Not affiliated with npm, React, or other entities
* Any modification requires written permission

---

## 10 · Contact & Workflow

* **Brand Lead**: Skimi (@skimi)
* **Design Review**: GitHub PR with `design` label
* All changes via PR, reviewed by @skimi + @design-team

---

> *Keep it minimal. Keep it disciplined. – codexlog* 🫡
