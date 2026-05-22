# ESHOP — frontend

> A responsive, component-driven e-commerce frontend built with React 18, Vite, and Tailwind CSS — exploring UI composition patterns, dark mode theming, and scroll-driven animation.

---

## Badges

![React](https://img.shields.io/badge/React-18-blue?style=for-the-badge&logo=react)
![Vite](https://img.shields.io/badge/Vite-6-purple?style=for-the-badge&logo=vite)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-3.4-blue?style=for-the-badge&logo=tailwindcss)
![Status](https://img.shields.io/badge/Status-Learning%20Project-yellow?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen?style=for-the-badge)

---


# About The Project

ESHOP is a frontend storefront prototype for a consumer electronics retailer.

It was built as a deliberate exercise in:

- React component architecture
- Utility-first CSS design
- Client-side UX patterns
- Theme persistence
- Scroll-driven animations
- Build tooling exploration

The project includes:

- Carousel hero section
- Product category grids
- Promotional banners
- Product cards
- Blog sections
- Brand partner strip
- Modal order popup
- Dark mode support

Dark mode is implemented using Tailwind's class strategy with persistence via `localStorage`.

Animations are powered by AOS (Animate On Scroll), which internally uses the browser's `IntersectionObserver` API.

---

# Live Demo

| Resource | Link |
|---|---|
| Frontend | [View Demo](https://responsive-ecommerce-website-omega.vercel.app/) |

> To deploy:
>
> ```bash
> npm run build
> ```
>
> Upload the generated `dist/` folder to:
>
> - Vercel
> - Netlify
> - GitHub Pages

---

# Project Type

Frontend UI Prototype — Single-Page Client-Side Rendered React Application

---

# Project Status

**Experimental Prototype / Learning Project**

This repository successfully served its purpose as a practical exploration of:

- React component architecture
- Tailwind CSS workflows
- Vite build tooling
- Client-side state handling
- Dark mode implementation
- Scroll-based UI animation

The project is complete as a learning artifact.  
Known issues and architectural improvements are documented below.

---

# Why I Built This

I wanted practical experience with frontend engineering patterns commonly used in production systems:

- Component composition
- Tailwind CSS JIT workflows
- React hooks behavior
- Dark mode persistence
- Modern build tooling

The project became a way to understand how frontend architectural decisions behave in real implementations — not just tutorials.

---

# Features

## Core UI Features

- Responsive hero carousel
- Product category grids
- Promotional banners
- Product cards
- Blog grid
- Brand partner strip
- Modal order popup

---

## Engineering Features

- Dark mode toggle with `localStorage` persistence
- Scroll-triggered animations using AOS
- Tailwind custom design token system
- Reusable UI atoms:
  - Button
  - Heading
  - ProductCard
  - DarkMode

---

# Tech Stack

## Frontend

| Technology | Version | Purpose |
|---|---|---|
| React | 18.3.1 | Component-based UI |
| Vite | 6.x | Development/build tooling |
| Tailwind CSS | 3.4.17 | Utility-first CSS |
| AOS | 2.3.4 | Scroll-triggered animations |
| react-slick | 0.30.3 | Carousel implementation |
| slick-carousel | 1.8.1 | Carousel styles |
| react-icons | 5.5.0 | SVG icon components |

---

## Intentional Scope Boundaries

| Missing Layer | Why Absent | Production Alternative |
|---|---|---|
| Backend/API | Frontend learning focus | Node.js / Express |
| Database | No dynamic data | PostgreSQL + Prisma |
| Authentication | No user accounts | NextAuth.js / Clerk |
| State Management | Minimal shared state | Zustand / Redux Toolkit |
| Router | Single-page application | React Router v6 |
| Testing | Future scope | Vitest + Testing Library |

---

# Architecture

This is a Client-Side Rendered (CSR) Single Page Application.

There is:

- No server
- No API
- No build-time data fetching

---

## Application Flow

```text
Browser
  │
  └─► index.html
        │
        └─► main.jsx
              │
              └─► createRoot(<App />)
                    │
                    ├── Navbar
                    ├── Hero
                    ├── Category
                    ├── Services
                    ├── Banner
                    ├── Product
                    ├── Blogs
                    ├── Partner
                    ├── Footer
                    └── Popup
```

---

# Folder Structure

```text
ecommerce/
├── index.html
├── vite.config.js
├── tailwind.config.js
├── postcss.config.js
├── eslint.config.js
├── package.json
│
└── src/
    ├── main.jsx
    ├── App.jsx
    ├── index.css
    ├── App.css
    ├── Popup.jsx
    │
    └── components/
        └── Navbar/
            ├── Navbar.jsx
            ├── DarkMode.jsx
            ├── Hero.jsx
            ├── Category.jsx
            ├── Category2.jsx
            ├── Services.jsx
            ├── Banner.jsx
            ├── Product.jsx
            ├── ProductCard.jsx
            ├── Blogs.jsx
            ├── Partner.jsx
            ├── Footer.jsx
            ├── Heading.jsx
            └── Button.jsx
```

> Current structure is tutorial-derived and intentionally documented as technical debt.

---

# Getting Started

## Prerequisites

- Node.js >= 18
- npm >= 8

---

## Installation

```bash
# Clone repository
git clone https://github.com/yourusername/eshop-react-storefront.git

# Enter project
cd eshop-react-storefront/ecommerce

# Install dependencies
npm install

# Start dev server
npm run dev
```

---

## Build for Production

```bash
npm run build
```

Output is generated in:

```text
dist/
```

---

## Preview Production Build

```bash
npm run preview
```

---

## Lint

```bash
npm run lint
```

---

# Usage

| Feature | Interaction |
|---|---|
| Order Popup | Click cart icon or CTA button |
| Dark Mode | Toggle via navbar switch |
| Product Browsing | Scroll and hover cards |
| Animations | Triggered on scroll via AOS |

---

# Screenshots

| Section | Preview |
|---|---|
| Hero Carousel | <img width="1897" height="866" alt="Screenshot 2026-05-22 230449" src="https://github.com/user-attachments/assets/6e65018a-88a7-4e0d-8c56-0cc56155ca95" /> |
| Category Grid | <img width="1900" height="867" alt="Screenshot 2026-05-22 230514" src="https://github.com/user-attachments/assets/6d9e8eeb-a418-4b78-93f7-9e282ecc53e9" />|
| Product Section | <img width="1901" height="869" alt="Screenshot 2026-05-22 230525" src="https://github.com/user-attachments/assets/2861ce2e-7bc6-49af-bf96-563fbde527e4" />|
| Dark Mode | <img width="1893" height="862" alt="Screenshot 2026-05-22 230537" src="https://github.com/user-attachments/assets/31e8f04c-8bca-4834-977b-5583d4f0fe94" /> |
| Order Popup | <img width="373" height="292" alt="Screenshot 2026-05-22 230553" src="https://github.com/user-attachments/assets/2f75dbb2-c10a-47d2-89b3-0e126d4a8121" /> |

---

# Performance Considerations

## Optimized Areas

- Tailwind JIT CSS generation
- Vite production bundling
- Rollup tree-shaking
- Hashed asset filenames
- IntersectionObserver-based animations

---

## Known Bottlenecks

| Issue | Impact |
|---|---|
| No image optimisation | Slower LCP + CLS |
| No lazy loading | Higher initial load |
| No React.memo | Unnecessary re-renders |
| AOS layout shifts | Potential CLS |
| react-slick DOM cloning | Additional hidden DOM nodes |

---

# Security Considerations

## Current Posture

- React escapes JSX by default
- No `dangerouslySetInnerHTML`
- Minimal localStorage usage
- No backend attack surface

---

## Future Backend Requirements

- CSRF protection
- httpOnly cookies
- Input sanitisation
- Rate limiting
- CSP headers

---

# Tradeoffs & Limitations

| Decision | Tradeoff |
|---|---|
| CSR only | Poor SEO |
| Hardcoded data | No scalability |
| react-slick | Older architecture |
| Prop drilling | Limited scalability |
| AOS | Less React-native than Framer Motion |
| No TypeScript | Reduced type safety |
| Tailwind-only | No design-system layer |

---

# Known Issues

| Issue | File | Severity | Status |
|---|---|---|---|
| Missing dependency array | DarkMode.jsx | Medium | Open |
| Input type typos | Popup.jsx | Medium | Open |
| Stale closure risk | App.jsx | Low | Open |
| Missing rel="noopener noreferrer" | Footer.jsx | Low | Open |
| Duplicate IDs | Navbar.jsx | Low | Open |
| Duplicate color tokens | tailwind.config.js | Low | Open |
| Unused App.css | App.css | Low | Open |
| All components in Navbar folder | Structure | Medium | Open |
| Broken inline style | Hero.jsx | Low | Open |

---

# Technical Debt

## Structural

- All components inside `components/Navbar/`
- Data co-located with components

---

# Challenges Faced

## 1. Dark Mode Flicker

Understanding synchronous `localStorage` reads before first render.

## 2. AOS Lifecycle Integration

Ensuring animations initialize after DOM mount.

## 3. React StrictMode + Carousel Timers

Understanding double-invoked effects in development.

## 4. Tailwind Class-Based Theming

Balancing imperative DOM manipulation with React's declarative model.

---

# What I Learned

## React Hooks

- Dependency arrays matter
- Functional state updates prevent stale closures
- Lazy initialization prevents unnecessary synchronous work

---

## CSS Architecture

- Tailwind JIT scanning
- Dark mode class strategy
- Tailwind component layers

---

# Contributing

Contributions, discussions, and improvements are welcome.

```bash
# Fork repository

# Create branch
git checkout -b fix/feature-name

# Commit changes
git commit -m "fix: description"

# Push branch
git push origin fix/feature-name
```

Please follow Conventional Commits.

---

# License

Distributed under the MIT License.  
See `LICENSE` for details.

---

# Contact

**Heramb Chaudhari**

[![GitHub](https://img.shields.io/badge/GitHub-Heramb1221-black?style=for-the-badge&logo=github)](https://github.com/Heramb1221)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Heramb%20Chaudhari-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/heramb-chaudhari)

[![Email](https://img.shields.io/badge/Email-hchaudhari1221%40gmail.com-red?style=for-the-badge&logo=gmail)](mailto:hchaudhari1221@gmail.com)
