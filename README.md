# digi-tech.in — coming soon page

A single self-contained `index.html` holding page for **Digital Technologies**, a Gujarat-based B2B dealer of wide-format printing machines and inks (Ahmedabad; proprietor Kalpesh Trivedi). It sits on `digi-tech.in` while the main site is in development, and doubles as a digital visiting card: a printer-feed ink-drop intro reveals a business card that flips between a front (branding) and back (contact details + QR + Save Contact) face.

No build step, no bundler, no framework — just open `index.html` in a browser.

## File map

```
index.html                # the entire page: markup, styles, and script
assets/logo-mark.png      # source logo, kept for future edits (inlined as base64 in index.html)
README.md
.gitignore
```

## External requests

The page only reaches out to:

- Google Fonts — Space Grotesk (500/700) and Inter (400/500/600)
- `qrcodejs` via cdnjs, to render the vCard QR code on the back of the card

Everything else, including the logo, is inlined so the page renders correctly even when opened directly from disk with no sibling files present.

## Deploying to GitHub Pages

1. Push this repository to GitHub on the `main` branch.
2. In the repo, go to **Settings → Pages**, and set the source to deploy from `main` / root.
3. Add a `CNAME` file to the repo root containing:
   ```
   digi-tech.in
   ```
4. Point your domain's DNS at GitHub Pages (an `A`/`ALIAS` record to GitHub's Pages IPs, or a `CNAME` record if using a subdomain), per [GitHub's custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).
