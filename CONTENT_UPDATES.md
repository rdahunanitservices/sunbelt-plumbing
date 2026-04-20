# Content Update Guide

This site was built with **placeholder content** so development could begin before all client assets arrived. Every placeholder is marked in the code with a `<!-- REPLACE ME -->` HTML comment so you can find them with a quick search across files.

---

## ✅ Quick Replacement Checklist

Use this checklist as you swap each piece of content:

### 1. Business Logo
- [ ] Drop logo file in `assets/images/logo.png` (transparent PNG preferred)
- [ ] In **all 5 HTML files**, find `<span class="logo-mark">SP</span>` (appears twice per file: header + footer)
- [ ] Replace with: `<img src="assets/images/logo.png" alt="Sunbelt Plumbing" style="height:38px">`

### 2. Phone Number
- [ ] Search all files for `(555) 555-1234` and `+15555551234`
- [ ] Replace with the real phone in both display format AND `tel:` link format
- [ ] Locations: header nav (every page), hero section (homepage), CTA bands (multiple pages), footer (every page)

### 3. Email Address
- [ ] Search all files for `hello@sunbeltplumbing.com`
- [ ] Replace with the actual business email
- [ ] Locations: footer (every page), contact page

### 4. Business Address & Service Area
- [ ] Open `contact.html`, find the "Service Area" contact info block
- [ ] Update with real cities served
- [ ] Search all files for `Phoenix, Scottsdale, Mesa` and update wherever it appears

### 5. Google Maps Embed
- [ ] Open `contact.html`, find the `<iframe class="map-embed" ...>` element
- [ ] Go to [Google Maps](https://maps.google.com), search the business address
- [ ] Click **Share → Embed a map → Copy HTML**
- [ ] Replace the entire `<iframe>` with the new one (keep `class="map-embed"`)

### 6. Services List
- [ ] Open `services.html`
- [ ] Each service is in a `<div class="service-detail">` block — edit the `<h3>` and `<p>` to match the client's actual offerings
- [ ] Add new services by copying any `<div class="service-detail">` block; remove ones they don't offer
- [ ] Also update the **homepage services overview** (`index.html`, find the `services-grid` section) to match — keep it to 6 highlights
- [ ] Update the **quote form's service dropdown** in `quote.html` (find `<select id="service">`) so it matches

### 7. Photo Gallery
- [ ] Drop client's job photos into `assets/images/` (e.g., `job-01.jpg`, `job-02.jpg`)
- [ ] Open `gallery.html`, find each `<div class="gallery-item">` block
- [ ] Replace `src="https://images.unsplash.com/..."` with `src="assets/images/job-01.jpg"`
- [ ] Update the `alt`, `<h4>`, and `<p>` text to describe the actual job
- [ ] **Tip:** For best performance, resize photos to ~1200px wide and save as JPG before uploading
- [ ] Categories available: `repair`, `install`, `remodel` — set in `data-category="..."` to enable filter buttons

### 8. Testimonials
- [ ] Open `index.html`, find the `testimonials-grid` section
- [ ] Replace placeholder quotes with real reviews from Google, Yelp, or Facebook
- [ ] Update `testimonial-name`, `testimonial-meta`, and `testimonial-avatar` (initial letter) for each

### 9. Social Media Links
- [ ] Search all files for `<a href="#" aria-label="Facebook">` and `<a href="#" aria-label="Instagram">`
- [ ] Replace `href="#"` with the actual social profile URLs
- [ ] If the client doesn't have one of these accounts, delete that `<a>` block
- [ ] To add other platforms (TikTok, YouTube), copy an existing block and swap the SVG icon

### 10. Business Hours
- [ ] Open `contact.html`, find the "Hours" contact info block
- [ ] Update days/times to match actual operating hours

### 11. Form Endpoints (Formspree)
- [ ] See `README.md` → "Setting Up the Contact Forms" for full instructions
- [ ] Search `quote.html` and `contact.html` for `YOUR_FORM_ID` and replace with real Formspree ID

---

## 🔍 How to Find All Placeholders Fast

In your code editor (VS Code, Sublime, etc.), do a project-wide search for:

```
REPLACE ME
```

This will list every spot that needs updating, with the file and line number. Work through them one by one.

You can also search for specific placeholder values like:
- `(555) 555-1234` — all phone number instances
- `hello@sunbeltplumbing.com` — all email instances
- `YOUR_FORM_ID` — Formspree placeholders
- `Unsplash` (in image URLs) — placeholder gallery images

---

## 📷 Image Optimization Tips

For fast page loads:
- **Logo:** PNG with transparent background, max 200px wide
- **Job photos:** JPG, ~1200px wide, compressed to ~150–250 KB each
- Use a free tool like [TinyPNG](https://tinypng.com) or [Squoosh](https://squoosh.app) to compress before uploading

---

## ❓ Need Help?

If anything breaks or looks off after a content swap, the most common causes are:
1. **Broken image link** — double-check the file path and spelling
2. **Missing closing tag** — make sure every `<div>` you edit still has a matching `</div>`
3. **Form not sending** — verify your Formspree form ID is correct and you've confirmed the email Formspree sent on signup

For anything else, contact RDahunan IT Services.
