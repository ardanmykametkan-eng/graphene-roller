# Graphene Roller — Premium Landing Page SPEC v4

## Goal
Create a SINGLE production-ready HTML file that looks like a **$10,000+ premium site**. Must exceed https://graphene.aowei.org in quality, design, and interactivity.

## CRITICAL: No Placeholder Photos!
- **REAL photos only** — use these local files:
  - `./roller1.jpg` — main product photo (720x1280, portrait)
  - `./roller2.jpg` — secondary product photo (720x1280, portrait)
  - NO Unsplash, NO stock photos, NO placeholder images
  - Photos must be converted to base64 inline OR copied to same directory and referenced locally
  - Roller photos should be used in: Hero background, Product cards, About section

## Design System

### Colors
- Primary: `#00c8ff` (cyan)
- Secondary: `#64ffda` (mint)
- Gradient: `linear-gradient(135deg, #00c8ff, #64ffda)`
- Background: `#0a0a0f` (deep dark)
- Surface: `rgba(255,255,255,0.03)` to `0.06`
- Border: `rgba(255,255,255,0.08)`
- Text: `#e0e0e0`, muted: `#888`
- Card hover: subtle glow effect

### Typography
- Font: `'Inter', sans-serif` from Google Fonts (weights 300-900)
- Headings: bold, gradient text on key elements
- Smooth: `-webkit-font-smoothing: antialiased`

## Sections (11 sections minimum)

### 1. Scroll Progress Bar
- Fixed top, 3px height
- Cyan-mint gradient
- Smooth width transition based on scroll position

### 2. Navbar
- Fixed, glass backdrop (`backdrop-filter: blur(20px)`)
- Hide on scroll down, show on scroll up
- Logo: "✦ GRAPHENE ROLLER" with gradient text
- Links: Home, Products, Technology, About, Contact
- Mobile: hamburger menu with smooth open/close animation

### 3. Language Toggle (KZ / RU / EN)
- Fixed position top-right
- 3 buttons in a row
- Active button has gradient background
- Default language: RU
- ALL text must use data-i18n attributes

