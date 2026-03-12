# RepGen Support & Privacy Website

Single-page site for **RepGen** (workout app) that satisfies Apple’s **Support URL** and **Privacy Policy URL** requirements for App Store submission.

## What’s included

- **Hero** – App name and tagline
- **About / Features** – Short description of RepGen
- **Support & Contact** – Prominent contact (email)
- **Privacy Policy** – App-specific policy with data practices
- **Terms of Use** – Short terms section

The page is static (HTML + CSS), mobile-first, and works on iPhone/iPad.

## URLs for App Store Connect

After you deploy with HTTPS:

- **Support URL:** `https://yourdomain.com` or `https://yourdomain.com#support`
- **Privacy Policy URL:** `https://yourdomain.com#privacy`

Use the same domain for both; anchors scroll to the right section.

## Customize before deploy

1. **Contact email** – Replace `support@repgen.app` in `index.html` with your real support email (search for `support@repgen.app` and replace all occurrences).
2. **Domain** – Deploy to your chosen domain and use that in App Store Connect.

## Deploy (static hosting)

Upload the contents of this folder to any static host with HTTPS:

- **GitHub Pages** – Push to a repo, enable Pages, select branch/folder.
- **Netlify / Vercel** – Drag this folder or connect the repo; no build step.
- **S3 + CloudFront, Firebase Hosting, etc.** – Serve `index.html` and `styles.css` as static files.

No build step required. Ensure the site is served over **HTTPS**.

## Apple checklist (before submit)

- [ ] Page loads over **HTTPS**
- [ ] **Support URL** in App Store Connect points here; page clearly identifies RepGen and has working contact
- [ ] **Privacy policy URL** in App Store Connect points here (e.g. `#privacy`)
- [ ] Test on **iPhone/iPad** in Safari: readable, no horizontal scroll, buttons/links work
- [ ] Page does **not** redirect to the App Store
- [ ] (Recommended) In the RepGen app Settings, add links to this page for “Privacy policy” and “Help & support” using `expo-web-browser` or `Linking`

## Optional: app icon on the page

To show the RepGen app icon, copy `assets/images/icon.png` (or a web-friendly version) from the `workouts-expo-app` project into this repo (e.g. `icon.png`) and in `index.html` replace the `.app-icon` span with an `<img src="icon.png" alt="RepGen" width="64" height="64">` (or similar).
