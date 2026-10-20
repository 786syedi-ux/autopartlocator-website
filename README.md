# Autopart Locator

Static website for selling used car and HTV parts. Customers browse the catalogue and place orders on WhatsApp.

## Files
- `index.html` – customer site (catalogue, order form, Terms & Conditions)
- `parts.js` – list of parts and categories (edit to add or rename parts)
- `prices.json` – WhatsApp number, prices and photo paths (the file you update most)
- `admin.html` – private helper to edit prices and download a new `prices.json`
- `images/` – part photos

## Publish on GitHub Pages
1. Create a new GitHub repository and upload all these files (keep `images/`).
2. Settings → Pages → Source: *Deploy from a branch* → `main` / root → Save.
3. Your site will be live at `https://<username>.github.io/<repo>/`.

## Update prices
1. Open `admin.html` (locally or on the live site at `/admin.html`), set prices and the WhatsApp number.
2. Click **Download prices.json**, then replace `prices.json` in the repo (Add file → Upload files, or edit it on GitHub) and commit.
3. Each commit is tracked in the repo history, so you can see and roll back price changes.

You can also edit `prices.json` directly on GitHub. Part IDs are listed in `parts.js` order; `admin.html` handles this for you.

## Notes
- `admin.html` is not password protected and cannot change the live site; only someone with write access to your repo can. Use a private repo plus a custom domain if you prefer to hide it.
- Add photos you own or have rights to use under `images/`, then enter their path in admin.
- Review the Terms & Conditions with a legal advisor before going live.
