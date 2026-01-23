# 🍒 cherry.js

**A native, zero-config optimization engine for the modern web.**

Cherry.js is a "healing" library designed to bridge the gap between semantic design and technical performance. It identifies common accessibility gaps, SEO omissions, and performance bottlenecks (like Cumulative Layout Shift) and patches them at runtime during browser idle periods.

---

## 🚀 Quick Start

Cherry.js is designed to be a "drop-in and forget" solution. No configuration objects or API codes are required.

### 1. Installation
Include the script in your `<head>` to allow it to monitor the DOM early:

```html
<script src="<script src="https://cdn.jsdelivr.net/gh/Kaiserrrrrr/cherry/dist/cherry.min.js"></script>"></script>
```

### 2. Usage
Once loaded, the engine initializes an `IdleCallback`. It waits for the browser to be "bored" before performing DOM surgery, ensuring that it never contributes to Total Blocking Time (TBT).

## 🛠 What it Fixes

| Module | Description |
| :--- | :--- |
| **Accessibility Patch** | Auto-generates `aria-labels` for icon-only elements and repairs broken `tabindex` hierarchies. |
| **CLS Patch** | Identifies images/media missing dimensions and injects them to prevent Cumulative Layout Shift. |
| **SEO Patch** | Ensures document contains a single `h1` and generates missing meta-descriptors dynamically. |
| **Security Patch** | Automatically patches `target="_blank"` links with `rel="noopener"` to prevent tab-nabbing. |

---

## 🎨 Built for Blossom

Cherry.js is the definitive technical companion for **[Blossom.css](https://github.com/Kaiserrrrrr/blossom)**. While Blossom provides the visual framework and semantic baseline, Cherry handles the technical enforcement:

* **Automatic Centering:** Designed to respect Blossom's `max-width` and `margin: auto` structures without causing layout jumps.
* **Theme Integration:** Uses Blossom's native CSS variables (`--bg-color`, `--text-color`, `--btn-bg`) for any injected UI elements.
* **Dark Mode Ready:** Inherits `@media (prefers-color-scheme: dark)` styling directly from the Blossom root.

---

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.

---
Built with 🍒 and Blossom.
