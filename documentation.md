# QuickBite — Full Project Documentation

**Course:** EWA408510 – E-Commerce and Web Application
**Instructor:** Eric Maniraguha
**Assessment:** Group Assignment II — Designing a User-Friendly Web Application Prototype
**Institution:** UNILAK, Kigali, Rwanda

---

## Group Members

| Name | Registration Number |
|------|-------------------|
| [Student 1 Full Name] | [Reg. No.] |
| [Student 2 Full Name] | [Reg. No.] |

---

## Selected Application

**Food Delivery Web Application — QuickBite Rwanda**

---

## 1. Problem Statement

### What problem does the application solve?
Ordering food in Rwanda's growing urban areas — especially Kigali — still relies heavily on phone calls, WhatsApp messages, or physically visiting restaurants. This process is slow, error-prone (wrong orders, miscommunication), and offers no delivery visibility. Customers have no way to compare menus, read reviews, or track their orders once placed.

Local restaurants also lack a unified digital channel to reach customers, accept orders efficiently, or manage deliveries. The result is lost revenue, poor customer experience, and slow adoption of digital commerce.

### Who are the target users?
- Urban professionals aged 20–40 in Kigali who are time-constrained
- University students who want affordable food delivered to campus
- Families ordering occasional takeout for convenience
- Remote workers who eat at home and want variety without cooking
- Restaurant owners wanting to expand their customer reach digitally

### Why is the system important?
QuickBite removes friction from the food ordering experience. By centralizing multiple restaurants in one interface, enabling real-time delivery tracking, and providing a secure payment flow (including MTN MoMo and Airtel Money), it saves time, reduces ordering errors, and increases satisfaction for both customers and restaurant partners. It also supports Rwanda's national digital economy goals by bringing local food businesses online.

---

## 2. User Personas

### Persona 1: Amina Uwase

| Attribute | Detail |
|-----------|--------|
| **Name** | Amina Uwase |
| **Age** | 27 |
| **Occupation** | Software Developer at a tech firm in Kicukiro |
| **Location** | Kigali, Rwanda |
| **Devices** | Laptop (primary), Android phone |
| **Tech Comfort** | High |

**Goals:**
- Order lunch quickly during short work breaks (under 10 minutes)
- Discover new restaurants near her office
- Track delivery without calling the restaurant
- Pay using MTN MoMo or card

**Challenges / Frustrations:**
- Restaurants have no website — she has to call and describe what she wants
- No confirmation that the order was received correctly
- Delivery times are unpredictable — she doesn't know when to expect food
- Wants to see photos and prices before choosing a restaurant

---

### Persona 2: Jean-Pierre Habimana

| Attribute | Detail |
|-----------|--------|
| **Name** | Jean-Pierre Habimana |
| **Age** | 20 |
| **Occupation** | Second-year student at UNILAK |
| **Location** | Gasabo, Kigali (on-campus hostel) |
| **Devices** | Android smartphone (primary) |
| **Tech Comfort** | Medium |

**Goals:**
- Find affordable food options that deliver to campus
- Split orders with friends easily
- Get food quickly between classes
- Use mobile money since he has no bank card

**Challenges / Frustrations:**
- Most food apps don't deliver to his area or have high minimum orders
- Doesn't always have cash and can only pay via MTN MoMo
- Hard to know which restaurants are open late in the evening
- Spends too much time searching WhatsApp groups for restaurant contacts

---

## 3. User Flow Diagram

See the interactive visual diagram: `/docs/user-flow-diagram.html`

**Text Summary:**

```
[Open App]
    |
    v
[Has Account?]
    |-- YES --> [Login Page]
    |-- NO  --> [Register Page]
    |
    v
[Home / Landing Page]
  - Search bar
  - Category filter (Burgers, Pizza, Sushi, etc.)
  - Featured restaurants
    |
    v
[Browse Restaurants]
  - Filter chips (category, free delivery, fast)
  - Live search
    |
    v
[Restaurant Menu Page]
  - Category tabs
  - Menu items with Add to Cart
  - Live cart sidebar
    |
    v
[Add More Items?]
    |-- YES --> back to menu
    |-- NO  --> [Cart Page]
    |
    v
[Cart Page]
  - Item management (qty, remove)
  - Promo code
  - Order summary
    |
    v
[Checkout Page]
  - Delivery address form
  - Delivery time (ASAP / Schedule)
  - Payment method (MTN MoMo / Airtel / Card / Cash)
    |
    v
[Payment Successful?]
    |-- FAILED  --> Error message + Retry
    |-- SUCCESS --> [Order Confirmed]
    |
    v
[Order Tracking Page]
  - Live status: Confirmed → Preparing → Out for Delivery → Delivered
  - Driver info
  - Map placeholder
    |
    v
[Leave Review / Reorder / View Profile]
    |
    v
[Session Complete]
```

---

## 4. Wireframes (Low-Fidelity)

Six wireframe screens are included in `/wireframes/`:

| File | Screen |
|------|--------|
| `01-home-wireframe.html` | Home / Landing Page |
| `02-restaurant-wireframe.html` | Restaurant Menu Page |
| `03-cart-wireframe.html` | Cart Page |
| `04-checkout-wireframe.html` | Checkout Page |
| `05-login-register-wireframe.html` | Login & Register |
| `06-profile-wireframe.html` | User Profile Page |

