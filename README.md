# adoption.ae

Landing page for the AI Consulting practice (Imad / Alex Reid side business — operator collective with George Eid).

**Live:** https://adoption.ae · **Backup:** https://adoption-ae.pages.dev

## How it works

Single-file HTML site. Hosted on Cloudflare Pages. Push to `main` → auto-deploys in ~30s.

```
.
├── index.html           # the whole site
├── 404.html             # mirror of index.html (single-page site)
├── _headers             # security + caching headers (Cloudflare Pages convention)
├── og.png               # social preview image
├── apple-touch-icon.png # iOS home-screen icon
├── llms.txt             # AI crawler hints
├── robots.txt
├── sitemap.xml
└── README.md
```

## Edit & deploy

```bash
# Clone (one-time)
git clone https://github.com/georgeeid008-boop/adoption-ae.git
cd adoption-ae

# Edit (Claude Code, Codex, your editor — whatever)
# ...

# Ship
git add .
git commit -m "what you changed"
git push origin main
# Cloudflare auto-deploys. Refresh https://adoption.ae in ~30s.
```

Every branch other than `main` gets its own preview URL automatically — e.g. `https://<branch>.adoption-ae.pages.dev` — handy for showing something before merging.

## Collaborators

- George Eid (georgeeid008-boop) — owner
- Imad (handle TBD) — collaborator

## Cloudflare details

- Account: `f17007e7ae3f9a71da3703bfb10c0eef`
- Pages project: `adoption-ae`
- Zone: `adoption.ae` (Zone ID `d2c95dad911f2c44e96ba21d346c0de2`)
- Registrar: tasjeel.ae (NS pointed to `ezra` + `raphaela.ns.cloudflare.com`)

Build settings inside Cloudflare Pages: **build command = none**, **output dir = `/`** (root of repo). No framework.
