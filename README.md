# ⚡️ AnkiDroid Neon Light Theme

> **An ultra-clean, high-performance minimalist theme for Anki and AnkiDroid featuring CSS3 custom properties, dynamic client-side font scaling, and optimized MathJax typesetting.**

[![Anki Version](https://img.shields.io/badge/Anki-2.1%2B-d946ef?style=flat-square&logo=anki&logoColor=white)](https://apps.ankiweb.net/)
[![AnkiDroid](https://img.shields.io/badge/AnkiDroid-Compatible-10b981?style=flat-square&logo=android&logoColor=white)](https://github.com/ankidroid/Anki-Android)
[![Language](https://img.shields.io/badge/Language-HTML5%20%2F%20CSS3%20%2F%20JS-06b6d4?style=flat-square)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)

---

## 🚀 Project Overview

This repository provides a lightweight, production-ready frontend template designed to optimize active recall and spaced repetition interfaces within **Anki** and **AnkiDroid**. By combining modern web technologies (HTML5, CSS3, ES6 JavaScript), this theme delivers an distraction-free visual environment accented by vibrant, high-contrast neon highlights. 

Additionally, it implements dynamic DOM text measurement algorithms to solve rendering and text-overflow issues on mobile viewports.

---

## ✨ Features & Architecture

* 🤍 **Cyber-Minimalist Design:** Utilizes a high-contrast white card-container to eliminate cognitive load and maximize user focus during long study sessions.
* 📏 **Dynamic Text Auto-Scaling:** Integrates an active ES6 JavaScript micro-engine on the back card template. The script measures the textual length of the answer dynamically, applying step-down font sizes to prevent layout breaking or text-overflow on smaller mobile viewports.
* 📐 **MathJax & LaTeX Engine Integration:** Explicit styling override hooks designed for mathematical rendering, utilizing deep glow text shadows to highlight formulas without sacrificing legibility.
* 📱 **Viewport Agnostic (Responsive):** Styled from the ground up using modern CSS flexible box models (`Flexbox`), ensuring consistent rendering across Desktop clients, tablets, and smartphones.

---

## 📂 Repository Structure

```directory
AnkiDroid_Stylization/
├── Front_AnkiDroid.html   # Front card HTML template structure
├── Back_AnkiDroid.html    # Back card template incorporating the auto-scale script
├── Style_AnkiDroid.css    # Centralized stylesheet using CSS variables
├── LICENSE                # MIT License
└── assets/                # Directory containing preview assets
    ├── front_preview.png
    └── back_preview.png