Wireframes focus on **structure and layout** — no colors, using dashed borders and grey boxes as placeholders. They demonstrate the placement of key UI elements including navigation, content areas, forms, CTAs, and sidebars.

---

## 5. High-Fidelity UI Design

Eight polished screens are included in `/high-fidelity-designs/`:

| # | Screen | Description |
|---|--------|-------------|
| 01 | Landing Page | Hero, search, categories, restaurant grid, how-it-works, footer |
| 02 | Browse Restaurants | Filterable grid with 10 restaurants |
| 03 | Restaurant Menu | Category tabs, food items, live cart sidebar |
| 04 | Cart | Full cart management with promo code |
| 05 | Checkout | Address, delivery time, payment methods |
| 06 | Order Tracking | Live progress tracker, driver info, map |
| 07 | Login & Register | Tabbed auth with validation and password strength |
| 08 | User Profile | Sidebar navigation, order history, addresses, settings |

**Design System:**

| Token | Value | Usage |
|-------|-------|-------|
| Primary | `#FF4B2B` | CTAs, active states, brand |
| Gradient | `#FF4B2B → #FF416C` | Buttons, hero, accents |
| Background | `#FAFAF8` | Page background |
| Surface | `#FFFFFF` | Cards, modals |
| Text | `#1A1A2E` | Body and headings |
| Muted | `#6B7280` | Secondary text |
| Success | `#2ECC71` | Confirmations, free delivery |
| Font (Display) | Poppins 700–800 | Headings, buttons |
| Font (Body) | Inter 400–600 | Body text, inputs |

---

## 6. Features Implemented

- ✅ Responsive navigation with live cart counter
- ✅ Category filter buttons (Home page) — filters restaurant grid in real time
- ✅ Filter chips (Browse page) — 12 filters including Free Delivery and Under 30 min
- ✅ Live search — matches restaurant name and food tags
- ✅ Restaurant browsing with 10 restaurants across 8 food categories
- ✅ Restaurant menu with 5 category tabs and 14+ menu items
- ✅ Add to cart with live sidebar updates
- ✅ Cart page with quantity controls and item removal
- ✅ Promo code system (try: QUICKBITE or SAVE10)
- ✅ Checkout with address form, time selector, payment method picker
- ✅ Order confirmation with animated success state
- ✅ Order tracking with live progress bar, step tracker, driver info
- ✅ Login with form validation and error highlighting
- ✅ Register with password strength meter and terms agreement
- ✅ User profile with 6 sections: Profile, Orders, Addresses, Payment, Favourites, Settings
- ✅ Toast notification system for user feedback
- ✅ Fully responsive layout (mobile, tablet, desktop breakpoints)
- ✅ MTN MoMo and Airtel Money as primary payment options (Rwanda-specific)
- ✅ Prices displayed in RWF (Rwandan Franc)

---

## 7. Accessibility Considerations

| Consideration | Implementation |
|---------------|---------------|
| Font sizes | Minimum 13px body text; headings scale up with `clamp()` |
| Color contrast | All text meets WCAG AA contrast ratio (≥4.5:1) |
| Keyboard navigation | Logical tab order through all interactive elements |
| Button targets | Minimum 44×44px touch targets on all buttons |
| Form labels | All inputs have visible, associated labels |
| Error messages | Inline error text with red border highlighting |
| Focus states | Browser-native focus rings preserved |
| Semantic HTML | Proper use of `<nav>`, `<button>`, `<input>`, `<label>` |
| Responsive layout | CSS Grid + Flexbox with mobile breakpoints at 600px and 900px |
| Motion | Animations subtle and functional (toast, confirmation pop) |
| Empty states | Clear messaging when cart is empty or no search results |
| Contrast on dark bg | White text on dark hero maintained at high contrast |

---

## 8. Challenges Faced

- **Cart state across pages:** Without a framework, keeping cart data consistent required a shared JavaScript array with re-render functions called on every navigation.
- **Responsive grid:** Ensuring the restaurant grid collapses gracefully from 3 columns → 2 → 1 required careful use of `auto-fill` and `minmax()` in CSS Grid.
- **Filter logic:** Combining category filter + search query required a single filter function that checks both conditions simultaneously to avoid conflicts.
- **Rwanda-specific payments:** Designing for MTN MoMo and Airtel Money (rather than just card/PayPal) required custom UI that still felt familiar and trustworthy.
- **No-dependency approach:** Building a fully interactive prototype without React or any library meant managing all DOM updates manually — a good exercise in vanilla JavaScript.

---

## 9. Conclusion

QuickBite demonstrates a complete, user-centered food delivery web application — from initial problem definition through wireframing, visual design, and a fully interactive prototype. The design prioritizes clarity, accessibility, and a warm visual identity that makes ordering food feel effortless and appealing.

The project addresses a real gap in Kigali's food delivery market, with Rwanda-specific features including MTN MoMo payment, Airtel Money, RWF pricing, and restaurant names reflective of Kigali's food scene.

All assignment deliverables have been met: problem statement (5 pts), two user personas and visual user flow (10 pts), six wireframe screens (15 pts), eight high-fidelity screens (15 pts), a fully interactive prototype with working navigation, cart, filters, and checkout (25 pts), and documented accessibility and responsive design considerations (20 pts).
