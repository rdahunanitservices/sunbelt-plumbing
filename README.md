# Sunbelt Plumbing — Website

Production website for Sunbelt Plumbing, a family-operated plumbing business in Arizona.

**Built by:** RDahunan IT Services
**Tech:** Static HTML / CSS / vanilla JavaScript (no build step, no dependencies)

---

## ✅ What's Already Real (no edits needed)

The following client information is already baked into every page:

- **Phone:** (480) 527-5385
- **Email:** shan@sunbeltplumbingaz.com
- **License:** ROC #344103 (badge displayed on every page)
- **Service Areas:** Maricopa, Pinal & Pima counties (Arizona City, Casa Grande, Maricopa, Phoenix, Tucson)
- **Real services list:** All 9 services match Sunbelt's actual offerings
- **Facebook Messenger chat widget:** Floating button on every page → opens m.me/SunbeltPlumbingLLC
- **Footer Facebook link:** Points to fb.com/SunbeltPlumbingLLC
- **Real tagline:** "We handle the pressure so you don't have to"
- **Brand colors:** Blue + Yellow/Gold (matches existing Sunbelt brand)

## 🔲 What Still Needs Princess's Real Content

- **Logo image:** Currently shows "SP" letter mark. Drop her real logo PNG into `images/logo.png` and update the logo `<a>` tags in all HTML files
- **Photo gallery:** Currently uses Unsplash placeholder photos. Replace with real job photos in `images/` and update `gallery/index.html`
- **Testimonials:** 3 sample testimonials on homepage. Replace with real Google/Facebook reviews
- **Formspree form ID:** Sign up at formspree.io and replace `YOUR_FORM_ID` in quote/index.html and contact/index.html

See `CONTENT_UPDATES.md` for step-by-step instructions on each.

---

## 📁 File Structure

```
sunbelt-plumbing/
├── index.html              → Home page         → loads at  /
├── services/index.html     → Services list     → loads at  /services/
├── quote/index.html        → Quote form        → loads at  /quote/
├── gallery/index.html      → Photo gallery     → loads at  /gallery/
├── contact/index.html      → Contact + map     → loads at  /contact/
├── css/
│   └── style.css           → All styling
├── js/
│   └── script.js           → Nav toggle, gallery filter, form handling
├── images/                 → Drop client logo and job photos here
├── CONTENT_UPDATES.md      → Guide for swapping placeholder content
└── README.md               → This file
```

## 🔗 Clean URLs

This site uses **folder-based clean URLs** — visitors see `/services/` instead of `/services.html`. This is more professional and SEO-friendly. All internal links use root-relative paths with the `/sunbelt-plumbing/` prefix (the GitHub Pages subpath).

**⚠️ If you change the repo name or move to a custom domain, update the `BASE_PATH` in all HTML files.**

Quick global replace example (using the GitHub web editor or your code editor):
- For a custom domain like `sunbeltplumbing-az.com`: replace `"/sunbelt-plumbing/` with `"/`  in all .html files
- For a different repo name: replace `"/sunbelt-plumbing/` with `"/your-new-repo-name/` in all .html files

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
