# ✈️ Wanderlust Travel Agency — Multi-Page Website

A professional, fully responsive multi-page travel agency website built with **HTML5**, **Bootstrap 5.3**, and **custom CSS3**. Designed around a sky-blue and white theme with modern animations, interactive components, and a clean typographic system using Google Fonts.

---

## 📋 Table of Contents

- [Project Overview](#-project-overview)
- [Implemented Features](#-implemented-features)
- [Technologies Used](#-technologies-used)
- [Project Structure](#-project-structure)
- [How to Run](#-how-to-run)
- [Page-by-Page Breakdown](#-page-by-page-breakdown)
- [Screenshots](#-screenshots)
- [Future Improvements](#-future-improvements)
- [Author](#-author)

---

## 🌍 Project Overview

**Wanderlust Travel Agency** is a four-page static website that presents a fictional travel agency. It covers everything a real agency site needs: an immersive homepage, a team-and-values about page, a full-service catalogue with pricing, and a detailed contact page with a validated enquiry form. All pages are interconnected via a shared sticky navbar and identical footer.

The site loads all assets from CDN (no build step required) and uses only vanilla JavaScript for interactivity — making it exam-ready, beginner-friendly, and immediately runnable by opening any HTML file in a browser.

---

## ✅ Implemented Features

### 🔧 Global / Cross-Page
- **Sticky glassmorphic navbar** — `backdrop-filter: blur(12px)`, 97% opaque white, stays fixed on scroll across all four pages
- **Animated nav-link underlines** — CSS `::after` pseudo-element scales in on hover/active
- **"Book a Trip" CTA pill** in the navbar linking to `contact.html`
- **Scroll-triggered reveal animations** — `IntersectionObserver` adds `.visible` to `.reveal` elements, triggering a `fadeInUp` transition as sections enter the viewport
- **Smooth scrolling** — `scroll-behavior: smooth` on the `html` element
- **Back-to-top button** — fixed position, appears after scrolling 400 px, smooth-scrolls to top on click
- **Consistent footer** across all pages with four columns: brand + about blurb, quick links, top destinations, full contact block
- **Footer social icons** — Facebook, Instagram, Twitter, YouTube, LinkedIn (Font Awesome 6)
- **CSS custom properties** — full design token system (`--sky`, `--navy`, `--gold`, `--radius`, `--transition`, `--font-display`, `--font-body`, and more)
- **Responsive layout** — Bootstrap grid + custom breakpoint overrides for mobile, tablet, and desktop
- **Google Fonts** — `Playfair Display` (headings/display) paired with `DM Sans` (body text)

---

### 🏠 Homepage (`index.html`)

#### Hero Section
- Full-viewport hero (`min-height: 92vh`) with an Unsplash travel landscape background
- **`heroZoom` CSS keyframe** — background image gently scales from 1.05 → 1.12 over 20 s on an infinite alternate loop
- Multi-layer gradient overlay (navy → sky) for text legibility
- **"Award-Winning Travel Agency"** glassmorphic badge with compass icon, animated via `fadeInDown`
- Headline **"Explore the *World* with Us"** — italic word in sky blue with an animated growing underline (`lineGrow` keyframe, 1 s delay)
- Tagline paragraph and two CTA buttons: **Explore Packages** and **Our Story**, each with staggered `fadeInUp` delays
- **Hero stats bar** — `50K+ Happy Travelers | 120+ Destinations | 15+ Years Experience` separated by a translucent border
- **Two floating info cards** (desktop only) — animate on a perpetual `float` keyframe (4 s ease-in-out): one showing next departure (Bali — 3 seats left), one showing a 4.9 / 5 star rating

#### Destination Search Bar
- Glassmorphic search card inside the hero (right column)
- **Five input controls**: free-text destination, departure date, return date, travellers select (1 Adult / 2 Adults / 2 Adults + 1 Child / Family 4+), trip type select (Any / Adventure / Beach & Relax / Cultural Tour)
- **"Search Trips"** submit button with sky gradient and lift-on-hover shadow

#### Featured Destinations (4 Cards)
| # | Destination | Badge | Price | Rating |
|---|---|---|---|---|
| 1 | Bali, Indonesia | Bestseller | From $899 | 4.9 ★ (312) |
| 2 | Paris, France | Romantic | From $1,249 | 4.7 ★ (428) |
| 3 | Santorini, Greece | Trending | From $1,599 | 4.9 ★ (257) |
| 4 | Maldives | Luxury | From $2,199 | 5.0 ★ (189) |

Each card contains: Unsplash image (with `scale(1.08)` zoom on hover), category badge, price chip, destination location line, title, short description, star rating with review count, and a **"Book Now"** pill button. The whole card lifts `translateY(-8px)` with an enhanced box-shadow on hover.

#### Why Choose Us Section
Dark navy gradient section with four glassmorphic feature cards, each with a sky-blue icon tile:
1. **100% Safe & Secure** — shield icon
2. **24/7 Expert Support** — headset icon
3. **Best Price Guarantee** — tags icon
4. **Personalized Journeys** — star icon

Cards highlight with a sky-tinted background and lift on hover.

#### Testimonials Carousel
- Bootstrap carousel (`data-bs-ride="carousel"`, `data-bs-interval="5000"`)
- **2 slides × 3 testimonial cards each** (3 visible on desktop, 1 on mobile)
- **6 reviewers total**: Sarah K. (Bali honeymoon), Michael T. (Greece islands), Priya M. (Maldives luxury), James L. (Japan family), Elena V. (Paris anniversary), Tom H. (New Zealand road trip)
- Each card: star rating row, italic quote with large decorative opening quotation mark, reviewer avatar (pravatar.cc), name, and trip label
- Custom pill indicators — active indicator stretches to a wider bar via CSS

#### Call-to-Action Banner
Sky gradient full-width strip with "Ready for Your Next Adventure?" headline and two buttons: **Get Free Quote** (white solid) and **Call Us Now** (outline).

---

### 👥 About Page (`about.html`)

- **Page hero** with breadcrumb trail (`Home › About Us`), clipped bottom edge via `clip-path: ellipse`
- **Story section** — Unsplash mountain image with an overlay badge card ("15+ Years of Excellence"), two story paragraphs, and a five-item credential list:
  - IATA Certified Travel Agency
  - Award-Winning Customer Service (2020–2024)
  - 200+ certified destination specialists worldwide
  - 100% secure online booking with price protection
  - Fully accredited by ASTA & CLIA
- **Stats band** (sky gradient) — `50K+` Travelers · `120+` Destinations · `200+` Team Specialists · `4.9★` Rating
- **Team section** — three cards in a Bootstrap grid:
  | Name | Role |
  |------|------|
  | David Chen | CEO & Founder (visited 95 countries) |
  | Amara Johnson | Head of Experiences (12 yrs luxury travel) |
  | Marco Rivera | Director of Operations |
  Each card has a portrait image (Unsplash), image zoom on card hover, name, role chip, biography, and three social icon links (LinkedIn, Twitter, Instagram)
- **Mission card** (sky gradient) and **Vision card** (navy gradient) — side by side
- **Three value cards** (sky-pale background): Integrity, Sustainability, Excellence

---

### 🛎️ Services Page (`services.html`)

#### 8 Service Cards (2 rows × 4 columns)
| Service | Icon | Key Features |
|---|---|---|
| Flight Booking | `fa-plane-departure` | 500+ airlines, business/economy/first, multi-city, free cancellation 48 h |
| Hotel Reservations | `fa-hotel` | 50,000+ properties, exclusive rates, free breakfast options |
| Car Rentals | `fa-car` | 300+ locations, GPS included, full insurance, 24/7 roadside |
| Tour Packages | `fa-map-marked-alt` | 80+ itineraries, local guides, meals & transfers, custom/private |
| Cruise Packages | `fa-ship` | Caribbean & Mediterranean, shore excursions, dining packages |
| Honeymoon Packages | `fa-heart` | Private villas, couple spa, sunset dining, anniversary perks |
| Adventure Tours | `fa-mountain` | Alpine treks, certified guides, safety equipment, emergency cover |
| Travel Insurance | `fa-shield-halved` | $5M medical, trip cancellation, evacuation, 24/7 hotline |

Each card: Unsplash image (with `scale(1.06)` on hover), **floating icon overlay** (colour switches to navy on card hover), four bullet feature points, **"Learn More"** pill button. Card lifts `translateY(-8px)` and gets a sky-light border on hover.

#### How It Works (4-Step Process)
Numbered circle steps connected by Font Awesome chevron arrows on desktop:
1. Tell Us Your Dream
2. Get Custom Plan
3. Confirm & Pay
4. Start Exploring!

#### Pricing Tiers
| Tier | Price | Duration | Highlight |
|---|---|---|---|
| 🌿 Essential | $599 / person | 7-day trip | Budget-friendly — economy, 3-star, group tours |
| ✈️ Premium | $1,199 / person | 10-day trip | **Most Popular** (gold badge, elevated navy card) — business option, boutique 4-star, private tours, all transfers |
| 👑 Luxury | $2,999 / person | 14-day trip | Ultimate — first class, 5-star villas, personal concierge, all-inclusive dining |

---

### 📬 Contact Page (`contact.html`)

#### Contact Info Card (Navy Gradient, Left Column)
- Office address (New York, NY)
- Phone: `+1 (800) 555-1234` with business hours
- Emails: `hello@wanderlust.travel` and `bookings@wanderlust.travel`
- Working hours block
- Social media links row

#### Enquiry Form (Right Column — 8 Fields + Checkbox)
| Field | Type |
|---|---|
| First Name | Text input (required) |
| Last Name | Text input (required) |
| Email Address | Email input (required) |
| Phone Number | Tel input (optional) |
| Destination | Select — 8 options |
| Travel Type | Select — 7 options |
| Travel Date | Date picker |
| Budget per person | Select — 5 ranges ($500 → $5,000+) |
| Message | Textarea (5 rows) |
| Newsletter opt-in | Checkbox |

**Form validation & submission:** JavaScript `preventDefault()` intercepts the submit event, fades the form (`opacity: 0.4`, `pointer-events: none`), reveals a green success message div with a "Message Sent Successfully!" confirmation, and smooth-scrolls to it.

#### FAQ Section — Bootstrap Accordion (5 Questions)
1. How far in advance should I book?
2. Are your prices all-inclusive?
3. What is your cancellation policy?
4. Do you offer group discounts?
5. Do I need a visa? Can you help?

First item is open by default; Bootstrap's `data-bs-parent` ensures only one is open at a time.

#### Embedded Google Map
`<iframe>` pointing to the New York / Midtown Manhattan area, full-width, 380 px tall, inside a rounded border card.

---

## 🛠 Technologies Used

| Technology | Version / Source | Purpose |
|---|---|---|
| **HTML5** | — | Page structure and semantics |
| **Bootstrap** | 5.3.3 (jsDelivr CDN) | Grid system, navbar, carousel, accordion, utilities |
| **Bootstrap JS Bundle** | 5.3.3 (jsDelivr CDN) | Navbar collapse, carousel, accordion interactivity |
| **CSS3** | `css/style.css` | Custom theme, animations, hover effects, design tokens |
| **Font Awesome** | 6.5.0 (cdnjs CDN) | All icons across the site |
| **Google Fonts** | CDN | `Playfair Display` (headings) + `DM Sans` (body) |
| **Vanilla JavaScript** | Inline `<script>` | IntersectionObserver reveals, back-to-top, form submit handler |
| **Unsplash** | CDN image URLs | All photography (hero, destinations, services, team, about) |
| **Pravatar.cc** | CDN avatar URLs | Testimonial reviewer avatars |
| **Google Maps** | Embed iframe | Office location map on Contact page |

> **No build tools. No Node.js. No frameworks. No dependencies to install.**

---

## 📁 Project Structure

```
travel-agency/
│
├── index.html          ← Homepage (hero, search, destinations, features, testimonials)
├── about.html          ← About page (story, stats, team, mission, vision, values)
├── services.html       ← Services page (8 service cards, process steps, pricing tiers)
├── contact.html        ← Contact page (form, info card, FAQ accordion, map)
│
├── css/
│   └── style.css       ← All custom styles (~850 lines): design tokens, animations,
│                          component styles, hover effects, responsive overrides
│
└── images/             ← Reserved for local image assets
                           (current build uses Unsplash CDN URLs)
```

### `css/style.css` — Architecture at a Glance

```
CSS Custom Properties (design tokens)
Base reset & typography
Navbar
Hero section + keyframe animations (heroZoom, float, fadeInUp, fadeInDown, lineGrow)
Hero search card
Destination cards
Why Choose Us / feature cards
Testimonials carousel
Footer
Page hero (inner pages)
About page components (img wrap, feature list, team cards, mission/vision cards)
Service cards + process steps
Contact components (info card, form card)
Back-to-top button
Scroll-reveal (.reveal / .visible)
Utility classes
Responsive media queries (991px, 768px, 576px)
```

---

## 🚀 How to Run

This is a **pure static website** — no server, no build step, no package manager.

### Option 1 — Open Directly in Browser (Simplest)
```
1. Download or clone the project folder
2. Double-click  index.html
```
That's it. All pages are linked relatively; navigate using the navbar.

### Option 2 — VS Code Live Server (Recommended for Development)
```
1. Open the  travel-agency/  folder in VS Code
2. Install the "Live Server" extension (ritwickdey.liveserver)
3. Right-click  index.html  → "Open with Live Server"
4. Browser opens at  http://127.0.0.1:5500/index.html
```
Live Server auto-refreshes on file save — ideal for editing.

### Option 3 — Python Local Server
```bash
# Python 3
cd travel-agency
python -m http.server 8080
# Then open: http://localhost:8080
```

### Option 4 — Node.js `serve`
```bash
npm install -g serve
cd travel-agency
serve .
# Then open: http://localhost:3000
```

### ⚠️ Internet Required
The project loads Bootstrap, Font Awesome, Google Fonts, and all photography via CDN. An internet connection is required for the full visual experience. The HTML structure and navigation work offline; fonts and images will fall back to system defaults.

---

## 📸 Screenshots

> Add screenshots by saving browser captures into `images/screenshots/` and updating the paths below.

| Page | Preview |
|------|---------|
| **Homepage — Hero & Search** | `images/screenshots/home-hero.png` |
| **Homepage — Destinations** | `images/screenshots/home-destinations.png` |
| **Homepage — Testimonials Carousel** | `images/screenshots/home-testimonials.png` |
| **About — Team Section** | `images/screenshots/about-team.png` |
| **Services — Service Cards** | `images/screenshots/services-cards.png` |
| **Services — Pricing Tiers** | `images/screenshots/services-pricing.png` |
| **Contact — Form & Info** | `images/screenshots/contact-form.png` |
| **Contact — FAQ & Map** | `images/screenshots/contact-faq-map.png` |

---

## 🔮 Future Improvements

The following features are **not currently implemented** and represent natural next steps:

1. **Live destination search** — Wire the homepage search bar to a real travel API (Amadeus, Skyscanner) or filter locally rendered cards by keyword
2. **Backend form handling** — Connect the contact form to a server endpoint (e.g. Node.js + Nodemailer, or a service like FormSpree / EmailJS) so enquiries are actually delivered
3. **Destinations catalogue page** — A dedicated `destinations.html` with filtering by region, price, and trip type; the navbar currently lists only four pages
4. **Blog / Travel Guides section** — The footer links to a "Blog" page that does not yet exist
5. **Image optimisation** — Replace Unsplash CDN URLs with locally stored, WebP-converted, and lazily loaded images for offline use and faster load times
6. **Cookie consent banner** — GDPR-compliant consent notice for the newsletter checkbox and any future analytics
7. **Dark mode** — A CSS `prefers-color-scheme` media query toggle; the design token system (`--sky`, `--navy`) is already well-suited for this
8. **Booking / payment flow** — A multi-step booking wizard with seat selection, passenger details, and payment integration (Stripe, PayPal)
9. **Accessibility audit** — Add `aria-label` attributes to icon-only buttons, improve colour contrast ratios, and add `skip to content` link for keyboard users
10. **JavaScript search filtering** — Enable the "Search Trips" button to dynamically filter the destination cards by typed keyword, date range, and traveller count without a page reload

---

## 👤 Author

**Gajanan Deshmukh**

> Built as a complete front-end practice project demonstrating multi-page site architecture, Bootstrap 5 component usage, custom CSS3 animations, and responsive design principles.

---

<div align="center">

Made with ❤️ and a love for travel &nbsp;|&nbsp; Wanderlust Travel Agency &copy; 2024

</div>
