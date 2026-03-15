# ⚡ AWAM TECH — Pure CSS Web Assignment

> **CSS3333 | Individual Assignment | University of Technology Sarawak**  
> Student: Chiu Siew Seng | Matric: BCS24020043 | Date: 15 March 2026

A fully interactive, JavaScript-free web project built using only **HTML5 & CSS3**, demonstrating advanced CSS architecture, state machines, 3D transforms, and animation systems.

---

## 📁 Project Structure

```
/
├── Question%201.html    # One-Page Computer Sale Website (AWAM TECH)
└── Question%202.html    # Interactive Digital Name Card (AWAM TECH Cafe)
```

---

## 🖥️ Question 1 — One-Page Computer Sale Website

A fully functional Single Page Application (SPA) for **AWAM TECH**, a fictional cyberpunk hardware retailer — built with zero JavaScript.

### ✨ Features

| Feature | CSS Technique Used |
|---|---|
| 4-page navigation (Home / Products / About / Contact) | `radio` inputs + General Sibling Combinator (`~`) |
| Shopping cart with live item count badge | CSS Counters (`counter-increment`, `counter-reset`) |
| Slide-out cart drawer | `checkbox` toggle + `position: fixed` + `transition` |
| Product category filtering (All / Laptops / Desktops / Accessories) | `radio` inputs + `:not()` selector |
| Animated countdown timer | `@keyframes` with `step-end` timing + `content` property |
| Add-to-cart state change (button turns green ✓) | `:checked` + sibling combinator |
| Pulsing discount badges | `@keyframes pulse-badge` |
| Responsive layout | CSS Grid + Flexbox, mobile-first |

### 🎨 Design System

```css
:root {
  --bg-dark:    #0b0c10;   /* Deep space background */
  --bg-card:    #1f2833;   /* Card surface */
  --brand-cyan: #00d2ff;   /* Primary action / neon accent */
  --brand-red:  #ff4757;   /* Urgency / sales / alerts */
  --brand-green:#2ed573;   /* Success / confirmed state */
  --text-light: #c5c6c7;   /* Body text */
}
```

**Aesthetic:** Cyberpunk / Hard Sci-Fi — dark immersive backgrounds with neon accents, uppercase sans-serif headings, and responsive grid layouts.

### 🔧 Pure CSS State Machine — How It Works

```
[Hidden Radio Inputs] ──checked──▶ CSS ~ Combinator ──▶ Show/Hide Page Sections
[Hidden Checkboxes]   ──checked──▶ counter-increment  ──▶ Cart Badge Count Updates
[Hidden Checkboxes]   ──checked──▶ CSS ~ Combinator  ──▶ Cart Items Appear in Drawer
```

### 📄 Pages

1. **Home** — Hero banner, Flash Sale strip with countdown, Featured Products grid, Who Are We teaser, Hot Deals section, Customer Testimonials
2. **Products** — Full 6-product catalog with sidebar category filter and search bar UI
3. **About** — Company story, mission & vision, AWAM TECH Cyber Cafe subsidiary section
4. **Contact** — HQ info, map mockup, contact form

---

## 💳 Question 2 — Interactive Digital Name Card

A **3D flip business card** for AWAM TECH Cyber Cafe & E-Sports, thematically connected to Question 1.

### ✨ Features

- **3D Flip on Hover** — CSS `perspective`, `transform-style: preserve-3d`, `rotateY(180deg)`
- **Holographic Scanline Overlay** — `repeating-linear-gradient` pseudo-element
- **Neon Glow Effects** — `text-shadow` and `box-shadow` for cyberpunk atmosphere
- **Sci-Fi Grid Background** — `background-image` with layered linear gradients
- **Responsive** — adapts to small screens via `@media` query

### 🃏 Card Information

| Side | Content |
|---|---|
| **Front** | Employee name (Chiu Siew Seng), Title (Cyber Operations Manager), Phone, Email |
| **Back** | Company address (Sibu), Website, Working hours, HQ address (Kuching) |

### 🔧 3D Flip Implementation

```css
/* Parent sets the 3D space */
.card-container { perspective: 1500px; }

/* Child preserves 3D for both faces */
.card-inner { transform-style: preserve-3d; transition: transform 0.8s; }

/* Back face pre-rotated */
.card-back { transform: rotateY(180deg); }

/* Hover triggers the flip */
.card-container:hover .card-inner { transform: rotateY(180deg); }

/* Hide faces when facing away */
.card-front, .card-back { backface-visibility: hidden; }
```

---

## 🚀 Getting Started

No build tools or dependencies needed. Open directly in any modern browser.

```bash
# Clone the repository
git clone https://github.com/your-username/awam-tech-css-assignment.git

# Open Question 1
open "Question%201.html"

# Open Question 2
open "Question%202.html"
```

Or simply double-click either `.html` file to run locally.

---

## 🛠️ Technology Stack

| Technology | Version | Usage |
|---|---|---|
| HTML5 | — | Semantic structure, form elements as state controllers |
| CSS3 | — | All layout, animations, interactivity, state management |
| JavaScript | ❌ None | Strictly not used (assignment constraint) |

---

## 📸 Screenshots

| Page | Preview |
|---|---|
| Home — Hero + Flash Sale | (See report Figure 2.2) |
| Products — Catalog + Filter | *(See report Figure 2.2)* |
| Shopping Cart Drawer | *(See report Figure 2.3)* |
| Name Card — Front | *(See report Figure 3.1)* |
| Name Card — Back (after flip) | *(See report Figure 3.2)* |

---

## 📚 Key Concepts Demonstrated

- **CSS-only SPA routing** using radio button state machines
- **CSS Counters** for dynamic UI state (cart badge)
- **`@keyframes` countdown timer** using `step-end` and the `content` property
- **3D CSS transforms** with `preserve-3d` and `backface-visibility`
- **CSS Grid & Flexbox** for fully responsive layouts
- **Pseudo-element overlays** for holographic visual effects

---

## 👤 Author

**Chiu Siew Seng**  
Bachelor of Computer Science (BSc)  
University of Technology Sarawak  
Course: CSS3333 | Lecturer: Tanalachimi A/P Ganapathy

---

> *"This assignment drastically expanded the capability to implement advanced user interactions, modern UI/UX design principles and robust CSS architectures."*
