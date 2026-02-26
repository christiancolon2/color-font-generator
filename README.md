# 🎨 Aesthetic Generator

A single-file, production-quality aesthetic generator built with **HTML5, CSS3, and Vanilla JavaScript**.

Generate cohesive color palettes and font pairings with:

- 🎯 Reproducible seed-based generation
- 🔒 Role-based locking
- 🎨 Palette bias controls (base color + saturation tuning)
- 🔤 Curated font pairings
- 📋 One-click CSS export
- ⭐ Local favorites system
- ♿ Built-in WCAG contrast checks
- 🌗 Auto / Light / Dark theme support

No frameworks. No build tools. No dependencies.

---

## ✅ What This Project Does

This app generates _sensible_ UI aesthetics (not random neon chaos):

- A full UI-ready palette with roles (`background`, `surface`, `accent`, etc.)
- A font pairing (heading + body)
- A realistic SaaS-style live preview
- Accessibility checks to keep palettes readable
- Local favorites so you can save and reuse combos

---

## 🚀 Features

### 1) Seed-Based Generation (Reproducible)

Every palette + font pairing is generated from a **numeric seed**, meaning:

- Same seed = same output (as long as locks/bias are the same)
- Great for sharing combos
- Great for returning to previous results

**Controls included:**

- Seed input
- Copy seed
- Copy share URL
- New seed button

---

### 2) Palette Bias Controls (Influence the Palette)

Influence the generator while still keeping it “auto”.

**Base Color Picker**

- Sets the main hue direction used for backgrounds/surfaces
- Useful when starting from a brand color

**Saturation Bias Slider**

- Controls overall vibrancy
- Negative = calmer / more neutral
- Positive = more vibrant

**Lock Base Hue**

- Forces the generator to always keep the chosen hue

**Reset Bias**

- Resets base color + saturation + hue lock

---

### 3) Role-Based Palette System

The palette is generated into roles:

- `background`
- `surface`
- `primary`
- `secondary`
- `accent`
- `text`
- `muted`

Each role supports:

- 🔒 Locking
- 📋 Copying individual hex values
- Visual swatch preview

---

### 4) One-Click Exports

Copy outputs for real project use:

- **Copy All Colors** → quick list for notes/docs
- **Copy CSS Variables** → `:root { --role: #HEX; }`
- Font CSS helpers:
  - Copy heading font stack
  - Copy body font stack
  - Copy example CSS block

---

### 5) Font Pairing Generator

Generates:

- **Heading font**
- **Body font**

Supports:

- Lock heading font
- Lock body font
- Copy font stacks

Uses a curated pool of safe, modern fonts (with offline fallbacks).

---

### 6) Accessibility Checks (WCAG)

Built-in contrast checks for:

- Text on background
- Text on surface
- Button text on accent

Shows results as:

- **AAA**
- **AA**
- **Near**
- **Fail**

This helps avoid generating palettes that look good but are unreadable.

---

### 7) Favorites (localStorage)

Save combinations directly in the app:

Each favorite stores:

- Seed
- Palette roles
- Font pairing
- Timestamp
- Optional name

Supports:

- Load favorite
- Delete favorite
- Clear all favorites

Favorites persist via `localStorage` on the current device/browser.

---

### 8) Theme Toggle (App Chrome)

The app chrome (UI outside the preview) supports:

- **Auto** (follows system preference)
- **Dark**
- **Light**

This is separate from the generated preview theme.

---

## 🧠 How It Works (High-Level)

- Uses a deterministic PRNG (Mulberry32) for reproducible generation
- Generates a palette with constraints (background/surface calm, accent strong)
- Applies contrast adjustments to keep readability sane
- Generates fonts from a curated list
- Stores state in `localStorage`:
  - last used combo
  - favorites
  - theme
  - palette bias settings

---

## 📁 Project Structure

````txt
.
├── index.html
├── favicon.png
└── README.md

## 🔧 Setup / Run Locally

No install required.

### Option 1: Open directly
- Double click `index.html`

### Option 2: Simple local server (recommended)
This avoids some browser restrictions in certain environments.

```bash
# Python 3
python -m http.server 8000
Then open:
http://localhost:8000

## 🌍 Deploy as a Static Site

This is designed for static hosting:

- GitHub Pages
- Netlify
- Vercel
- Cloudflare Pages
- Any static web host

No build step, no backend.

---

## 🎯 Why This Is a Strong Portfolio Project

This project demonstrates:

- Clean UI layout + modern component styling (no frameworks)
- Thoughtful UX (locks, export, favorites, seed sharing)
- Deterministic stateful JS logic
- Accessibility awareness (contrast checks)
- Practical design-system thinking (roles + preview kit)
- Production-level attention to details (persistence, keyboard shortcut, theming)

---

## ⌨️ Keyboard Shortcuts

- **Cmd/Ctrl + Enter** → regenerate unlocked items

---

## 🛣️ Future Improvements (Optional)

- Export downloadable CSS file
- Export JSON theme tokens
- Generate Tailwind config from palette
- Generate design tokens for Figma
- Animate palette transitions
- Add “accent-driven” mode (picker controls accent hue instead of base hue)
- Add saved bias presets

---

## 📄 License

MIT — free to use, modify, and ship.
````
