# Graphene Roller — Complete Site Spec

## Goal
Create a SINGLE production-ready HTML file matching (and exceeding) the quality of https://graphene.aowei.org.
This is a B2B industrial landing page for Graphene Roller — graphene composite rollers.

## MUST USE
- UI/UX Pro Max v2.5 design system (read skills from ~/.openclaw/workspace/.claude/skills/ui-ux-pro-max/)
- Theme: Hero-Centric + Feature-Rich Showcase pattern

## Design System
- Primary: #00c8ff (cyan)
- Secondary: #64ffda (mint)  
- Gradient: linear-gradient(135deg, #00c8ff, #64ffda)
- Background: #0a0a0f
- Glass: rgba(255,255,255,0.04)
- Border: rgba(255,255,255,0.08)
- Text: #e0e0e0, muted: #888
- Font: 'Inter', sans-serif (300-900 from Google Fonts)

## All Sections (11 total)
1. **Scroll Progress Bar** - fixed top, cyan-mint gradient
2. **Navbar** - fixed glass, hide on scroll down, show on scroll up, logo "✦ GRAPHENE ROLLER", links: Home, Products, Technology, About, Contact. Mobile hamburger.
3. **Language Toggle** - fixed top-right (KZ/RU/EN buttons), default RU
4. **Hero** - 100vh, Three.js 3D hexagonal particle background, gradient title, subtitle, WhatsApp CTA button (+77022655423), scroll indicator
5. **Benefits** - 4 cards: +300% durability, −40°C temp, 8→24 months lifespan, 40% savings. Gradient top-border on hover.
6. **Products** - 3 cards with 3D hover perspective. Use real Unsplash images. Tags: Bestseller/Heavy Duty/Smart with specs
7. **Technology** - 4 cards with big background numbers (01-04). Material Science, Nano Coating, Precision Engineering, Quality Control
8. **About + Stats** - Gradient numbers with counters: 250+ installations, 50+ clients, 15+ countries, ISO certified
9. **Process** - 6 steps numbered: Material → CVD → Coating → Testing → Assembly → Delivery
10. **Global Presence** - Country tags: Kazakhstan, Russia, UAE, Germany, USA, China, Turkey, India, South Korea
11. **Contact Form** - Name, Email, Phone, Message fields. 4 info cards: WhatsApp, Email, Location, Hours
12. **CTA Banner** - Gradient background, big heading, WhatsApp button
13. **Footer** - 4-column grid: Company, Products, Support, Legal. Social icons. Copyright.

## Three.js 3D Background
Load from CDN: https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js
Create animated hexagon particles floating and rotating slowly. THIS IS ESSENTIAL — the main premium feature.

## 3 Languages
Every text visible to user must have data-i18n="key" attribute.
Language toggle switches all text between KZ/RU/EN.
Store translations in JS object: translations = { ru: {...}, en: {...}, kk: {...} }

## Chatbot
Floating chat toggle button (cyan gradient, bottom-right).
Chat panel with:
- Bot greeting message
- Quick reply buttons: prices, delivery, catalog, discount, contact
- Send message input
- Simple keyword-based responses in 3 languages

## WhatsApp Floating Button
Fixed bottom-right (above chatbot). Green gradient. Pulse animation.

## Animations
All use IntersectionObserver:
- fade-up: translateY(40px) → 0
- slide-left: translateX(-40px) → 0  
- slide-right: translateX(40px) → 0
Scroll reveal with 0.7s cubic-bezier transition

## Mobile Responsive
- Hamburger menu for mobile
- Grids collapse to 1 column
- Touch-friendly tap targets

## Images
Use real Unsplash images for:
- Hero (abstract industrial/graphene)
- Products (rollers, machinery)
- Technology (lab, coating)
- About/process (factory, manufacturing)

## Contact Form
Collect: name, email, phone, message.
On submit: show success message + redirect to WhatsApp with pre-filled message.

## Output
Write to ~/.openclaw/workspace/graphene-roller/index.html

## IMPORTANT
- Complete file, NO placeholders
- All CSS inline in <style>
- All JS inline in <script> at bottom before </body>
- All 3 languages fully implemented
- Must pass HTML validation
- No external dependencies except: Google Fonts, Three.js CDN
