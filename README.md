# Reinventados Expo Website

## 🔍 Quick Reference: Search Keywords
Use these keywords to quickly jump to specific sections in `index.html` and `style.css`:

| Section | Keyword | Description |
| :--- | :--- | :--- |
| **Global Styles** | `:root` | Colors, fonts, and global variables |
| **Header / Nav** | `.header` | Navigation bar and logo styles |
| **Hero (Top)** | `hero-v3` | The main split-screen entry section |
| **About Event** | `about-section-v3` | "Es el evento más importante..." section |
| **Success Block** | `section-v2-match` | Multi-use sections for "El empresario exitoso" |
| **Speakers** | `speakers-section-v5` | The full-width speaker grid and categories |
| **Target Audience** | `section-dirigido` | "¿A quién va dirigido?" green cards |
| **Experience** | `section-encontrar` | Blue banner and dark green info boxes |
| **Why Participate** | `section-participar` | Red bordered cards with icons |
| **Characteristics** | `section-caracteristicas`| Key traits list and image bento grid |
| **Stories** | `section-historias` | 3-column journalistic story grid |
| **Conecta** | `conecta-section` | Gradient titles and large images |
| **Contact / Footer** | `contact-section-v12` | Founder info and final branding bar |
| **Animations** | `reveal` | Scroll-triggered entrance animations |
| **Mobile Menu** | `mobile-menu` | Sidebar navigation for smaller screens |

---

This is the **Premium Edition** of the Reinventados Expo landing page. It has been engineered for visual excellence, rapid performance, and high conversion, featuring custom integrations of client-provided high-fidelity assets and specific requested journalistic layouts.


## ⚙️ Common Customizations
To modify the site quickly, follow these paths:

*   **Change Logo**: Replace `assets/logo.png`. To change its size, search `.logo img` in `style.css`.
*   **Change Main Colors**: Update the Hex codes in the `:root` section (lines 4-15) of `style.css`.
*   **Change Hero Image**: Replace `assets/hero.png`. It is controlled by the `.hero-right` class.
*   **Update Text**: All text content is located within the `<main>` tag in `index.html`. Each section is clearly commented.
*   **Adjust Header Opacity**: Search for `.header` in `style.css` and modify the `background: rgba(255, 255, 255, 0.85)` value.

---

## 📁 Project Structure

```text
/3
├── assets/         # High-resolution optimized images, icons, and branding
├── index.html      # SEO-semantic structure & core content
├── style.css       # Custom high-fidelity design system (Vanilla CSS3)
├── script.js       # Lightweight interaction logic & reveal animations
└── README.md       # Technical Documentation & Backend Handover
```

## 🚀 Key Design Features

1.  **Historias de Reinventados**: Implemented as a 3-column journalistic grid matching the high-end editorial look of design reference `page 10`.
2.  **Product Integration**: Sections "¿Qué encontrar?" and "¿Por qué participar?" feature full-width asset integration (`section2.png` and `section-1.png`) for maximum impact.
3.  **Vibrant Dirigido Cards**: A solid green card system implemented to match the specific color targets and rounding of design reference `page 6`.
4.  **Premium Contact Module**: A 2-column "Card" design inspired by Version 1, providing a luxurious container for founder info and integrated mapping.

## 🛠 Backend Developer Integration Guide

If you are a backend developer taking over this project for CRM integration or dynamic content, please note the following:

### 1. Form & Lead Generation

The contact module currently displays founder info and a map. To add a lead capture form:

- **Location**: Insert your `<form>` element inside the `.contact-info-v3` div in `index.html`.
- **Styling**: Use the existing design variables (e.g., `var(--primary-cyan)`) to ensure new inputs match the premium aesthetic.

### 2. Map Configuration

The map is implemented via a Google Maps `iframe` located in the `footer-links-side` equivalent block within the Contact Card.

- **Update Location**: Locate the `<iframe>` inside the `.contact-map-mini` container and update the `src` attribute with your client's specific Google Maps embed link.

### 3. Dynamic Section Rendering

If you are pulling **Speakers** or **Stories** from a database:

- **Speakers**: The grid `.speakers-grid` utilizes a circular portal system. Ensure your loop generates the `.speaker-portal` structure for each entry.
- **Stories**: Ensure images remain uncropped by maintaining the `object-fit: contain` and `background: #f1f5f9` logic on the `.story-img-v3` class.

### 4. Configuration & SEO

- **Navigation**: All navigation links are anchor-based (`#inicio`, `#contacto`, etc.). Ensure your routing maintains these fragment identifiers.
- **Favicon**: Remember to upload a specific favicon to the root directory for final branding.
- **Metadata**: Social meta tags (OG tags) should be added to the `<head>` of `index.html` once the final URL is determined.

## 🛠 Technical Details

### 🏗 HTML Architecture

The structure of **Reinventados Expo V3** is built on high-performance, semantic HTML5, ensuring both accessibility and SEO optimization.

- **Semantic Layout**: Utilizes `<header>`, `<main>`, `<section>`, and `<footer>` tags to provide clear document hierarchy.
- **SEO Metadata**: Optimized with descriptive meta tags, viewport settings, and structured titles for better indexing.
- **Asset Integration**: Features 30+ custom-designed assets, optimized for fast loading without sacrificing visual fidelity.
- **Third-Party Libraries**:
  - **Google Fonts**: Anton & Inter for a modern, high-contrast typographic hierarchy.
  - **Lucide Icons**: Scalable vector icons for clean, lightweight interface indicators.
  - **Google Maps**: Integrated mini-map for physical event localization.

### 🎨 CSS & Design System

The visual layer is powered by a custom **Vanilla CSS3** engine, avoiding the overhead of heavy frameworks while maintaining a premium look.

- **CSS Variables**: A centralized design system in `:root` controls the entire palette (`--primary-cyan`, `--primary-teal`, etc.) and shadows (`--shadow-premium`).
- **Advanced Aesthetics**:
  - **Glassmorphism**: Strategic use of `backdrop-filter: blur()` for header and info cards.
  - **Layered Layouts**: Complex positioning (blobs, shapes, and image stacks) to create depth.
  - **Responsive Engine**: A robust set of media queries ensures the "Journalistic Grid" and "Bento Grid" layouts adapt perfectly to mobile, tablet, and desktop.
  - **Micro-interactions**: Smooth transitions on buttons and links using cubic-bezier timing functions.

### ⚡ JavaScript Interactivity

The interactivity is handled by a lightweight `script.js` that focuses on performance and smooth user experience.

- **Intersection Observer**: High-performance scrolling reveal system that triggers animations as sections enter the viewport.
- **Header Dynamics**: Real-time class toggling based on scroll position to maintain visibility and design consistency.
- **Custom Smooth Scroll**: Hand-coded scrolling logic for navigation links that accounts for fixed header offsets.
- **Parallax Micro-effects**: Subtle mouse-move listeners to animate background glows and shapes, creating a dynamic 3D feel.

## 📦 Deployment Instructions

1.  **Shared Hosting**: Upload all contents of the root folder to the `public_html` directory via FTP.
2.  **Netlify/Vercel**: Connect the repository and set the build directory to the root of this folder.
3.  **Assets**: Ensure the `assets/` folder is uploaded as-is, as specific sections depend on exact filename matches (e.g., `section2.png`, `logo.png`).

---

_Developed for Reinventados Expo 2024. Focused on Pixel-Perfection and Growth._
