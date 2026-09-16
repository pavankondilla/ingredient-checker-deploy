# Ingredient Safety Checker

A free, no-signup tool to check cosmetics and food ingredient labels for
commonly flagged chemicals and additives. Runs entirely in the browser —
no backend, no database, nothing to crash under load.

## Files in this folder

- `index.html` — the complete app (HTML + CSS + JS in one file)
- `vercel.json` — deployment config for Vercel
- `package.json` — project metadata

## Deploy in 3 Steps (fastest: Vercel, free)

### Option A — Vercel CLI (2 minutes)
```bash
npm install -g vercel
cd ingredient-checker-deploy
vercel login
vercel --prod
```
Vercel will print a live URL when done, e.g. `https://ingredient-safety-checker.vercel.app`

### Option B — Drag and drop (no command line)
1. Go to https://vercel.com
2. Sign up / log in (free)
3. Click "Add New Project" → "Upload"
4. Drag this whole folder in
5. Click Deploy

### Option C — Netlify (alternative, also free)
1. Go to https://app.netlify.com/drop
2. Drag this folder onto the page
3. Live URL appears instantly

## Test Locally Before Deploying (optional)
```bash
npx serve .
```
Then open the printed local URL (usually http://localhost:3000) in your browser.

## Verified Before Packaging
- HTML tags balanced (html/head/body/div/script/style)
- JavaScript syntax validated with `node --check` — no syntax errors
- vercel.json and package.json validated as proper JSON

## What This App Does
- **Cosmetics tab**: paste an ingredient list, flags substances like
  parabens, phthalates, triclosan, and synthetic fragrance with risk levels
  (low / moderate / high / critical)
- **Food tab**: paste an ingredient list including INS/E-numbers in
  brackets (e.g. "Antioxidant (320)") — auto-extracts and checks those
  codes against a database of commonly flagged food additives

## Limitations (be upfront about this with users)
This checker only covers a curated list of commonly-flagged substances.
A "no flagged ingredients" result means nothing in this specific list
matched — it does not certify the product as 100% safe. This is an
informational tool, not a medical or regulatory safety certification.
