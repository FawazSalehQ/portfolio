# Personal Resume Site

A single-file, static personal resume site. No build step. Drop it on Vercel and it ships.

## Deploy to Vercel — three options

### Option A — Drag-and-drop (fastest, ~30 seconds)
1. Go to **vercel.com/new**
2. Drag the entire folder onto the page
3. Click **Deploy**

That's it. Vercel auto-detects the static site, no framework config needed.

### Option B — GitHub + Vercel (recommended for ongoing edits)
```bash
git init
git add .
git commit -m "Initial resume site"
gh repo create resume-site --public --source=. --push
```
Then on **vercel.com/new**, click **Import Git Repository**, pick the repo, and deploy.

### Option C — Vercel CLI
```bash
npm i -g vercel
vercel
```
Follow the prompts. `vercel --prod` for production.

---

## Custom domain
On the Vercel dashboard → your project → **Settings → Domains** → add your domain. Vercel walks you through DNS setup.

---

## What to customize

Open `index.html` and edit in place. The main things to swap:

| Where | What to change |
|---|---|
| `<title>` and `<meta>` tags | Your name, description for SEO + social cards |
| `.mark` in the nav | Your name |
| `.hero-title` | Your headline (keep the `<span class="em">` for the gold accent words) |
| `.hero-tag` | Your one-paragraph pitch |
| `.hero-stats` | Your three signature numbers |
| `.about-prose` | Your bio (3 short paragraphs work best) |
| `.about-aside .quote` | A real testimonial |
| `.exp-list` | Your jobs — copy an `<article class="exp">` block to add more |
| `.case-grid` | Your case studies |
| `.cap-grid` | Your skill domains |
| `.philosophy blockquote` | Your guiding quote |
| `.writing-list` | Your articles / talks (optional — delete the section if not relevant) |
| `.channels` | Your real contact links |

### Color accents
The signal color (warm gold) is set once at the top of the `<style>` block:
```css
--signal: #d4a857;
```
Change that one variable to re-tint the entire site.

### Typography
Currently using **Fraunces** (serif display) + **JetBrains Mono** + **Inter**. All loaded from Google Fonts. Swap the `<link>` tag if you want different ones.

---

## Files

```
.
├── index.html       — the site (everything is here)
├── vercel.json      — minimal headers + clean URLs
└── README.md        — this file
```

No `package.json`, no build, no dependencies. By design.
