# mitrajparmar93.github.io

Personal site for Mitraj Parmar. One static page, no build step, no dependencies. Fonts load from Google Fonts. Everything else (the globe, the charts, the land map data) is inline in `index.html`.

## What's in here

| File | What it's for |
|---|---|
| `index.html` | The whole site |
| `404.html` | Shown by GitHub Pages for any missing URL |
| `og-image.png` | Preview card shown when the link is shared on LinkedIn, Slack, iMessage and similar |
| `favicon.svg`, `apple-touch-icon.png` | Browser tab and home-screen icons |
| `robots.txt`, `sitemap.xml` | Help search engines find the page |
| `.nojekyll` | Tells GitHub Pages to serve the files as-is |

## Preview locally

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000. Opening `index.html` directly also works.

## Publish on GitHub Pages

The repo must be named exactly `mitrajparmar93.github.io` for the site to live at https://mitrajparmar93.github.io.

```sh
cd mitrajparmar93.github.io
git init -b main
git add .
git commit -m "Launch personal site"
gh repo create mitrajparmar93.github.io --public --source=. --remote=origin --push
```

Then on GitHub, open the repo's **Settings → Pages** and confirm the source is **Deploy from a branch**, branch `main`, folder `/ (root)`. The site is usually live within a minute or two.

No `gh`? Create an empty public repo named `mitrajparmar93.github.io` on github.com, then:

```sh
git remote add origin https://github.com/mitrajparmar93/mitrajparmar93.github.io.git
git push -u origin main
```

## Updating

Edit `index.html`, commit and push. GitHub Pages redeploys on every push to `main`.

## Using a custom domain later

1. Add a file named `CNAME` containing just the domain, for example `mitrajparmar.com`.
2. Point the domain's DNS at GitHub Pages (Settings → Pages shows the exact records).
3. Replace `https://mitrajparmar93.github.io/` with the new address in `index.html` (canonical link, `og:url`, `og:image`, `twitter:image` and the JSON-LD `url`), `robots.txt` and `sitemap.xml`.

## Privacy

This repo is public. Keep it to what's already on the page: no internal documents, metrics, project names or anything from work that isn't already on LinkedIn.
