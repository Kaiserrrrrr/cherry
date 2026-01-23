# 🍒 Cherry

**A native, zero-config optimization engine for the modern web.**

Cherry.js is a "healing" library designed to bridge the gap between semantic design and technical performance. It identifies common accessibility gaps, SEO omissions, and performance bottlenecks (like Cumulative Layout Shift) and patches them at runtime during browser idle periods.

## ❓ Why Cherry?

In modern web development, there is often a massive gap between a **beautiful design** and a **technically sound** document. Even with a perfect CSS framework it is easy to forget a single `alt` tag, a `width` attribute, or a proper heading hierarchy.

Cherry.js was built on the principle of **"In-Flight Repair"**:

* **Zero Technical Debt:** You don't have to go back and manually edit thousands of lines of legacy HTML to fix a low contrast ratio or a missing ARIA label.
* **Performance Without Effort:** By utilizing `requestIdleCallback`, Cherry.js ensures that optimization never comes at the cost of the main thread. It works when the browser is resting.
* **Designer Friendly:** It allows designers to focus on aesthetics while the engine ensures those aesthetics meet WCAG and Core Web Vitals standards.

Instead of just telling you what is wrong in a console report, Cherry.js simply makes it right.

---

## 🚀 Installation

**CDN** (*recommended*):

1. Simply add this in your `<head>` tag:

    ```html
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/Kaiserrrrrr/cherry/dist/cherry.min.js" type="text/css">
    ```

**Manually**:

1. Download the file:

    ```bash
    wget "https://cdn.jsdelivr.net/gh/Kaiserrrrrr/cherry/dist/cherry.min.js"
    ```

    **OR** download directly:
    [blossom](https://cdn.jsdelivr.net/gh/Kaiserrrrrr/cherry/dist/cherry.min.js)

2. Link it from HTML:

    ```html
    <link rel="stylesheet" href="cherry.min.js" type="text/css">
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
&copy; Cherry 2026. Code released under the [MIT license](https://github.com/Kaiserrrrrr/cherry/blob/master/LICENSE).

---
Built with 🍒 and Blossom.
