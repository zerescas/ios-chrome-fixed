# Chrome iOS Scrolling Bug Reproduction

This project demonstrates a rendering bug in **Google Chrome on iOS**, where a `position: fixed` bottom element (e.g. mobile navbar) scrolls out of view despite being fixed.

<details>
    <summary>Screenshot</summary>
  
  ![image](https://github.com/user-attachments/assets/64e84a1a-025e-4021-b3bd-2af9ea15636d)   
</details>

## 🔍 Problem

On some versions of **Chrome on iOS**, the browser allows scrolling beyond the actual content height. As a result, elements like a sticky header or fixed bottom navbar become misplaced.

Specifically:
- The **`mobile_navbar`** (positioned with `fixed; bottom: 0;`) scrolls up.
- The page seems to have an **artificially doubled height**.
- This does **not** occur in Safari or on Android.

## 📂 Files

- `index.html` — A simple page with a fixed header and fixed bottom navbar.
- `style.css` — Minimal styles to reproduce the issue.
- `/img/450px-Itoddlers-btfo.gif` — An image to fill the page with contents.

## 🧪 Reproduction Steps

1. Open `index.html` on **Chrome iOS**.
2. Scroll the page downward.
3. Observe that the bottom navbar (`mobile_navbar`) scrolls out of view, even though it’s `position: fixed`.

## ✅ Works As Expected

- Safari iOS (except **Bug Appears On** below)
- Chrome Android
- Desktop Chrome

## ❌ Bug Appears On

Confirmed on:
- iPhone 15 Pro, iOS 18.4.1, Chrome 136.0.7103.91
- iPad Air 5, iPadOS 18.3.2, Chrome 136.0.7103.91
