# Project Context — Caffe Primo Firle "Under Renovation" Page

## What this is
A single-page static website (`index.html`) acting as a temporary **"under
renovation / coming soon"** landing page for **Caffe Primo Firle**, an Italian
restaurant on Glynburn Rd, Firle SA 5070 (part of the Caffe Primo family of
restaurants). It is served at https://caffeprimofirle.com.au/ and is hosted via
GitHub Pages (a `CNAME`, `sitemap.xml`, `robots.txt`, and a Google site
verification file are present in the repo).

## What it does
- Tells visitors the venue is temporarily closed for renovation and will
  "be back soon," while keeping the brand visible to search engines.
- Shows a preview gallery of architectural renders of the refreshed interior
  and exterior so customers know what to expect.
- Surfaces the key practical details: location, reopening status, and a phone
  contact (`tel:` link to 0450 950 083).
- Is built for SEO/social sharing: canonical URL, meta description, Open Graph
  and Twitter Card tags, Google site verification, and an inline SVG favicon.

## How it looks (visual design)
A warm, editorial, fine-dining aesthetic. Everything is self-contained — all
CSS is inline in a `<style>` block, no JavaScript, no external CSS frameworks.

**Color palette** (CSS variables in `:root`):
- Espresso `#2A3020` / dark brown `#1E2518` — dark backgrounds
- Cream `#F2EDE3` / warm white `#F8F5EF` — text and the light editorial section
- Sage greens `#5C7A3E` / `#7A9C58` — accents
- Gold `#B8A96A` / gold light `#D4C98A` — luxury accents, rules, ornaments

**Typography**: Google Fonts — *Cormorant Garamond* (elegant serif, used italic
for headings/taglines) and *DM Sans* (clean sans-serif for labels/body).

**Page sections (top to bottom):**
1. **Hero** — Full-height espresso-colored banner, centered. Contains an
   "Under Renovation" eyebrow, the gold Primo Firle logo image
   (`assets/primo-firle-logo.png`) with a soft gold drop-shadow, the tagline
   *"Italian dining for the whole famiglia,"* and *"Refreshing your favourite
   local. Back soon."* Decorative touches: a radial gold halo glow behind the
   logo, a faint hand-drawn marble-vein SVG overlay, an animated film-grain
   texture, a top-right "GLYNBURN RD / FIRLE · SA" corner lockup (desktop only),
   and a bottom-left hand-drawn olive-sprig SVG ornament.
2. **Editorial / renovation** — Light (warm white) section. Centered header
   ("A Taste of What's Coming" / "A *fresh* chapter") above a responsive image
   gallery of three renders (interior, arches, exterior) using `<picture>` with
   WebP + JPG fallbacks. Images are intentionally slightly blurred. Credited
   "Renders by ACDESIGN."
3. **Info band** — Dark section with a 3-column grid: Location, Reopening
   ("Coming soon"), and Contact (phone). Columns are divided by thin gold rules.
4. **Footer** — "Primo Firle" wordmark, "Part of the Caffe Primo family of
   restaurants," and a 2026 copyright line.

## Responsiveness & accessibility
- Mobile-first with breakpoints at 640px, 768px, and 1024px. The gallery goes
  from 1 column → 3 columns → an asymmetric 3-column layout; the info band
  stacks on mobile and splits into columns on tablet+.
- Uses `dvh` units, `env(safe-area-inset-bottom)` for notched devices,
  `prefers-reduced-motion` to disable the grain animation, `aria-label`/
  `aria-labelledby`, `sr-only` headings, descriptive `alt` text, and 44px
  minimum touch targets on links.

## File map
- `index.html` — the entire page (HTML + inline CSS).
- `assets/` — logo PNG and the six render images (each as `.jpg` + `.webp`).
- `CNAME`, `sitemap.xml`, `robots.txt`, `google89f30d58cb26f4f9.html` — hosting
  and SEO/verification files for GitHub Pages.
