---
status: pending
title: Chocolate Hub Business Website
---

## Goal
A warm, cozy single-page business website for **Chocolate Hub** — a chocolate store — where customers can learn about the brand and get in touch via a contact form, phone, email, address, and social media.

## Visual Style
- Colour palette: rich browns, creams, and gold tones
- Warm, inviting typography
- Smooth scroll between sections
- Fully responsive (mobile + desktop)

---

## Steps

### 1. Project foundation
- Create /app/src/styles/global.css starting with `@import "tailwindcss";`
- Define warm CSS custom properties (brown, cream, gold colour tokens) using `@theme` inside global.css
- Ensure global.css is imported once in /app/src/main.tsx
- Create /app/src/types/index.ts to hold shared TypeScript interfaces (e.g. NavItem, Service, Testimonial, FAQItem)

### 2. Layout shell
- Create /app/src/components/Navbar.tsx — sticky top navigation with the "Chocolate Hub" logo/name on the left and smooth-scroll links to each section on the right; collapses to a hamburger menu on mobile
- Create /app/src/components/Footer.tsx — contains copyright text, quick nav links, and social media icon links (Instagram, Facebook, TikTok, X/Twitter, YouTube, WhatsApp)
- Create /app/src/pages/HomePage.tsx — the single root page that assembles all sections in order, wrapped by Navbar and Footer

### 3. Hero section
- Create /app/src/components/sections/HeroSection.tsx
- Full-viewport-height banner with a rich chocolate-toned background
- Large welcoming headline ("Welcome to Chocolate Hub") and a short tagline
- A prominent call-to-action button that smooth-scrolls to the Contact section
- Decorative subtle texture or gradient overlay to reinforce the cozy feel

### 4. About section
- Create /app/src/components/sections/AboutSection.tsx
- Two-column layout (image placeholder on one side, story text on the other) that stacks on mobile
- Short "Our Story" narrative about the brand's passion for chocolate

### 5. Services section
- Create /app/src/components/sections/ServicesSection.tsx
- Grid of service cards (e.g. Artisan Chocolates, Gift Boxes, Custom Orders, Chocolate Tasting)
- Each card has an icon, title, and short description
- Service data defined as a typed array in /app/src/lib/servicesData.ts

### 6. Gallery / Portfolio section
- Create /app/src/components/sections/GallerySection.tsx
- Responsive masonry-style or uniform grid of placeholder image tiles
- Soft hover effect (slight zoom or golden overlay) on each tile
- Placeholder images using a solid brown/cream coloured div with a label (ready to swap for real photos)

### 7. Testimonials section
- Create /app/src/components/sections/TestimonialsSection.tsx
- Horizontally scrollable or grid layout of customer review cards
- Each card shows a star rating, quote text, and reviewer name
- Testimonial data defined as a typed array in /app/src/lib/testimonialsData.ts

### 8. FAQ section
- Create /app/src/components/sections/FAQSection.tsx
- Accordion-style list of common questions and answers
- Clicking a question expands/collapses the answer with a smooth animation
- FAQ data defined as a typed array in /app/src/lib/faqData.ts
- Create /app/src/hooks/useAccordion.ts to manage open/close state

### 9. Contact section
- Create /app/src/components/sections/ContactSection.tsx
- Contact form with fields: Full Name, Email Address, Message — and a styled Submit button
- Create /app/src/hooks/useContactForm.ts to manage form state and basic validation (required fields, valid email format); shows inline error messages and a success confirmation message after submission
- Below the form, display a contact info panel with:
  - Phone number (placeholder)
  - Email address (placeholder)
  - Physical address (placeholder)
  - Social media icon links (Instagram, Facebook, TikTok, X/Twitter, YouTube, WhatsApp) opening in a new tab

### 10. Routing and page assembly
- Update /app/src/main.tsx to render HomePage and import global styles
- Update /app/src/App.tsx (or equivalent entry) to render the HomePage component
- Ensure all section components are imported and rendered in correct order inside /app/src/pages/HomePage.tsx:
  1. HeroSection
  2. AboutSection
  3. ServicesSection
  4. GallerySection
  5. TestimonialsSection
  6. FAQSection
  7. ContactSection
