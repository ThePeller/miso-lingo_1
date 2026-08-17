# Miso-Lingo

Interactive prototype for **Miso-Lingo** ("Duolingo for Misogyny"), a proactive concept for TIFF Share Her Journey. A flashcard course in the real reasons women-led films get rejected — official studio note on the front, the actual reason underneath.

This is a static, single-page prototype. No build step, no dependencies — just HTML, CSS, and two logo assets.

## Structure

```
.
├── index.html            # the whole site
├── logo-stacked.png      # landing page hero lockup
├── logo-horizontal.png   # header lockup (interior pages)
└── README.md
```

All files sit flat in the repo root — no subfolders. This was a deliberate simplification to avoid folder-upload issues in GitHub's web UI; if you're pushing via `git` from the command line, folders work fine either way.

## Local preview

Open `index.html` directly in a browser, or serve it locally:

```
npx serve .
```

## Deploying to Vercel

**Option A — Vercel dashboard (no CLI needed)**
1. Push this repo to GitHub (see below).
2. Go to [vercel.com/new](https://vercel.com/new) and import the GitHub repo.
3. Framework preset: **Other** (it's static — no build command, no output directory needed).
4. Deploy.

**Option B — Vercel CLI**
```
npm i -g vercel
vercel
```
Follow the prompts. No project configuration is required; Vercel auto-detects the static `index.html`.

## Pushing this to GitHub

From this folder:

```
git init
git add .
git commit -m "Miso-Lingo prototype"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

(Replace `<your-username>/<repo-name>` with wherever you create the empty repo on GitHub first.)

## Notes for whoever picks this up next

- The donate button on every screen links to `https://tiff.net/donate/share-her-journey`.
- All 20 flashcard pairs are hardcoded in the `REASONS` array near the bottom of `index.html` — no CMS, no data file. Easiest place to edit copy.
- Colors, type, and layout are locked to the approved keyframes (cream `#FAF7F0`, red `#EA3325`, black `#141414`; Fredoka for display type, Archivo for labels/body).
- The small pill nav fixed to the top of the page (labeled "wireframe nav") is a dev/QA convenience for jumping between screens without clicking through the flow — remove it before this goes anywhere client-facing as a final build.
