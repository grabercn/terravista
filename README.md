# Terra Vista

A simple static website for Terra Vista (custom pergolas), hosted free on **GitHub Pages** at **https://terravista.living**.

Plain HTML, no build step. Edit `index.html` and push to `main` — the GitHub Actions workflow redeploys automatically.

## What your dad needs to add at Hostinger (one time)

In Hostinger: **Domains → terravista.living → DNS / Nameservers**, and add these records so the domain points at GitHub Pages.

**Four A records** (the apex/root domain):

| Type | Name / Host | Points to        |
|------|-------------|------------------|
| A    | `@`         | `185.199.108.153`|
| A    | `@`         | `185.199.109.153`|
| A    | `@`         | `185.199.110.153`|
| A    | `@`         | `185.199.111.153`|

**One CNAME** (so `www.terravista.living` works too):

| Type  | Name / Host | Points to             |
|-------|-------------|-----------------------|
| CNAME | `www`       | `grabercn.github.io` |

Notes:
- If Hostinger already created default `A` or `CNAME` records for `@`/`www`, delete those first so they don't conflict.
- DNS can take anywhere from a few minutes to a few hours to take effect. GitHub then issues a free HTTPS certificate automatically.

## Editing the site
- All the text lives in `index.html` (look for the `EDIT` comments).
- Images are in `images/`. Swap a file (keep the same name) to change a photo.
- The contact email is `hello@terravista.living` — set that mailbox up in Hostinger, or change it in `index.html`.

Photos: Pexels (Max Vakhtbovych, Matheus Bertelli, Natalia Chiciuc, Maria Orlova).
