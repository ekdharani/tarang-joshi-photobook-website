**# Ek Dharani Photobook Donation Site**

A dedicated microsite for the **Ek Dharani** photobook campaign. This is a testing / staging version intended for final integration into the main [Ek Dharani](https://ekdharani.org) website.

---

### About Ek Dharani

**Ek Dharani** is a non-profit organization dedicated to environmental conservation, sustainability, and raising awareness about our planet through powerful storytelling and community action.

### Project Purpose

This microsite serves as a focused donation portal for **Tarang Joshi’s limited-edition photobook**. Every contribution helps support Ek Dharani’s conservation projects, and donors have the option to receive a **physical hard copy** of the photobook as a token of appreciation.

The site is designed to:
- Clearly communicate the story and impact of the photobook
- Provide a smooth and trustworthy donation experience
- Track donations and manage hard-copy fulfillment by Tarang Joshi
- Serve as a beautiful, high-conversion landing page

---

### Features

- Clean, emotionally engaging design optimized for storytelling
- Secure donation processing
- Tiered donation options with corresponding rewards (especially hard-copy photobook)
- Progress tracker / goal visualization
- Mobile-responsive layout
- Integration-ready for the main Ek Dharani website
- Analytics and conversion tracking hooks

---

### How It Works

1. Visitors explore the photobook story and impact
2. They choose a donation amount
3. Option to receive a **physical hard copy** (handled personally by Tarang Joshi)
4. Secure donation is processed
5. Confirmation + fulfillment details sent

---

### Current Status

**Testing / Pre-Production**  
This repository contains the version currently being reviewed for final inclusion in the main Ek Dharani website.

---

### Tech Stack

- [Next.js / React] *(update with actual stack)*
- Tailwind CSS
- Payment integration *(Stripe / Razorpay / etc.)*
- Form handling & validation
- Deployment-ready for Vercel / Netlify / main hosting

---

### Local Development

```bash
# Clone the repository
git clone <repository-url>
cd ek-dharani-photobook

# Install dependencies
npm install

# Run development server
npm run dev
```

---

### Deployment

This site is built to be easily deployed as a standalone microsite or embedded/integrated into the main Ek Dharani platform.

---

### Contributing

We welcome improvements, bug fixes, and design suggestions. Please create an issue or submit a pull request.

---

### Credits

- **Photography & Concept**: Tarang Joshi
- **Organization**: Ek Dharani (Non-Profit)
- **Development**: [AI Generated - DeepSeek]

---

### Contact

For partnership, press, or donation-related queries:  
**Ek Dharani** — [contact@ekdharani.org] *(update with actual email)*

### Requirements

Build a single-file HTML site (no external dependencies—all CSS/JS self‑contained or loaded from a CDN, no framework) for **Tarang Joshi’s minimalist photo‑book store**.

**Product & brand**
- Tarang’s two physical photo books, created with 14Trees.
- Book 1: `tarang.joshi-2509-ungreen-scape.pdf`, thumbnail `tarang.joshi-2509-ungreen-scape.jpg`
- Book 2: `tarang.joshi-2503-between-shadows.pdf`, thumbnail `tarang.joshi-2503-between-shadows.jpg`

**Design & layout**
- Ultra‑minimalist, mobile‑first (85% mobile), responsive from smart‑watch to TV.
- Splash hero image at top (placeholder fine), then product cards below.
- Product cards: thumbnail, title, short description, two CTAs – “Preview” & “Order on WhatsApp”.
- Clicking **thumbnail** or “Preview” opens the flipbook preview.
- Future‑ready: placeholder sections for Video & Stories (coming soon).

**Flipbook preview (core interactive)**
- Use an open‑source page‑flip library (Turn.js, dFlip Lite/Non‑Commercial, or 3D‑Flipbook by subhamgiri16 – prefer one that avoids jQuery, e.g., 3D‑Flipbook, to keep the bundle tiny). Embed its source directly or via a single CDN `<script>` tag.
- Combined with **PDF.js** (CDN) to render PDF pages into canvas.
- **Preview gating**: Show **only the first 5 and last 5 pages** of each PDF. All intermediate pages are invisible in the book.
- Overlay the entire flipbook area with a **dark blurred overlay** and CTA text: *“Donate to EkDharani to get the complete book”*.
- Once overlay is dismissed (e.g., after donation signal), unlock the full book (simulated: show a success message or enable all pages – implementation can be a simple toggle after the user confirms donation).

**Payment & conversion UX**
- Tapping the overlay CTA opens a payment modal with multiple options:
  1. **UPI app deep‑link**: `upi://pay?pa=EKDHARANI.09@cmsidfc&pn=Donation%20to%20EkDharani&mode=02&am=` (amount omitted or user‑chosen). Mobile tap → opens UPI app instantly.
  2. **QR fallback**: Show image `ek.dharani.UPI.png` prominently for scanning.
  3. **Bank details fallback** (trust layer):
     - Account: 10059271015
     - IFSC: IDFB0040101
     - Bank: IDFC
- Auto‑detect mobile (to prioritise UPI intent) vs desktop (show QR primarily).
- “Unlock after payment” semi‑automated flow: after donation, user clicks “I have donated” → a thank‑you message and manual unlock (or display a link to claim the full book via WhatsApp). Store the unlocked state in localStorage so returning visitors don’t see the overlay again for that book.

**WhatsApp ordering**
- Pre‑filled WhatsApp link (phone: **91993006169**, replace any placeholder with this number).
- Message template: “Hi Tarang, I’m interested in buying your photo book [Book Name]. Please share details.”
- Button opens chat directly.

**Technical must‑haves**
- **Real page‑flip animation** (no scrolling PDF view).
- **Progressive page loading** in PDF.js (load pages on‑demand as user flips).
- **Gesture‑based flipping** (swipe on touch, click‑drag/mouse wheel on desktop).
- **Lazy loading** of product thumbnails and hero image.
- **No framework** – vanilla HTML/CSS/JS, single `.html` file. All assets (PDFs, JPGs, PNGs) referenced by URL, no local dependency.
- The entire site must work offline‑first where possible (service worker optional, but at minimum no 404 if CDN fails, graceful fallback).
- Cinematic micro‑transitions: card hover, overlay fade, modal entrance.

**Output**
Deliver the complete HTML code with all styles and scripts inline, ready to open in any browser. Add clear comments where iterative additions (videos, blog, cart) can be plugged in later.

---

**Thank you for helping us protect and celebrate our one Earth — Ek Dharani.**

---

*Made with ❤️ for a greener planet.*
