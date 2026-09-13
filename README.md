# 💌 Interactive Letter

An elegant, deeply emotional, and interactive digital love letter built with pure **HTML5, CSS3, and Vanilla JavaScript**. Designed with a soft rose-tinted stationery aesthetic, real-time typewriter typography, gesture-based page swiping, and immersive romantic micro-interactions.

---

## ✨ Features

- **✉️ Interactive Envelope Unfolding**  
  Click to open the digital seal and watch the envelope flap gracefully open with 3D CSS transforms as the teaser note glides up.

- **📄 Realistic A4 Letter Paper Aesthetic**  
  Crafted like genuine stationery with warm cream paper (`#fffdf8`), red left margin rules, faint notebook guidelines, and soft ambient drop shadows.

- **✍️ Real-Time Live Typewriter Engine**  
  Words type themselves onto the parchment character-by-character on both Page 1 and Page 2.
  - *Smooth timing*: Begins after the page-slide transition smoothly settles.
  - *Fast reading*: Double-click anywhere on the page to instantly reveal all text.

- **🖱️ Drag & Swipe Page Navigation**  
  Navigate naturally between pages using mouse click-and-drag or touch swipe gestures, complete with smooth spring transitions and arrow controls.

- **❤️ Dynamic Love Progress Bar**  
  A beating heart icon (`❤️` → `💖`) glides across an accent bar, filling from **0% to 100%** as you turn from Page 1 to Page 2.

- **✨ Sparkle & Heart Cursor Trail**  
  A soft, ethereal trail of floating micro-hearts and sparkles (`❤️`, `💕`, `💗`, `💖`, `🌸`, `✨`) follows cursor movement across the screen.

- **🌹 Grand Finale & Digital Wax Seal**  
  Concludes with a heartfelt sacred vow, formal romantic sign-off (`— My Love ❤️`), a crimson wax seal badge (`💌 Sealed With Eternal Love 💌`), and an interactive *"Seal & Keep Close to My Heart"* button that folds the letter back into the envelope.

- **📱 Fully Responsive Design**  
  Optimized for screens of all sizes — mobile phones, tablets, and desktop displays.

---

## 🚀 Quick Start

This project is completely self-contained with **zero dependencies** or build steps.

### Option 1: Open Directly in Browser
Simply double-click `index.html` or drag it into any modern web browser (Chrome, Safari, Edge, Firefox).

### Option 2: Run with a Local Server
Using Python:
```bash
python -m http.server 8000
```
Or using Node.js:
```bash
npx serve .
```
Then navigate to `http://localhost:8000` in your browser.

---

## 🎨 Customization Guide

All styling, content, and scripting live inside [`index.html`](index.html), making personalization easy:

### 1. Changing the Recipient & Dedication
- **Header Pill Badge**:
  ```html
  <span class="name-badge">For My Love 💌</span>
  ```
- **Letter Greeting** (Page 1):
  ```html
  <h1 class="letter-greeting">Dear My Love, 🌹</h1>
  ```

### 2. Customizing the Letter Content
The letter is organized into two swipeable pages inside `.pages-track`:
- **Page 1**: Contains the initial greeting, drop-cap opening paragraph, and devotion prose.
- **Page 2**: Contains the climax, sacred promise box (`.letter-promise`), wax seal, and closing signature (`.letter-signature`).

### 3. Adjusting Typewriter Speed
In the `<script>` section under `startTypewritePage()`:
```javascript
chars.forEach((span) => {
  setTimeout(() => {
    span.classList.add("revealed");
  }, delay);
  delay += 11; // Lower number = faster typing; Higher number = slower typing
});
```

### 4. Customizing Floating Emojis
Update the array in `createHeart()` to use any emojis you like:
```javascript
const icons = ["❤️", "💖", "💕", "💗", "💓", "🌸", "✨"];
```

---

## 📂 Project Structure

```text
Vintage-Valentine-Letter-main/
│
├── index.html       # Complete application (HTML, CSS animations, JavaScript)
├── letter.gif       # Preview animation asset
└── README.md        # Project documentation
```

---

## 🛠️ Built With

- **HTML5** — Semantic structure and accessible markup
- **CSS3** — Custom keyframe animations, radial gradients, CSS transforms, and responsive media queries
- **Vanilla JavaScript** — Gesture physics, touch/drag detection, and typewriter scheduler
- **Google Fonts** — Playfair Display, Cormorant Garamond, and Poppins

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE) — feel free to customize and share it with someone special! 💕
