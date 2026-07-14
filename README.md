# Roina Tours

Marketing site for Roina Tours — educational travel programs across China (Xi'an, Shanghai, Beijing, Chongqing). Plain HTML/CSS/JS, no build step, hosted on GitHub Pages.

## Structure

```
.
├── index.html                  Home
├── about.html                  About Us / team
├── products.html               Destination programs (Xi'an, Shanghai, Beijing, Chongqing)
├── smart-model.html            SMART learning model / approach
├── contact.html                Contact details
├── privacy-policy.html         Privacy policy
├── terms-and-conditions.html   Fees, refund policy, participation notes, FAQ
├── css/
│   └── style.css               Single stylesheet (passport / postcard / travel-journal theme)
├── js/
│   └── main.js                 Mobile nav toggle
└── images/
    ├── logo-mark.png           Site logo (header + footer)
    ├── XIAN-photo.png
    ├── SHA-photo.png
    ├── BEIJING-photo.png
    └── CHQ-photo.png
```

Every page shares the same `<header>` and `<footer>` markup, copied from `index.html`:

- **Header**: logo (`images/logo-mark.png`) + nav links (About Us / Products / SMART Model / Contact Us), with `aria-current="page"` set on the link matching the current page, a language toggle, and a mobile menu button.
- **Footer**: brand blurb, About / Privacy / Social link columns, and a copyright line. The Privacy and Social links point to the real pages and social profiles (not placeholders).

`js/main.js` toggles the `.open` class on `.nav-links` when `.nav-toggle` is clicked, for the mobile menu — this is shared across all pages and needs no per-page changes.

## Content status

Most page bodies are still placeholder copy/images (marked `[ ... ]` or described as "placeholder" in the HTML) and need real content:

- `about.html` — team bios and photos
- `smart-model.html` — actual SMART framework description
- `products.html` — full per-city program details (duration, itinerary, pricing)
- `index.html` — hero image

`privacy-policy.html`, `terms-and-conditions.html`, and `contact.html` have real copy already.

## Local development

No build tools required — open `index.html` directly in a browser, or serve the folder with any static file server, e.g.:

```bash
python3 -m http.server
```

## Deployment

Static site, hosted on GitHub Pages directly from this repo.

## Recent changes

- Standardized header/footer markup across all pages to match `index.html` (logo image instead of a text "R" mark on the Terms and Privacy pages; real Privacy and Social links in the footer instead of `#` placeholders; removed the extra "Built with plain HTML..." footer line for consistency).