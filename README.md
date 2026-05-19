# Trio Tales Adventures

This project is now named `Trio Tales Adventures` and is ready to be checked in to GitHub and deployed to Netlify.

Applied quick accessibility, SEO and robustness fixes to `index.html`:

- Added `meta description`, Open Graph tags and `favicon` link.
- Added `rel="noopener noreferrer"` to external `target="_blank"` anchors.
- Added `loading="lazy"` to images (hero, polaroids, gallery, vlog thumbnails).
- Connected form `label` elements to inputs and added `id` + `name` attributes for form fields.
- Added basic ARIA attributes to the modal and simple focus preservation on open/close.
- Replaced an inline clickable `div` with an accessible `button` for the hero thumbnail.
- Made vlog cards keyboard-accessible (`role="button"`, `tabindex`, `onkeydown` handler).

Missing/local assets to add to the project (place in this folder):
- `family.jpeg`
- `amaani.jpeg`
- gallery images referenced in the `BASE_GALLERY` array (e.g. `Secrets Day1.jpeg`, `Secrets Day2.JPG`, etc.)
- `favicon.ico` (optional)

The following improvements were also completed in this commit:
- Added a small focus-trap for the modal and focus restoration logic.
- Extracted inline CSS to `styles.css`.
- Added Netlify-friendly form handling attributes and a honeypot field.
 
Additional options if you want to extend the project:
- Add a lightweight server-side form handler or API endpoint.
- Optimize the local gallery assets with `srcset` and compressed images.
- Add Lighthouse-based CI for performance and SEO scoring.
 
Completed extra improvements in this commit:
- Extracted inline CSS to `styles.css` and linked it from `index.html`.
- Added JSON-LD structured data for `Organization` and the main `VideoObject`.
- Added Netlify form attributes (`data-netlify`) and a honeypot field for spam protection.
- Implemented a simple modal focus-trap and focus restoration logic.
- Added `sitemap.xml` and `robots.txt` (update hostnames as needed).
- Added a basic GitHub Actions workflow at `.github/workflows/ci.yml` that runs `html-validator-cli` and `pa11y-ci`.
- Included a commented Plausible analytics snippet and a simple opt-in/opt-out helper.

Notes:
- Replace `http://example.com/` in `sitemap.xml` with your real site URL before submitting to search consoles.
- The CI installs dependencies from `package.json` and runs validation scripts with npm.
- I added lightweight checks and conservative defaults — we can extend them (Lighthouse, image optimization) next.

## Deploying to GitHub + Netlify

Recommended GitHub repo name: `trio-tales-adventures`

1. Initialize git:
   ```bash
   git init
   git add .
   git commit -m "Rename project to Trio Tales Adventures and add Netlify/GitHub config"
   ```
2. Add your GitHub remote and push:
   ```bash
   git remote add origin git@github.com:youruser/trio-tales-adventures.git
   git branch -M main
   git push -u origin main
   ```
3. Link this repo in Netlify (or run `netlify deploy` if using Netlify CLI).

The project includes:
- `netlify.toml` for static publish settings
- `.gitignore` for common ignores
- `package.json` for dev tooling and validation scripts
- `sitemap.xml` and `robots.txt` for SEO
- Basic CI workflow in `.github/workflows/ci.yml`

Run the local server and open http://127.0.0.1:8000 to preview the changes.
