# 🎨 CodexLog Styleguide

Ein minimalistischer, strukturierter Leitfaden für alle visuell und funktional relevanten Elemente von **codexlog**.

---

## 🏷 Wortmarke

- Schreibweise: **codexlog** (immer klein)
- Einheitlich in Code, UI, Domains, Dokumentation
- Siehe: [`wordmark.md`](./wordmark.md)

---

## 🎨 Farbpalette

### Primärfarben

| Zweck                      | Hex       | Beschreibung                     |
|---------------------------|-----------|----------------------------------|
| Icon / Call to Action     | `#D33838` | Monolith-Rot, dominant           |
| Schriftmarke / UI-Rahmen  | `#021B36` | Dunkles Blau, seriös, Header     |
| Hintergrund (Lightmode)   | `#FAFAFA` | Klar, softweiß                   |
| Hintergrund (Darkmode)    | `#0F172A` | `dark:bg-slate-900`              |

### Sekundärfarben

| Zweck               | Hex       | Beschreibung                      |
|---------------------|-----------|-----------------------------------|
| Akzent 1 (Hellrot)  | `#FF5757` | Hover/Active-Zustände             |
| Akzent 2 (Sandgrau) | `#D6D3D1` | Layer, Border                     |
| UI-Text dunkel       | `#1E293B` | `text-slate-800`                  |
| UI-Text hell         | `#CBD5E1` | `text-slate-300` (Darkmode)       |

---

## 🔠 Typografie

- **Satoshi**: Headlines, UI-Elemente
- **IBM Plex Mono**: Logbuch, Affirmationen, kodexartige Texte
- Optional: Inter, Space Grotesk

---

## 🧱 Komponentenstil (Tailwind)

### Primärbutton

```jsx
<button className="bg-[#D33838] text-white font-medium px-4 py-2 rounded hover:bg-[#bb2f2f] dark:hover:bg-[#a72a2a]">
  {t("cta.start")}
</button>
```

### Sekundärbutton

```jsx
<button className="border border-[#D33838] text-[#D33838] px-4 py-2 rounded hover:bg-[#fef2f2] dark:hover:bg-[#3b0d0d]">
  {t("cta.secondary")}
</button>
```

### Input-Feld

```jsx
<input className="bg-white dark:bg-slate-800 border border-gray-300 dark:border-slate-600 rounded px-3 py-2 text-sm text-gray-900 dark:text-gray-100 placeholder:text-gray-400 dark:placeholder:text-gray-500 focus:outline-none focus:ring-2 focus:ring-[#D33838]" />
```

---

## 🌒 Darkmode-Kompatibilität

- Immer mit Tailwind `dark:`-Klassen arbeiten
- Kein invertiertes Design – getrennte Farbwelten
- Logos mit `fill="currentColor"`
- Fokus: Kontrast, Lesbarkeit, Layering

---

## 🌐 Internationalisierung (i18n)

- Unterstützte Sprachen: Deutsch (de), Englisch (en)
- UI-Texte über `useTranslation()` (react-i18next)
- Übersetzungsdateien in `frontend/src/locales/de|en/*.json`
- Sprachumschalter: „DE“ / „EN“ im Header

---

## 📁 Ablageort

Dieses Dokument liegt im Projektverzeichnis:  
`/docs/branding/styleguide.md`

---

# 🎨 CodexLog Style Guide

A minimalist and structured guide for all visual and functional elements of **codexlog**.

---

## 🏷 Wordmark

- Spelling: **codexlog** (always lowercase)
- Used consistently in code, UI, domains, and documentation
- See: [`wordmark.md`](./wordmark.md)

---

## 🎨 Color Palette

### Primary Colors

| Purpose                  | Hex       | Description                      |
|--------------------------|-----------|----------------------------------|
| Icon / Call to Action    | `#D33838` | Monolith red, strong, emotional |
| Wordmark / UI Frame      | `#021B36` | Blue-black, solid header base   |
| Background (Lightmode)   | `#FAFAFA` | Soft white, subtle base         |
| Background (Darkmode)    | `#0F172A` | Tailwind `dark:bg-slate-900`    |

### Secondary Colors

| Purpose             | Hex       | Description                        |
|---------------------|-----------|------------------------------------|
| Accent 1 (light red)| `#FF5757` | Hover/Active states                |
| Accent 2 (sand gray)| `#D6D3D1` | Borders, dividers, layers          |
| UI Text dark        | `#1E293B` | `text-slate-800`                   |
| UI Text light       | `#CBD5E1` | `text-slate-300` (dark mode text)  |

---

## 🔠 Typography

- **Satoshi**: Headlines, large UI elements
- **IBM Plex Mono**: Logbook entries, affirmations, code-like elements
- Optional: Inter, Space Grotesk

---

## 🧱 Component Style (Tailwind)

### Primary Button

```jsx
<button className="bg-[#D33838] text-white font-medium px-4 py-2 rounded hover:bg-[#bb2f2f] dark:hover:bg-[#a72a2a]">
  {t("cta.start")}
</button>
```

### Secondary Button

```jsx
<button className="border border-[#D33838] text-[#D33838] px-4 py-2 rounded hover:bg-[#fef2f2] dark:hover:bg-[#3b0d0d]">
  {t("cta.secondary")}
</button>
```

### Input Field

```jsx
<input className="bg-white dark:bg-slate-800 border border-gray-300 dark:border-slate-600 rounded px-3 py-2 text-sm text-gray-900 dark:text-gray-100 placeholder:text-gray-400 dark:placeholder:text-gray-500 focus:outline-none focus:ring-2 focus:ring-[#D33838]" />
```

---

## 🌒 Dark Mode Compatibility

- Always use Tailwind `dark:` classes
- Avoid inversion – define dark mode colors separately
- Use `fill="currentColor"` for icons/logos
- Focus on contrast, readability, and layering

---

## 🌐 Internationalization (i18n)

- Supported languages: German (de), English (en)
- Use `useTranslation()` (react-i18next) in components
- Translation files in `frontend/src/locales/de|en/*.json`
- Language switch: "DE" / "EN" in header

---

## 📁 Location

This file resides at:  
`/docs/branding/styleguide.md`
