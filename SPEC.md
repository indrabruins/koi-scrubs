# KOI Scrubs — GitHub Pages Deploy — SPEC

## Problem
KOI / koi Designer Scrubs is a print-on-demand apparel brand (via Printful) with no live storefront. The `operations/pod-store/` directory has a built HTML storefront but it's not deployed.

## Solution
1. Audit the existing `operations/pod-store/` HTML file
2. Fix any broken links, images, or resources
3. Deploy to GitHub Pages at `https://indrabruins.github.io/koi-scrubs/`
4. Wire up Printful storefront embed or product links
5. If the store is too basic, build a clean single-product landing page for the first product (scrubs/medical apparel)
6. Set up GitHub Actions CI/CD — push to `main` auto-deploys

## Technical Approach
- Target repo: create `indrabruins/koi-scrubs` on GitHub (or use existing)
- GitHub Pages from `main` branch `/docs` or root
- Single HTML file with embedded CSS (or minimal assets)
- Printful embed: `https://printiful.com/store/{store-id}/embed`
- GitHub Actions: `peaceiris/actions-gh-pages@v4`

## Files
- `index.html` — storefront (rebuild if current one is broken)
- `README.md` — store URL + update instructions
- `.github/workflows/deploy.yml` — CI/CD

## Success Criteria
- Store live at `https://indrabruins.github.io/koi-scrubs/`
- Products visible without login
- Deploys automatically on push to main
