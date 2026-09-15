# Seartec Microsite

A single-page, self-contained microsite for Seartec (printing/trading services, South Africa), built as one standalone HTML file with fonts and images bundled inline — no external assets or build step required.

## 🚀 Publishing with GitHub Pages — clean "seartec-staging" URL

GitHub Pages auto-serves a file named **`index.html`** at whatever folder path it lives in. To get the site to resolve at:

```
https://conversionadvantage00.github.io/CAMicrosites/seartec-staging/
```

...the `index.html` in this download needs to sit **inside a folder named `seartec-staging`** in the repo — not at the repo root.

### Steps

1. **Create a repository** on GitHub (or use your existing `CAMicrosites` repo).
2. **Upload `index.html`** so it ends up at the path `seartec-staging/index.html` in the repo. The easiest way, since GitHub's drag-and-drop uploader won't create folders for you:
   ```bash
   mkdir seartec-staging
   mv index.html seartec-staging/
   git add seartec-staging/index.html README.md
   git commit -m "Add Seartec staging microsite"
   git push
   ```
   (Or, in the GitHub web UI: **Add file → Create new file**, then type `seartec-staging/index.html` as the filename — GitHub will create the folder automatically — and paste the file's contents in.)
3. Go to your repo's **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to `Deploy from a branch`.
5. Choose the branch (usually `main`) and the folder (`/ (root)`), then click **Save**.
6. GitHub will publish the site at:
   ```
   https://conversionadvantage00.github.io/CAMicrosites/seartec-staging/
   ```
   It usually takes a minute or two to go live after each deploy, and it redeploys automatically on every push.

### Important notes on the URL

- GitHub Pages will serve it at the folder path **with a trailing slash** (`.../seartec-staging/`). Visiting **without** the trailing slash (`.../seartec-staging`) also works — GitHub Pages redirects it to the slashed version automatically.
- A **bare filename with no extension** (e.g. a file literally named `seartec-staging`, no `.html`) is not a reliable way to get this URL — GitHub's static file server won't consistently serve it with the right content type, so browsers may try to download it instead of rendering it. The folder + `index.html` approach above is the standard, reliable way to get an extension-less path.
- If you *also* want the site reachable at the repo root (`.../CAMicrosites/`), you'd need a **second, separate** `index.html` at the repo root (outside the `seartec-staging` folder) — the root and the subfolder don't share one file.

## 📁 Repository structure

```
.
├── seartec-staging/
│   └── index.html   # the microsite (self-contained: HTML, CSS, JS, fonts, and images all inline)
└── README.md         # this file
```

## Notes

- The file is fully self-contained (~12 MB) — there's nothing else to upload or configure.
- No build tools, dependencies, or custom domain setup are required for basic publishing.
- If you want a **custom domain**, add a `CNAME` file to the repo root with your domain name and configure the DNS records as described in GitHub's [custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).
