# Seartec Microsite

A single-page concept microsite for **Seartec** — office technology (printers, MFDs, scanners) on month-to-month rental, serving businesses across South Africa.

Built and hosted as part of the **CAMicrosites** collection (Conversion Advantage GitHub Pages project).

## Live site

Once GitHub Pages is enabled for this repo (see below), this microsite is served at:

```
https://conversionadvantage00.github.io/CAMicrosites/seartec-staging/
```

## What's in this folder

```
seartec-staging/
├── index.html   ← the entire site (self-contained bundle)
└── README.md    ← this file
```

`index.html` is a **standalone bundle**: all markup, styles, scripts, fonts, images and video are packed into the one file and unpacked client-side on load (you'll briefly see an "Unpacking..." indicator). That means:

- No build step, no separate `/assets` folder, no external file references needed.
- It's a large file (~12 MB) since every asset is embedded as base64 — that's expected for this export format, not a mistake.
- To update the site, just replace `index.html` with a freshly exported bundle. There's nothing else to edit or wire up.

## Deploying on GitHub Pages

If Pages isn't already turned on for the `conversionadvantage00/CAMicrosites` repo:

1. Push this folder (`seartec-staging/`) to the `main` branch.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch."
4. Choose the `main` branch and `/ (root)` folder, then save.
5. GitHub will publish the whole repo; this microsite will be reachable at the `/seartec-staging/` path shown above because `index.html` sits inside that folder.

If Pages is already enabled for the repo, no extra configuration is needed — pushing this folder is enough, and the site will appear at the URL above within a minute or two.

## About this build

- Site content and copy: rental plans, cost-saving analysis pitch, testimonials, and the Cape Town/Paarl rep contacts, as supplied for the Seartec concept.
- Footer note carried over from the export: *"Concept preview. Layouts, creative and campaign concepts shown here remain the property of Conversion Advantage until a signed engagement is in place."*
- The quote-request form on the page is a front-end demo only (it doesn't send anywhere) — the footer notes that in the live microsite it would deliver to a sales inbox/CRM.