### 4. Hero Section
- **100vh fullscreen**
- **Three.js 3D hexagonal particle background** — animated, floating, rotating hexagons in cyan/mint colors. This is THE premium feature.
- Large heading with gradient text: "Графеновые Композитные Валки"
- Subtitle describing the product
- WhatsApp CTA button: green gradient (#25d366 → #128C7E), with phone icon, link to `https://wa.me/77022655423`
- Scroll-down indicator (animated arrow/line)
- Subtle radial gradient overlay on top of Three.js canvas

### 5. Benefits Section (4 cards)
- `+300%` — Повышенная износостойкость
- `−40°C` — Работоспособность при экстремальных температурах
- `8→24 мес.` — Увеличенный срок службы
- `40%` — Снижение затрат на обслуживание
- Each card: large gradient number, icon, description
- Hover: gradient top border appears, card lifts

### 6. Products Section (3 product cards)
- **GR-2000 Pro** (Bestseller tag — orange/red gradient)
  - Specifications: ⌀ 200 мм, L 2000 мм, −40..+200°C, HRC 62
  - Use `roller1.jpg` as product image
- **GH-5000 Heavy Duty** (Heavy Duty tag — blue/purple gradient)
  - Specifications: ⌀ 350 мм, L 5000 мм, −50..+300°C, HRC 68
  - Use `roller2.jpg` as product image
- **GS-1000 Smart** (Smart tag — green/cyan gradient)
  - Specifications: ⌀ 150 мм, L 1000 мм, −30..+180°C, IoT Ready
  - Use abstract geometric SVG as product image
- 3D perspective hover effect on cards (rotate on mouse move)
- Smooth zoom on image hover

### 7. Technology Section (4 cards)
- Big numbers in background: 01, 02, 03, 04
- Icons (SVG or emoji): 🔬, ⚙️, 🧪, 🏅
- Content:
  - 01: Материаловедение — графеновые композиты
  - 02: Нано-покрытие — CVD нанесение
  - 03: Прецизионность — точность 0.001 мм
  - 04: Контроль качества — спектроскопия, термотестирование
- Number appears as large transparent text in corner

### 8. About + Stats Section
- Two columns: text + image
- Use `roller1.jpg` or `roller2.jpg` as the about image
- Stats with animated counters:
  - 250+ установок
  - 50+ клиентов
  - 15+ стран
  - ISO сертификат
- Numbers animate from 0 to target on scroll reveal

### 9. Production Process (6 steps)
- Horizontal or 3×2 grid layout
- Numbered: 01→06 with gradient circles
- Steps:
  1. Материалы — отбор графита
  2. CVD синтез — осаждение графена
  3. Покрытие — нанесение композита
  4. Тестирование — контроль качества
  5. Сборка — балансировка
  6. Доставка — по всему миру
- Connecting line/arrow between steps

### 10. Global Presence
- Grid of country tags: 🇰🇿 Казахстан, 🇷🇺 Россия, 🇦🇪 ОАЭ, 🇩🇪 Германия, 🇺🇸 США, 🇨🇳 Китай, 🇹🇷 Турция, 🇮🇳 Индия, 🇰🇷 Южная Корея
- Tags have glass border, hover effect (glow + lift)

### 11. Contact Section
- Form: Name, Email, Phone, Message fields
- Glass-style input fields
- Submit button with gradient
- On submit: show success message + WhatsApp redirect with pre-filled message
- Contact info cards: WhatsApp, Email, Address, Working hours
- Each info card: icon + text, hover lift effect

### 12. CTA Banner
- Full-width gradient background
- Big heading + WhatsApp button
- "Свяжитесь с нами сегодня" style text

### 13. Footer
- 4-column grid: Company, Products, Support, Legal
- Social icons (SVG)
- Copyright line
- Subtle top border

### 14. Chatbot (Floating)
- Fixed bottom-right, above WhatsApp button
- Toggle button: cyan gradient circle
- Chat panel: greeting message + quick reply buttons (prices, delivery, catalog, discount, contact)
- Input field for custom messages
- Simple keyword-based responses in all 3 languages
- Smooth open/close animation

### 15. Floating WhatsApp Button
- Fixed bottom-right
- Green gradient (#25d366 → #128C7E)
- Pulse animation
- Links to `https://wa.me/77022655423`

## Animations (IntersectionObserver)
- **fade-up**: translateY(40px) → 0, opacity 0 → 1
- **slide-left**: translateX(-40px) → 0
- **slide-right**: translateX(40px) → 0
- **scale-in**: scale(0.9) → 1
- Duration: 0.7s cubic-bezier(0.4, 0, 0.2, 1)
- Stagger delays for grid items

## 3 Languages (KZ/RU/EN)
- ALL visible text must have `data-i18n="key"` attribute
- Translation object: `translations = { ru: {...}, en: {...}, kk: {...} }`
- Language toggle switches all text immediately
- WhatsApp link same across all languages

## Contact Form
- Fields: name, email, phone, message
- Validation: all required
- Submit → success message inside the form
- Email to: ardanmykametkan@gmail.com
- WhatsApp fallback: `https://wa.me/77022655423?text=...`

## Technical Requirements
- **Single HTML file** — ALL CSS inline in `<style>`, ALL JS inline in `<script>`
- No external dependencies except:
  - Google Fonts (Inter)
  - Three.js from CDN (`https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js`)
- Must pass HTML validation
- All images loaded with `loading="lazy"`
- Smooth scrolling (`scroll-behavior: smooth`)
- Responsive: mobile-first, tablets, desktops
- Mobile: hamburger menu, stacked grids, touch-friendly targets

## Output
Write to: `/home/onion/.openclaw/workspace/graphene-roller/index.html`

## CRITICAL REMINDERS
1. **USE roller1.jpg AND roller2.jpg** — NOT Unsplash, NOT placeholders
2. Roller photos in: hero (as bg element), product cards, about section
3. Three.js 3D hex background in hero — this is non-negotiable
4. All 3 languages must be complete
5. NO ChatGPT-style filler text — use proper industrial/B2B copy
6. Each section must have scroll-reveal animation
7. File must be under 200KB (excluding base64 images, use relative paths for images)
