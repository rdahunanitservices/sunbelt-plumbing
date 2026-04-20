# Sunbelt Plumbing — Website

Production website for Sunbelt Plumbing, a family-operated plumbing business in Arizona.

**Built by:** RDahunan IT Services
**Tech:** Static HTML / CSS / vanilla JavaScript (no build step, no dependencies)

---

## 📁 File Structure

```
sunbelt-plumbing/
├── index.html          → Home page
├── services.html       → Services list
├── quote.html          → Quote request form
├── gallery.html        → Photo gallery (filterable)
├── contact.html        → Contact info + form + map
├── css/
│   └── style.css       → All styling
├── js/
│   └── script.js       → Nav toggle, gallery filter, form handling
├── assets/
│   └── images/         → Drop client logo and job photos here
├── CONTENT_UPDATES.md  → Guide for swapping placeholder content with real client content
└── README.md           → This file
```

---

## 🚀 Deploying to GitHub Pages

1. Create a new GitHub repository (e.g., `sunbelt-plumbing`)
2. Push all files to the `main` branch
3. Go to **Settings → Pages**
4. Under "Source", select **Deploy from a branch**
5. Choose `main` branch and `/ (root)` folder
6. Click **Save**
7. Site will be live at: `https://YOUR-USERNAME.github.io/sunbelt-plumbing/`

To use a custom domain (e.g., `sunbeltplumbing.com`), follow [GitHub's custom domain guide](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

---

## ⚙️ Setting Up the Contact Forms (Formspree)

The quote form (`quote.html`) and contact form (`contact.html`) use [Formspree](https://formspree.io) for submission handling — required for static sites with no backend.

**Setup steps:**

1. Sign up for a free Formspree account at https://formspree.io
2. Create a new form (the free plan allows 50 submissions/month)
3. Copy your form endpoint (looks like: `https://formspree.io/f/xpzgkqyl`)
4. Open `quote.html` and `contact.html`
5. Find every instance of `https://formspree.io/f/YOUR_FORM_ID` and replace `YOUR_FORM_ID` with your actual ID
6. Test by submitting a form — Formspree will send the submission to the email you registered with

> 💡 You can use the same form ID for both pages, or create separate forms to track quote requests vs. general inquiries.

---

## 🎨 Replacing Placeholder Content

See **`CONTENT_UPDATES.md`** for the complete checklist of what to replace and how. Every placeholder in the code is marked with a `<!-- REPLACE ME -->` comment so you can find them with a quick search.

---

## 📱 Browser Support

Tested on: Chrome, Firefox, Safari, Edge (latest 2 versions).
Mobile-responsive at 375px (iPhone) through 1280px+ (desktop).

---

## 🔧 Local Development

No build tools needed. Just open `index.html` in a browser, or run a simple local server:

```bash
# Python 3
python3 -m http.server 8000

# Node.js (if you have npx)
npx serve
```

Then visit `http://localhost:8000`.

---

© 2026 RDahunan IT Services. Built with care for Sunbelt Plumbing.
