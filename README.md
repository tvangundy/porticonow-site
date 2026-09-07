# porticonow-site

Essay site for [porticonow.com](https://porticonow.com) — a plain case for keeping personal data at home. Top-of-funnel; product onboarding lives at [web.porticoworks.dev](https://web.porticoworks.dev).

## Update the site

- Essay copy: `index.html`
- Layout and typography: `styles.css`
- Brand mark: `logo.png`; tab icons: `favicon-*.png`, `apple-touch-icon.png`

No build tools. Open `index.html` in a browser to preview.

## Publish on GitHub Pages

1. Repository: `tvangundy/porticonow-site` (public), branch `main`.
2. **Settings → Pages** → Deploy from a branch → `main` / `/(root)`.
3. **Custom domain:** `porticonow.com` (keep the `CNAME` file in the repo).
4. After DNS is healthy, enable **Enforce HTTPS**.

## GoDaddy DNS for porticonow.com

In GoDaddy: **My Products → Domains → porticonow.com → DNS**. Remove domain-forwarding and conflicting `@` / `www` records, then add:

| Type | Name | Value | TTL |
| --- | --- | --- | --- |
| A | @ | 185.199.108.153 | 1 hour |
| A | @ | 185.199.109.153 | 1 hour |
| A | @ | 185.199.110.153 | 1 hour |
| A | @ | 185.199.111.153 | 1 hour |
| CNAME | www | tvangundy.github.io | 1 hour |

Do not add a wildcard (`*`) record. Propagation can take up to 24 hours.

## Related sites

| URL | Repo | Role |
| --- | --- | --- |
| porticonow.com | this repo | Essay / why home data |
| web.porticoworks.dev | ws-website | Product + onboarding |
| porticoworks.dev | porticoworks-site | Company + legal |
