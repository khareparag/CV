# Parag Khare · Personal Portfolio Site

A multilingual executive portfolio site for procurement, pricing and tender leadership roles. Built as a single static HTML file for easy GitHub Pages deployment.

## What is included

- `index.html` — the full site with EN / DE / FR / ZH translations, executive dark theme, all interactivity inline.
- `Khare_CV_EN.pdf` — downloadable CV (English).
- `Khare_CV_DE.pdf` — downloadable CV (German).
- `og-image.png` — 1200×630 social share card. Shown automatically when your site URL is shared on LinkedIn, X, Slack, email previews.
- `avatar.png` — 400×400 branded avatar shown in the site header. Also reusable as a profile photo placeholder.
- `linkedin-banner.png` — 1584×396 LinkedIn banner. Upload to your LinkedIn profile so your profile and site read as one brand.
- `og-image.svg`, `avatar.svg`, `linkedin-banner.svg` — editable source files. Open in any vector editor (Illustrator, Inkscape, Figma, Affinity Designer) to tweak colors or copy.
- `README.md` — this file.

## How to use the LinkedIn banner

1. Open LinkedIn → your profile.
2. Click the pencil icon on the existing banner area (top of profile).
3. Click "Change photo" → upload `linkedin-banner.png`.
4. The banner is sized to LinkedIn's exact 1584×396 spec, with the bottom-left zone left empty so your profile photo does not cover any text.

## Features

- Four-language live switcher with browser-language auto-detection (English, German, French, Simplified Chinese).
- Executive dark theme (deep navy + gold) targeted at senior recruiters.
- Hero with six big impact metrics: win-rate +15%, margin +1.7%, $8M+ deals, 68+ shippers, −20% manual effort, 12+ years.
- Career timeline with all six roles. Selected highlights per role to keep it scannable for busy executives.
- Dedicated "Availability" section using the exact target area you specified.
- Three contact paths: LinkedIn (primary), email (mailto), phone (tel://).
- Both CV PDFs downloadable from hero and contact section.
- GoatCounter analytics: cookieless, GDPR-exempt, no consent banner needed.
- Live public page-view counter visible in the footer, fed by GoatCounter.
- Mobile-responsive, print-friendly, accessible.
- SEO meta tags, Open Graph tags, favicon.

## Deploying to GitHub Pages — step by step

### 1. Create the repository

1. Sign in to GitHub.
2. Create a new repository named `YOUR-USERNAME.github.io` (replace `YOUR-USERNAME` with your actual GitHub username, for example `paragkhare.github.io`). This naming makes it a user site and gives you a clean URL.
3. Set visibility to Public.
4. Do not initialise with a README (you already have one).

### 2. Upload the files

Easiest path via the GitHub web UI:

1. On the empty repository page, click **uploading an existing file**.
2. Drag and drop all four files from this folder: `index.html`, `Khare_CV_EN.pdf`, `Khare_CV_DE.pdf`, `README.md`.
3. Commit directly to the `main` branch.

Or via git on your machine:

```bash
git init
git remote add origin https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io.git
git add .
git commit -m "Initial portfolio site"
git branch -M main
git push -u origin main
```

### 3. Enable GitHub Pages

1. Open the repository on GitHub.
2. Go to **Settings → Pages**.
3. Under "Build and deployment", set Source to **Deploy from a branch**.
4. Branch: `main`, Folder: `/ (root)`. Save.
5. Wait 1 to 2 minutes. Your site goes live at `https://YOUR-USERNAME.github.io`.

### 4. Share on LinkedIn

Add the live URL to your LinkedIn profile:
- **Contact info → Website** with label "Portfolio".
- Pin a featured post linking to it.
- Add the URL to your headline or featured section.

## Setting up GoatCounter analytics (free, cookieless, GDPR-exempt)

The site is wired for GoatCounter. No cookie consent banner needed because GoatCounter does not use cookies and does not collect personal data. This keeps the site clean and friction-free for visitors.

### 1. Create a free GoatCounter account

1. Go to https://www.goatcounter.com/signup.
2. Pick a code that becomes your subdomain (e.g. `paragkhare`). Your dashboard will live at `https://paragkhare.goatcounter.com`.
3. Email address and password. Free plan covers up to 100,000 page views per month.
4. Confirm your email and log in.

### 2. Wire your code into the site

Open `index.html` and find-replace `MYCODE` with your GoatCounter code (e.g. `paragkhare`). Two matches near the top of the file:

```html
<script data-goatcounter="https://MYCODE.goatcounter.com/count" async src="//gc.zgo.at/count.js"></script>
```

and inside the view counter function:

```js
const GC_CODE = 'MYCODE';
```

Commit and push. Tracking starts on the next page load.

### 3. Where to see your view counts

- **Public counter on the page**: bottom-right of the site footer, shows total unique visitors. Refreshes on every load.
- **Full dashboard** (only you): `https://YOURCODE.goatcounter.com`. Shows pageviews, top pages, referrers, browsers, screen sizes, locations (country level only, no IP storage), and language preferences. Real-time. Beautiful UI. No cookies.

### Why GoatCounter over Google Analytics

- No cookies, so no consent banner. Cleaner UX, faster page load.
- GDPR, PECR, CCPA exempt by design. Important for German recruiters who care about privacy.
- Lightweight: 3 KB script vs GA4's 50+ KB.
- The dashboard does not require you to log in to see your own counter, only for full analytics. You can even share the dashboard URL publicly if you want.

## Tweaks you might want to make

### Custom domain

If you buy a domain like `paragkhare.com`:

1. Add a file named `CNAME` to the repository root containing just the domain: `paragkhare.com`.
2. At your domain registrar, add these DNS A records pointing to GitHub's IPs:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
3. Add a CNAME record for `www` pointing to `YOUR-USERNAME.github.io`.
4. Wait for DNS propagation (up to 24 hours).
5. In GitHub Settings → Pages, enter your custom domain. Tick "Enforce HTTPS" once available.

### Add a professional photo

The site currently uses a "PK" monogram avatar. To swap for a real photo:

1. Add `headshot.jpg` (square, around 400×400 px) to the repository root.
2. Open `index.html` and find the `<div class="monogram">PK</div>` element in the header.
3. Replace it with `<img