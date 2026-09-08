# Carlee & Garrett

Static wedding site (Webflow export) for [carleeandgarrett.com](https://carleeandgarrett.com).

No build step. HTML, CSS, JS, and images in the repo root are the site.

## Local preview

```bash
npx wrangler pages dev .
```

## GitHub

This repo is ready to push. From the project root:

```bash
gh auth login
gh repo create carleeandgarrett --source=. --public --remote=origin --push
```

Use `--private` instead of `--public` if you do not want the source photos on GitHub.

## Cloudflare Pages

After the repo is on GitHub:

1. Open [Workers & Pages](https://dash.cloudflare.com/?to=/:account/workers-and-pages)
2. **Create** → **Pages** → **Connect to Git**
3. Select the `carleeandgarrett` repository
4. Use these build settings:
   - Framework preset: **None**
   - Build command: *(leave empty)*
   - Build output directory: `/`
   - Production branch: `main`
5. **Save and Deploy**

Wrangler is also set up if you want a direct upload instead of Git:

```bash
npx wrangler pages deploy . --project-name=carleeandgarrett
```

Custom domain: in the Pages project, **Custom domains** → add `carleeandgarrett.com` (and `www` if you use it).
