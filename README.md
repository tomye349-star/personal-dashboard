# AthenaOS Lite — Training + HSC Study Dashboard

**Website:** https://tomye349-star.github.io/personal-dashboard/ (when GitHub Pages is enabled)

## Public, privacy-preserving setup

This repository holds the dashboard interface and **fictional example data only**. It does NOT contain real Garmin history, health or recovery metrics, personal study milestones, school details, cookies, API tokens, or credentials.

1. Open the hosted dashboard.
2. Download your separate `AthenaOS-Personal-Snapshot-YYYY-MM-DD.json` from the private ChatGPT conversation.
3. Click **Import private snapshot** in the header; choose that downloaded JSON.
4. Your personal overview, training graphs, study plan and insights appear and remain saved **in this browser's local storage**.
5. On a new device or browser, import the file there once. Local storage **does not sync between devices**.

No packages, npm, build step or server are needed. Your browser reads the JSON locally; the website makes no uploads or requests to Garmin or GitHub. Be aware that browser local storage is readable to anyone with access to the same browser profile and should not be used on a shared device.

## Updating your data

Ask ChatGPT: **Refresh AthenaOS Lite using my latest Daash Garmin data and update the study plan, then give me the personal snapshot JSON.** Download the new JSON and import it again. Your public GitHub repository requires no update for data refreshes.

## Hosting on GitHub Pages

A GitHub Actions workflow is included at `.github/workflows/pages.yml`. If no Pages deployment appears automatically:

1. Go to **Settings → Pages** in this repository.
2. Under **Build and deployment**, set **Source** to **GitHub Actions**.
3. Rerun the **Deploy AthenaOS Lite** workflow in the repository's **Actions** tab if needed.

Pages is PUBLIC, even if its source repo is private. That is why the actual personal data is **never** committed here. This is a read-only dashboard, not a live Garmin connection or secure multi-device personal database.

## Source files

- `index.html` — all dashboard layout, CSS and browser import logic.
- `demo-data.js` — fictional example statistics and generic study demo.
- `.github/workflows/pages.yml` — no-build static hosting on GitHub Pages.
- `.nojekyll` — static file deploy support.

No external JavaScript libraries, third-party analytics or remote fonts are required.