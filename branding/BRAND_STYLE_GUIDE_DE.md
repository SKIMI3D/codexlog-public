# codexlog – Brand & Style Guide

> **Version 1.0** · gültig ab: 01.5.2025
> Dieses Dokument vereint das frühere **BRAND\_GUIDELINES.md** und **styleguide.md** in einem einzigen, verbindlichen Leitfaden.
>
> **Ziel:** Einheitliche, minimalistische und disziplinierte Marken‑ und UI‑Sprache für alle codexlog‑Touchpoints: Code‑Repos, Web‑App, Docs, Marketing.

---

## 1 · Wortmarke

* Schreibweise immer: **codexlog** (klein)
* Keine CamelCase‑, ALLCAPS‑ oder Abkürzungsvarianten.
* In Code‑Variablen, Domains, UI, Marketing identisch verwenden.

---

## 2 · Logo‑System

### 2.1 Primär‑Icon

* Rotes Quadrat (`#D33838`) mit zentriertem weißen Schlitz.
* Corner‑Radius ≈ 12 %.
* Mindestfreiraum: **½ × Iconbreite** um das Symbol.

### 2.2 Lockup (Icon + Wortmarke)

* Wortmarke setzt in **Satoshi** (Fallback: system‑sans).
* Iconhöhe = x‑Höhe der Wortmarke.

### 2.3 Skalierung

| Asset            | Größe  | Zweck               |
| ---------------- | ------ | ------------------- |
| `icon-16.png`    | 16 px  | Favicon             |
| `icon-32.png`    | 32 px  | Browser‑Tab @2×     |
| `icon-128.png`   | 128 px | Desktop App, Social |
| `splash-512.png` | 512 px | PWA Splash          |

**Don’ts:** Rot verändern · Spiegeln/Neigen/Verzerren · Buchstaben hinzufügen (npm‑Look‑alike) · Schlitz schließen.

---

## 3 · Farbpalette

### 3.1 Design Tokens

```css
:root {
  --cl-primary: #D33838; /* Monolith‑Rot */
  --cl-ink: #021B36;    /* Wortmarke‑Blau-Schwarz */
  --cl-bg: #FAFAFA;     /* Light‑BG */
  --cl-bg-dark: #0F172A;/* Dark‑BG */
  --cl-accent-1: #FF5757;/* Hover‑Rot */
  --cl-accent-2: #D6D3D1;/* Sandgrau */
  --cl-text-dark: #1E293B;
  --cl-text-light: #CBD5E1;
}
```

Palette übernommen aus dem ursprünglichen Styleguide .

### 3.2 Kontrast‑Check

Alle Farb­kombinationen erfüllen WCAG AA (Kontrast ≥ 4.5) – geprüft für Light‑ und Dark‑Mode.

---

## 4 · Typografie

| Einsatz               | Font          | Gewicht     | Bemerkung              |
| --------------------- | ------------- | ----------- | ---------------------- |
| Headlines / Wortmarke | **Satoshi**   | Bold 700    | minimalistisch, modern |
| Body‑Text             | Inter         | Regular 400 | fallback‑sicher        |
| Code & Log‑Entries    | IBM Plex Mono | Regular 400 | technischer Look       |

> Max. 2 Fonts gleichzeitig verwenden.

---

## 5 · UI‑Komponenten (Tailwind‑Snippets)

### 5.1 Primär‑Button

```jsx
<button className="bg-[#D33838] text-white font-medium px-4 py-2 rounded hover:bg-[#bb2f2f] dark:hover:bg-[#a72a2a] focus:outline-none">
  {t("cta.start")}
</button>
```

### 5.2 Sekundär‑Button

```jsx
<button className="border border-[#D33838] text-[#D33838] px-4 py-2 rounded hover:bg-[#fef2f2] dark:hover:bg-[#3b0d0d]">
  {t("cta.secondary")}
</button>
```

### 5.3 Input‑Feld

```jsx
<input className="bg-white dark:bg-slate-800 border border-gray-300 dark:border-slate-600 rounded px-3 py-2 text-sm text-gray-900 dark:text-gray-100 placeholder:text-gray-400 dark:placeholder:text-gray-500 focus:outline-none focus:ring-2 focus:ring-[#D33838]" />
```

Snippets direkt aus dem alten Styleguide übernommen .

---

## 6 · Dark‑Mode‑Richtlinien

* Tailwind `dark:`‑Klassen, kein automatisches Invertieren.
* `fill="currentColor"` für Icons/Logos verwenden.
* Layering & Transparenz beibehalten.
* Focus: Lesbarkeit, Kontrast.

---

## 7 · Internationalisierung (i18n)

* Sprachen: **de**, **en**.
* Übersetzungsdateien in `frontend/src/locales/{lang}/*.json`.
* In React‑Komponenten `useTranslation()` nutzen.
* Sprache persistent via `localStorage` oder User‑Einstellung.

---

## 8 · Asset‑ & Repo‑Struktur

```
/docs/
  BRAND_STYLE_GUIDE.md   ← dieses Dokument
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

## 9 · Legal / Trademark

* Icon + Wortmarke werden als Wort‑/Bildmarke „codexlog“ angemeldet (DPMA / EUIPO).
* Nicht mit npm, React oder anderen Marken verbunden.
* Jede Modifikation bedarf schriftlicher Genehmigung.

---

## 10 · Kontakt & Workflow

* **Brand Lead**: Skimi (@skimi)
* **Design Review**: GitHub PR mit Label `design`
* Änderungen nur via PR, Reviewer: @skimi + @design‑team

---

> *Keep it minimal. Keep it disciplined. – codexlog* 🫡
