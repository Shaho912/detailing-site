# NextDoorCustoms — Product Requirements Document

## Business Overview

**Business:** NextDoorCustoms  
**Type:** Mobile & shop car detailing  
**Location:** Connecticut (203 area code — local & surrounding towns)  
**Phone:** (203) 550-7730 — call or text  
**Instagram:** @NextDoorCustoms  
**Booking:** DM on Instagram or call/text  
**Promo:** First-time customers get 10% off  

## Goals

- Establish a professional online presence that converts visitors into bookings
- Make phone/text booking frictionless on mobile devices
- Present services and pricing clearly so customers arrive pre-qualified
- Lay groundwork for Netlify form submissions (wired up separately)

## Target Users & Devices

Primary: Mobile users (smartphone, tapping to call/text)  
Secondary: Desktop users researching before booking  
Design approach: Mobile-first, tested at 375px minimum width

## Tech Stack

- Plain HTML5 + CSS3 + minimal vanilla JS — no build step
- Google Fonts (Inter) via CDN
- No CSS framework — custom design tokens via CSS variables
- Contact form uses Netlify Forms attributes (`data-netlify="true"`)

## Design System

| Token | Value | Usage |
|---|---|---|
| `--bg` | `#0D0D0D` | Page background |
| `--bg-card` | `#1A1A1A` | Card/section backgrounds |
| `--accent` | `#E63946` | Buttons, badges, highlights |
| `--accent-hover` | `#C1121F` | Button hover state |
| `--text` | `#F1F1F1` | Body text |
| `--text-muted` | `#9CA3AF` | Secondary text |
| `--border` | `#2A2A2A` | Card borders, dividers |

**Font:** Inter (400, 600, 700 weights)  
**Motif:** Single checkered CSS stripe on hero — subtle, not repeated

## Site Structure

| Page | File | Purpose |
|---|---|---|
| Home | `index.html` | First impression, CTAs, promo |
| Services & Pricing | `services.html` | Package cards, add-ons |
| Gallery | `gallery.html` | Before/after photo grid |
| About | `about.html` | Brand story, service area |
| Contact | `contact.html` | Form, phone, Instagram |

## Services & Pricing

### Packages

| | Basic | Exclusive ⭐ | Premium |
|---|---|---|---|
| Exterior Detail | $60 | $90 | $120 |
| Interior Detail | $70 | $100 | $130 |
| Both — Sedan | $125 | $175 | $225 |
| Both — SUV | $150 | $200 | $250 |

**Basic includes:** Exterior Hand Wash · Tire Cleaning & Shine · Interior Vacuum · Surface Wipe Down  
**Exclusive includes:** Everything in Basic + Wax Protection · Deep Interior Cleaning · Windows Cleaned · Dashboard & Trim Polish  
**Premium includes:** Everything in Exclusive + Full Interior Shampoo · Stain Removal · Clay Bar Treatment · High-Gloss Wax/Sealant  

Exclusive is marked as Most Popular / Recommended.

### Add-Ons

| Service | Price |
|---|---|
| Headlight Restoration | $60+ |
| Engine Bay Detail | $50+ |
| Rust Removal | $50+ |
| Pet Hair Removal | $40+ |
| Aftermarket Installation | $70+ |

Note shown: "Ask about bundle deals & monthly plans."

## Contact Form Fields

- Name (text, required)
- Phone (tel)
- Email (email, required)
- Service Interest (select: Basic / Exclusive / Premium / Add-On / Other)
- Message (textarea)
- Submit button

Form uses `data-netlify="true"` — activate by deploying to Netlify.

## Future Considerations

- Wire up Netlify Forms and add success/error redirect pages
- Replace gallery placeholder slots with real before/after photos
- Add Google Maps embed on About or Contact page showing service area
- Add a reviews/testimonials section (Google reviews embed or manual quotes)
- Consider a favicon using the NDC initials in accent red
- SEO: Add structured data (LocalBusiness schema) for Google search
