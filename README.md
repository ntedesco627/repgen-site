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
| Privacy Policy | Full policy (Apple required) |
| Terms | Short terms of use |
| Footer | Logo + nav links |

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

After deploying to HTTPS:

- **Support URL** → `https://yourdomain.com#support`
- **Privacy Policy URL** → `https://yourdomain.com#privacy`

## Deploy (no build step)

Upload this folder to any static host with HTTPS:

- **GitHub Pages** – Push repo, enable Pages.
- **Netlify / Vercel** – Drop the folder or connect the repo.
- **S3 + CloudFront / Firebase Hosting** – Upload static files.

## Apple checklist

- [ ] HTTPS live URL
- [ ] Support URL set in App Store Connect (points to `#support`)
- [ ] Privacy Policy URL set in App Store Connect (points to `#privacy`)
- [ ] Tested in Safari on iPhone — readable, no horizontal scroll, buttons tap correctly
- [ ] Page does NOT redirect to the App Store
- [ ] (Recommended) Link to `#privacy` and `#support` from app Settings
