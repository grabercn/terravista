# Terra Vista

A simple static website for Terra Vista (custom pergolas), hosted free on **GitHub Pages** at **https://terravista.living**.

Plain HTML, no build step. Edit `index.html` and push to `main` — the GitHub Actions workflow redeploys automatically.

## What to add at Porkbun (one time)

The domain's DNS is on **Porkbun** (`*.ns.porkbun.com`). Log in at **porkbun.com → Domain Management → terravista.living → DNS Records / Edit**, and set these so the domain points at GitHub Pages.

**First, delete Porkbun's default parking records** (the ALIAS / A record on the root, and the default `www`) so they don't conflict.

**Then add four A records** (root domain — leave the Host / Subdomain field blank):

| Type | Host    | Answer / Value    |
|------|---------|-------------------|
| A    | (blank) | `185.199.108.153` |
| A    | (blank) | `185.199.109.153` |
| A    | (blank) | `185.199.110.153` |
| A    | (blank) | `185.199.111.153` |

**And one CNAME** (so `www.terravista.living` works too):

| Type  | Host  | Answer / Value       |
|-------|-------|----------------------|
| CNAME | `www` | `grabercn.github.io` |

DNS usually updates within minutes (up to a couple hours). GitHub then issues a free HTTPS certificate automatically, and the site is live at **https://terravista.living**.

## Editing the site
- All the text lives in `index.html` (look for the `EDIT` comments).
- Images are in `images/`. Swap a file (keep the same name) to change a photo.

## Contact button (do later)
The "Email us" button points at `hello@terravista.living`, which isn't set up yet. Before sharing the site publicly, either:
- add a free email forward at **Porkbun → Email** (`hello@` → his real inbox), or
- edit `index.html` to use his real email or a phone number.

Photos: Pexels (Max Vakhtbovych, Matheus Bertelli, Natalia Chiciuc, Maria Orlova).
