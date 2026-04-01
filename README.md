
# ic-presentation-template (UNICAMP)

A modular LaTeX presentation template designed for the **Institute of Computing (IC)** community.

This template avoids outdated Beamer defaults and provides a clean, high-contrast, and maintainable structure with minimal configuration.

---

## 🚀 Status

- **Overleaf:** Verified (March 31, 2026)
- **Compiler:** pdfLaTeX
- **TeX Live:** 2025/2026 compatible

---

## ✨ Features

- **Clean Layout:** Removes default Beamer clutter for a modern look
- **Consistent Structure:** Clear separation between metadata, theme, and content
- **Modular Colors:** Centralized color palette (Primary, Secondary, Accent)
- **Stable TOC Styling:** Table of contents colors behave predictably
- **Scientific Ready:** Includes `chemfig` and `mhchem`
- **No Hidden Magic:** Minimal overrides, everything explicit

---

## 📁 Project Structure

```

.
├── src/
│   └── main.tex
└── README.md

````

---

## 🛠️ Usage

### Option A: Overleaf (Cloud - Beginner Friendly)

1. Create a new project in **Overleaf**
2. Copy the contents of `src/main.tex`
3. Paste into Overleaf
4. Update metadata at the top of the file
5. Click **Recompile**

---

### Option B: Local Setup (Arch / Omarchy)

#### Install Dependencies

```bash
sudo pacman -S texlive-basic texlive-latexextra texlive-fontsrecommended \
               texlive-fontsextra texlive-bibtexextra texlive-plaingeneric \
               texlive-binextra texlive-science biber
````

---

#### Continuous Compilation (Recommended)

```bash
latexmk -pvc -pdf src/main.tex
```

---

## ✏️ Customization

### Metadata

Edit the following section in `main.tex`:

```tex
% 1. METADATA
```

You can change:

* title
* author
* institute
* date

---

### 🎨 Colors

Edit:

```tex
% 2. COLORS
```

Available tokens:

* `ColorPrimary`
* `ColorSecondary`
* `ColorAccent`
* `ColorAccentLight`

---

## 🎓 Affiliation

Developed by **Luis Alberto Vásquez Vargas**
Institute of Computing (IC) — UNICAMP

