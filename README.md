# Meliora Support Website

This folder is the public website for the Meliora iOS app. It provides the homepage, the support page, the privacy policy, and a 404 page. It is a static site with no JavaScript, analytics, cookies, trackers, or external embeds.

## Purpose

- Privacy policy URL for App Store Connect
- Support URL for App Store Connect
- Optional marketing homepage

## File structure

```text
meliora-support/
├── index.html          Homepage
├── style.css           Shared styles
├── 404.html            Branded not-found page
├── README.md           This file
├── .nojekyll           Tells GitHub Pages to serve files as-is
├── assets/
│   └── meliora-icon.png
├── privacy/
│   └── index.html      Privacy policy
└── support/
    └── index.html      Support page
```

## Preview locally

From inside the `meliora-support` folder, run:

```bash
python3 -m http.server 8080 --bind 0.0.0.0
```

Then open `http://localhost:8080/` in a browser. The pages can be checked at `/privacy/` and `/support/`.

## Publish with GitHub Pages

1. Open the repository on GitHub.
2. Go to **Settings**, then **Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the **main** branch and the **/ (root)** folder, then save.
5. Wait for the deployment to finish, then open the site URL.

## Public URLs

- Homepage: https://weird-guitar.github.io/meliora-support/
- Privacy policy: https://weird-guitar.github.io/meliora-support/privacy/
- Support: https://weird-guitar.github.io/meliora-support/support/

Use the privacy and support URLs in App Store Connect.

## Replace the app icon

The file `assets/meliora-icon.png` is the app icon used on every page. Replace it with your final 1024 × 1024 PNG and keep the same file name. Commit the change and wait for GitHub Pages to redeploy.

The 404 page loads the icon and stylesheet from the full GitHub Pages URL, so the 404 page works from any missing path.

## Update the support email

The support address `meliora.app@proton.me` appears in the following files:

- `index.html`
- `privacy/index.html`
- `support/index.html`

Search for `meliora.app@proton.me` across the folder and replace every occurrence. Update both the visible text and the `mailto:` link.

## Warning

Do not add private app source code, signing certificates, provisioning profiles, App Store Connect credentials, API keys, or any other secrets to this repository. This site is public. Only publish website files and the public app icon.

## Version

Meliora 1.0.0
