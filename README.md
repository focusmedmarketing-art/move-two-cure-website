# Move Two Cure — Website

Single-page website for Move Two Cure (Rolfing® and Personalized Training clinic in London, Ontario, Canada).

## 📁 File structure

```
m2c_final/
├── index.html          # All site content (single page with navigation anchors)
├── styles.css          # All styling
├── images/             # Photos + logos
│   ├── jeymison-training.jpg       (hero photo)
│   ├── jackeline-rolfing-hero.jpg  (Rolfing services/hero)
│   ├── jackeline-rolfing-method.jpg (Rolfing section)
│   ├── jeymison-coaching.jpg       (About - Jeymison)
│   ├── couple-consultation.jpg     (unused - available for use)
│   ├── logo-green-horizontal.png   (navbar)
│   ├── logo-gold-horizontal.png    (footer)
│   └── enso-gold.png               (accent/badge)
└── README.md           # This file
```

## 🚀 How to view locally

Just open `index.html` in any browser. No build step needed.

## 🌐 How to deploy

Upload the whole `m2c_final/` folder to any static host:
- **Cloudflare Pages** (recommended — free, fast)
- Netlify (free)
- Vercel (free)
- GitHub Pages (free)

All links inside the site use anchors (`#about`, `#rolfing`, etc.), so everything works on a single page.

---

## ⚡ PROMPT FOR CLAUDE CODE

Copy and paste the prompt below into Claude Code to continue development:

---

```
I'm working on a single-page website for Move Two Cure (M2C), a Rolfing® and
personalized training clinic in London, Ontario, Canada. The site is built in
plain HTML/CSS/JS (no framework, no build step). Please help me improve and
finalize it.

## CURRENT STATE

Files:
- index.html — all sections (hero, philosophy, method, about, services,
  testimonials, rolfing in depth, training in depth, FAQ, contact, final CTA, footer)
- styles.css — all styling (editorial-minimalist aesthetic)
- images/ — all photos and logos

Brand identity (already locked):
- Colors: Forest Green #1A3330, Gold Vivid #D9A94D, Warm Cream #F0EDE4
- Typography: DM Serif Display (headlines) + DM Sans Light (body)
- Tagline: "Movement is information"
- Method framework: Aware → Restore → Build → Perform
- Philosophy: pain as a protective strategy; movement as information to
  the nervous system

## TASK 1 — CONNECT THE CONTACT FORM (PRIORITY)

The contact form currently has a placeholder `YOUR_FORMSPREE_ENDPOINT` in
its `action` attribute. Walk me through connecting it to Formspree:

1. Tell me exactly what steps to do on formspree.io
   (create account, create form, set destination email to
   movetwocure@gmail.com, copy endpoint URL)
2. Once I give you the endpoint, replace `YOUR_FORMSPREE_ENDPOINT`
   in index.html with the real URL
3. Test the form works by submitting a test message
4. Explain what happens to form submissions — where they go,
   how spam protection works, and what the 50 free/month limit means
5. Add a honeypot field to reduce spam (standard Formspree technique)

## TASK 2 — CANADIAN UX IMPROVEMENTS

Review the site specifically from the perspective of a Canadian (Ontario)
user arriving from a paid ad. Implement these additions:

### 2a. Trust badges section
Add a small "Credentials & Associations" strip below the Hero or between
About and Services. Include visual badges for:
- Dr. Ida Rolf Institute (Jackeline's certification)
- College of Physiotherapists of Ontario (if applicable — ask me first)
- Any other associations I confirm
Style: cream background, small grayscale logos, "Certified & Credentialed"
eyebrow label.

### 2b. Insurance / direct billing notice
Canadians expect to see this upfront. Add a clear line near the Contact
section and in the FAQ:
"Rolfing® sessions covered under most extended health plans in Ontario
(through Active Care Physiotherapy). Direct billing available for
participating plans. Ask during your free consultation."

### 2c. Google Maps embed
Add an embedded Google Map of the Active Care Physiotherapy location in
London, ON to the Contact section — below the Info sidebar or as its own
card. Use Google Maps iframe embed (not an image).

### 2d. Pricing hint
Ask me whether to show indicative pricing ("Starting from $XXX / 60 min")
or leave it for the consultation. If yes, add a subtle pricing note to
each service card.

## TASK 3 — BUG FIXES & POLISH

### 3a. Mobile photo sizing audit
Test the site at these mobile widths and report any cropped heads or
awkward image positioning: 375px (iPhone SE), 390px (iPhone 14),
414px (Pro Max), 768px (iPad). Fix `object-position` values per image
where needed — no face should ever be cropped.

### 3b. Testimonial carousel: add swipe indicators
The carousel at the testimonials section currently has Prev/Next buttons
but no indication of progress. Add a dots indicator below the carousel
showing which of the 4 testimonials is active.

### 3c. Accessibility pass
- Check all images have meaningful `alt` attributes
- Add `aria-label` to icon-only buttons where missing
- Verify color contrast meets WCAG AA on all text
- Ensure the mobile menu traps focus when open

### 3d. Performance
- Add `loading="lazy"` to all images below the fold
- Confirm font loading doesn't cause layout shift
  (add `font-display: swap` if not present)

## TASK 4 — CONTENT CUSTOMIZATION

Several places have placeholder content I need to replace:

### 4a. Replace placeholder testimonials
The 4 testimonials in the `#testimonials` section are placeholders
(Sarah M., Michael T., David K., Amanda R.). I'll provide real client
quotes — update the name, location, and quote for each.

### 4b. Add Summer Series, Blog, and E-books integration
These exist on the old site (movetwocure.com) but are linked as "#"
placeholders in the footer. Help me:
- Create a simple Summer Series section (evergreen, with event types
  explained, not tied to specific dates) OR a simple page for it
- Link the e-books (Move Again, 7 Days to Restart) to actual
  download pages (with Formspree form capture for email → PDF)

### 4c. Fill the unused photo
`images/couple-consultation.jpg` shows Jeymison + Jackeline looking at a
laptop. Suggest the best placement for it — probably near a
"Your assessment starts here" CTA or near the contact section.

## TASK 5 — ONGOING GUIDANCE

Before each significant change, ask me 1-2 quick questions if the
decision affects user-facing content. After changes, describe what
changed and why. Keep the editorial-minimalist aesthetic — don't
introduce new colors, fonts, or heavy components without asking.
```

---

## 🎯 Priority order (my recommendation)

1. **Connect Formspree** (Task 1) — without this, the form is broken
2. **Mobile photo audit** (Task 3a) — catches real visual issues
3. **Trust badges + insurance notice** (Tasks 2a, 2b) — biggest conversion wins for Canadian audience
4. **Replace placeholder testimonials** (Task 4a) — as soon as real ones are available
5. Everything else as capacity allows

## 📝 Notes on what's already done

- ✅ "Book Free Consultation" used everywhere (not "Assessment")
- ✅ Hero photo visible on both desktop AND mobile (stacked above text on mobile)
- ✅ Photos use `object-position: center 20-40%` to preserve heads/faces
- ✅ 4 testimonial cards in horizontal carousel
- ✅ Full mobile navigation with hamburger menu
- ✅ Formspree-ready form (just need to add endpoint)
- ✅ All brand colors + typography locked via CSS variables (--green, --gold-vivid, etc.)

---

## 🔗 Useful links

- Move Two Cure (current site): https://www.movetwocure.com/
- Instagram: https://www.instagram.com/move2cure
- Contact: movetwocure@gmail.com · +1 (226) 998-7843
