# Snapchat OAuth Callback Page

Static page that shows the `code`, `state`, `error` and `error_description` query parameters from an OAuth redirect so they can be copied manually. No scripts, styles or requests leave the page; everything is inline.

## Publish on GitHub Pages

1. Create a public GitHub repo (e.g. `snap-oauth-callback`).
2. Copy `index.html`, `callback.html` and `README.md` to the repo root.
3. Commit and push to `main`.
4. In the repo, go to Settings → Pages → Build and deployment → Source: "Deploy from a branch", Branch: `main`, Folder: `/ (root)`, then Save.

## Resulting URLs

- `https://{username}.github.io/{repo}/`
- `https://{username}.github.io/{repo}/callback.html`

Both serve the same page, so either can be used as the redirect URI.

## Important

The redirect URI must match exactly (scheme, host, path, trailing slash) in the Snap OAuth app settings, the authorize URL, and the token exchange POST. A mismatch causes the token request to fail.

The `code` is one-time use and expires quickly, so exchange it immediately.
