# Seartec Microsite

A single-page, self-contained microsite for Seartec (printing/trading services, South Africa), built as one standalone HTML file with fonts and images bundled inline — no external assets or build step required.

## 🚀 Publishing with GitHub Pages

GitHub Pages serves whatever is in your repo, but by default it looks for a file named **`index.html`** at the root of the branch it's pointed at. That's why this folder includes `index.html` — it's a straight copy of the original `Seartec_Microsite.html` file, just renamed.

### Steps

1. **Create a repository** on GitHub (or use an existing one).
2. **Upload `index.html`** (and this `README.md`) to the root of the repo — either via the web UI ("Add file" → "Upload files") or with git:
   ```bash
   git add index.html README.md
   git commit -m "Add Seartec microsite"
   git push
   ```
3. Go to your repo's **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to `Deploy from a branch`.
5. Choose the branch (usually `main`) and the folder (`/ (root)`), then click **Save**.
6. GitHub will publish the site at:
   ```
   https://<your-username>.github.io/<repo-name>/
   ```
   It usually takes a minute or two to go live after the first deploy.

### Keeping the original filename instead

If you'd rather keep the file named `Seartec_Microsite.html` instead of `index.html`, that's fine too — just note that visitors will need to browse to:
```
https://<your-username>.github.io/<repo-name>/Seartec_Microsite.html
```
since GitHub Pages won't automatically serve a non-`index.html` file at the site's root.

## 📁 Repository structure

```
.
├── index.html   # the microsite (self-contained: HTML, CSS, JS, fonts, and images all inline)
└── README.md    # this file
```

## Notes

- The file is fully self-contained (~12 MB) — there's nothing else to upload or configure.
- No build tools, dependencies, or custom domain setup are required for basic publishing.
- If you want a **custom domain**, add a `CNAME` file to the repo root with your domain name and configure the DNS records as described in GitHub's [custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).
