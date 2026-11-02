# RepGen Fitness — Support Website

Single-page support & privacy site for the **RepGen** iOS app. Satisfies Apple's **Support URL** and **Privacy Policy URL** requirements for App Store submission.

## Structure

| Section | Purpose |
|---|---|
| Nav | Sticky header with logo + links |
| Hero | Wordmark logo, tagline, support CTA |
| Screenshots | Phone mockup placeholders (replace with real screenshots) |
| Features | 4 feature cards |
| Support | Contact email (support@repgen.fit) |
| `#privacy` / `#terms` | Short summaries on the homepage. Existing links keep working and point to the full pages. |
| Privacy Policy | Full draft at `/privacy/` (`privacy/index.html`) |
| Terms of Use | Full draft at `/terms/` (`terms/index.html`) |
| Consumer Health Data Privacy Policy | Separate draft at `/health-data/` (`health-data/index.html`), linked from the homepage footer |
| Footer | Logo + nav links, including the consumer health data policy |

The legal pages are drafts pending legal review. They are not legal advice. Facts that are not confirmed yet are marked `[TODO: …]` in the pages.

## Adding real screenshots

The three phone mockup frames in the **Screenshots** section are CSS placeholders. To replace them:

1. Export 3 iPhone screenshots from your app (recommended: 390×844 PNG).
2. Save them to `assets/screen-1.png`, `assets/screen-2.png`, `assets/screen-3.png`.
3. In `index.html`, replace each `.phone-screen` div's contents with an `<img>` tag:

```html
<div class="phone-screen">
  <img src="assets/screen-1.png" alt="Workouts screen">
</div>
```

## App Store Connect URLs

After deploying to HTTPS (GitHub Pages serves the folder `index.html` files at these paths):

- **Support URL** → `https://repgen.fit/#support`
- **Privacy Policy URL** → `https://repgen.fit/privacy/`
- **Terms of Use** (linked from the privacy policy and the app, if you show it) → `https://repgen.fit/terms/`
- **Consumer Health Data Privacy Policy** → `https://repgen.fit/health-data/`

`https://repgen.fit/#privacy` and `https://repgen.fit/#terms` still open the homepage summaries.

## Deploy (no build step)

Upload this folder to any static host with HTTPS:

- **GitHub Pages** – Push repo, enable Pages.
- **Netlify / Vercel** – Drop the folder or connect the repo.
- **S3 + CloudFront / Firebase Hosting** – Upload static files.

## Launch checklist

- [ ] HTTPS live URL
- [ ] Support URL set in App Store Connect (points to `#support`)
- [ ] Privacy Policy URL set in App Store Connect (points to `/privacy/`, not only `#privacy`)
- [ ] Tested in Safari on iPhone — readable, no horizontal scroll, buttons tap correctly
- [ ] Page does NOT redirect to the App Store
- [ ] (Recommended) Link to `/privacy/` and `#support` from the app
- [ ] Production Gemini API key is on a billing-enabled (paid tier) Google project before any real users, including beta testers.
- [ ] Remove draft banners and DRAFT comments before publish
- [ ] Report and block, the content filter, and the AI consent screen are shipped in the app
- [ ] App privacy link updated from `/#privacy` to `/privacy/`
