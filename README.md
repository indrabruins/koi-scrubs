# KOI Designer Scrubs

**Live Storefront:** https://indrabruins.github.io/koi-scrubs/

Print-on-demand medical apparel brand built with love (and GitHub Pages).

---

## How to Update Products

1. Edit `index.html` — update product name, price, description, or image URL inside the `#products` section.
2. Commit your change:
   ```bash
   git add index.html
   git commit -m "feat: update product pricing"
   git push origin main
   ```
3. GitHub Actions automatically deploys your change to the live URL within ~2 minutes.

---

## How to Connect Printful

1. Set up your Printful store and add products.
2. In `index.html`, replace `https://printiful.com` in each `.btn-shop` link with your actual Printful product URL (e.g. `https://printful.com/store/YOUR-STORE/item/SLUG`).
3. If using Printful's storefront embed, replace the entire `#products` section with:
   ```html
   <iframe src="https://printiful.com/store/YOUR-STORE-ID/embed" width="100%" height="900" frameborder="0"></iframe>
   ```
4. Commit and push — live site updates automatically.

---

## CI/CD

Every push to `main` automatically triggers the GitHub Actions workflow which deploys the site to GitHub Pages. No manual steps required.

**Workflow file:** `.github/workflows/deploy.yml`

---

## Local Development

To preview locally:
```bash
open http://localhost:8000  # or any static server
python -m http.server 8000
```
