# ⚡️ AnkiDroid Neon Light Theme

> A high-performance, minimalist white theme for Anki and AnkiDroid featuring vibrant neon accents, custom MathJax/LaTeX integration, and intelligent responsive text auto-scaling.

[![Anki Version](https://img.shields.io/badge/Anki-2.1%2B-d946ef?style=flat-square&logo=anki&logoColor=white)](https://apps.ankiweb.net/)
[![AnkiDroid](https://img.shields.io/badge/AnkiDroid-Compatible-10b981?style=flat-square&logo=android&logoColor=white)](https://github.com/ankidroid/Anki-Android)
[![Style](https://img.shields.io/badge/Style-Neon_Minimalism-06b6d4?style=flat-square)](#)

---

## ✨ Features

* 🤍 **Cyber-Minimalism:** A clean, pure-white card background designed to eliminate visual clutter and maximize long-term study focus.
* ⚡️ **Neon Accent Signifiers:** Vivid cyan, purple, and green UI markers for instant visual hierarchy and immediate feedback processing.
* 📏 **JS Auto-Scale Engine:** A lightweight JavaScript algorithm that dynamically shrinks the answer font size if the text is too long, guaranteeing it never breaks the neon border on smaller screens.
* 📐 **MathJax & LaTeX Ready:** Seamless integration for mathematical expressions, rendered with a dedicated soft neon-purple glow.
* 📱 **Cross-Platform Responsive:** Pixel-perfect adaptation engineered for mobile displays (AnkiDroid/AnkiMobile) and Desktop clients alike.

---

## 🛠️ Tech Stack & Architecture

* **Frontend Structure:** HTML5 (Semantic architecture to ensure lightweight DOM parsing).
* **Styling & Layout:** CSS3 (Utilizes CSS Custom Variables for modular theme adjustments; Flexbox/Grid for robust component scaling).
* **Dynamic Logic:** Vanilla JavaScript (Zero dependencies; engineered to run efficiently inside Anki's restrictive internal webview environments).

### How the Auto-Scale Engine Works
To maintain strict UI boundaries without clipping text on ultra-compact mobile screens, the theme runs a real-time layout calculation:
1. The script monitors the target answer container and evaluates its `scrollWidth` against the layout's actual `clientWidth`.
2. If `scrollWidth > clientWidth`, a deterministic `while` loop systematically decreases the element's `fontSize` by increments of `1px`.
3. The loop terminates the moment the text fits perfectly inside the bounding box, preventing layout shifts or overflow bugs.

---

## 🚀 Performance Optimization

* **Zero External Dependencies:** No heavy libraries (like jQuery) or external web fonts are requested. The theme relies strictly on native system fonts (`San Francisco` / `Roboto`) ensuring instantaneous, **100% offline functionality**.
* **Render Pipeline Efficiency:** The CSS structure is optimized to prevent layout thrashing, minimizing continuous Reflow and Repaint cycles inside mobile webviews.

---

## 📸 Screenshots

| Front Template | Back Template (Answer) |
| :---: | :---: |
| <img src="assets/front_preview.png" width="320" alt="Front Preview"> | <img src="assets/back_preview.png" width="320" alt="Back Preview"> |

---

## 📦 Installation

### Option A: The Fast Route (Recommended)
1. Download the pre-configured **`Neon_Light_Theme.apkg`** from the [Releases](#) section.
2. Import it into your Anki Desktop or AnkiDroid app. It will automatically generate the pre-styled card type for you.

### Option B: Manual Setup
If you prefer configuring your existing note types manually:

1. **Styling (CSS):** Copy the entire payload from [`Style_AnkiDroid.css`](./Style_AnkiDroid.css) and paste it into the **Styling** field of your Card Layout options.
2. **Front Template:** Copy the structure from [`Front_AnkiDroid.html`](./Front_AnkiDroid.html) and paste it into the **Front Template** field.
3. **Back Template:** Copy the logic from [`Back_AnkiDroid.html`](./Back_AnkiDroid.html) and paste it into the **Back Template** field.

---

## 🎨 Customization

You can dynamically adjust the core identity of the theme by altering the global variables declared at the absolute top of your [`Style_AnkiDroid.css`](./Style_AnkiDroid.css) file:

```css
:root {
  --neon-cyan: #06b6d4;    /* Primary card border glow */
  --neon-purple: #d946ef;  /* Equations & MathJax accent color */
  --neon-green: #10b981;   /* Correct answer / success feedback */
}
