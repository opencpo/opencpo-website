# OpenCPO Website

The landing page for [OpenCPO](https://github.com/opencpo/opencpo) — the first complete open source EV charging platform.

## Deploy Anywhere

Static site. No build step. No framework. Just files.

```bash
# Serve locally
npx serve .
# or
python3 -m http.server 8000
# or
php -S localhost:8000
```

## Structure

```
opencpo-website/
├── index.html    # Everything — all sections, all JS
├── style.css     # All styles
├── favicon.svg   # SVG icon (works everywhere)
└── README.md     # This file
```

## Sections

1. **Hero** — Big headline, CTAs, animated gradient background
2. **The Stack** — 5 component cards with hover effects
3. **Why OpenCPO** — Complete / Open / Battle-tested
4. **Quick Start** — 3-command terminal demo
5. **Architecture** — SVG diagram of component connections
6. **Features** — 12-item feature grid
7. **Community** — Discord, GitHub Discussions, newsletter
8. **Footer** — Links, license, attribution

## Deployment Options

**Netlify/Vercel:** Drop the folder. Done.

**GitHub Pages:**
```bash
# Enable in repo settings → Pages → source: main branch / root
```

**Nginx:**
```nginx
server {
    listen 80;
    server_name opencpo.org;
    root /var/www/opencpo-website;
    index index.html;
}
```

**Docker:**
```dockerfile
FROM nginx:alpine
COPY . /usr/share/nginx/html
```

## Customization

Update links from `github.com/opencpo/*` placeholders once the GitHub org is created.

Find/replace `github.com/opencpo` across both `index.html` to update all links at once.

## License

Apache 2.0 — same as OpenCPO itself.

---

Made by [Stroomlijnen B.V.](https://stroomlijnen.nu)
