# TripSloth — Website

Marketing website for **TripSloth** (Xcode project: TourGuideAI).

## Structure

```
.
├── index.html            # Landing page (hero, features, how-it-works, screenshots, support)
├── privacy/
│   └── index.html        # Privacy policy (own URL: /privacy/)
├── assets/
│   ├── styles.css        # Shared styles (warm travel palette, no frameworks)
│   ├── favicon.ico       # Favicon generated from the app icon
│   ├── favicon-32.png / favicon-192.png / favicon-512.png
│   └── apple-touch-icon.png
└── images/
    ├── hero.png          # Hero image (from ~/Downloads/TourGuideAI/Hero)
    └── screenshot-1..7.jpg  # App screenshots (from ~/Downloads/TourGuideAI/IMG_7499..7505.PNG)
```

Images were downscaled/compressed for the web (originals in `~/Downloads/TourGuideAI/`).

## Hosting on GitHub Pages

1. Create a **public** repo, e.g. `TourGuideAI_website`, on GitHub.
2. Push this folder as the repo root:
   ```bash
   cd ~/Documents/Developer/iPhone/TourGuideAI_website
   git init && git add -A
   git commit -m "Add TripSloth marketing site"
   git branch -M main
   git remote add origin git@github.com:<you>/TourGuideAI_website.git
   git push -u origin main
   ```
3. In the repo: **Settings → Pages → Deploy from a branch → main / (root)**.
4. Site will be live at `https://<you>.github.io/TourGuideAI_website/` (or a custom domain via the Pages settings + a `CNAME` file).

## TODO before publishing

- **App Store link** — the app has no App Store Connect record yet. Replace the `APP_ID` placeholder in both App Store links in `index.html` (nav CTA + hero badge) with the real ID, e.g.:
  `https://apps.apple.com/us/app/trip-sloth/id<APP_ID>`
- Optionally set `og:image` to an absolute URL once hosted.

## Requirements checklist

- ✅ Hero image = `Hero.png` from `~/Downloads/TourGuideAI`
- ✅ Screenshots used as marketing material
- ✅ Standard "Download on the App Store" badge
- ✅ Privacy section with its own URL (`/privacy/`), honest about on-device + Gemini processing
- ✅ Support section with a button emailing `apps@maadotaa.com`, subject: *need help with TripSloth*
- ✅ Favicon generated from the app icon (`sloth.icon/Assets/TourGuideAIIcon-v2.png`)
