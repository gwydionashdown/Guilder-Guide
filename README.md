# Guilder Guide — website

Static site for **guilderguide.com** — _"Dutch money, explained for expats."_

## What's here
- `index.html` — the Box 3 tax calculator (currently the homepage)
- `netlify.toml` — hosting config (security headers; future redirect)
- `robots.txt` / `sitemap.xml` — search-engine basics
- `README.md` — this file

## How it's hosted
Hosted on **Netlify**, connected to this repository. Every change pushed
here deploys automatically. There is no build step — it's plain HTML/CSS/JS.

## Adding a new calculator later
1. Add a folder, e.g. `pension/` with its own `index.html`.
2. Add the new URL (e.g. `https://guilderguide.com/pension/`) to `sitemap.xml`.
3. Commit — it goes live automatically at guilderguide.com/pension/.

## Building a real homepage later
When you want guilderguide.com to be a homepage that links to several tools:
1. Move the calculator into a `box3/` folder.
2. Put the new homepage at `index.html`.
3. Uncomment the `/` → `/box3/` redirect in `netlify.toml` so old links survive.

## Updating the 2026 figures
Edit the values in the "2026 figures & assumptions" block inside `index.html`,
commit, and the change is live within a minute.
