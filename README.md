# Anmol Multani — Portfolio Site

A minimal, single-page portfolio site. Everything lives in one `index.html` file plus an `assets/` folder — no build step, no dependencies. Open `index.html` in a browser to preview it right now; the placeholder tiles show you exactly which file to drop in and where.

## 1. Add your photos & video in VS Code

Drop files into these folders using **these exact names** (or edit the paths in `index.html` if you'd rather rename them — each image/video tag has a matching `src` you can change):

```
assets/
├── profile/
│   ├── hero.jpg        ← optional lead image, top right of the hero
│   └── about.jpg        ← optional portrait next to the About text
├── rodd-royalty/         (2024 — business attire, Rodd Royalty)
│   ├── 01.jpg
│   ├── 02.jpg
│   ├── 03.jpg
│   ├── 04.jpg
│   └── campaign.mp4
├── island-beach/         (2025 — Island Beach Co., sweaters & tees)
│   ├── 01.jpg
│   ├── 02.jpg
│   ├── 03.jpg
│   ├── 04.jpg
│   └── 05.jpg
├── rodd-crowbush/        (2026 — Rodd Crowbush Resort, releasing June 2026)
│   └── campaign.mp4
└── coastal-culture/      (2026 — new partnership, video in production)
    └── preview.jpg       ← optional, otherwise the card just links out to Instagram
```

Until a file exists, that tile shows a dashed placeholder with the exact path so you always know what's missing — nothing ever looks broken, it just quietly waits for the file.

You don't need all 4 Rodd Royalty photos or all 5 Island Beach photos before publishing — add what you have now and drop the rest in later; the site updates the moment the file exists at that path.

## 2. Add your Instagram links

Open `index.html`, scroll to the bottom `<script>` block, and edit the `CONFIG` object:

```js
const CONFIG = {
  instagramProfile: "https://instagram.com/anmol.finance",
  campaignLinks: {
    roddRoyalty:    "",   // paste the Instagram post link for Rodd Royalty
    islandBeach:    "",   // paste the Instagram post link for Island Beach Co.
    coastalCulture: ""    // paste your Coastal Culture Instagram link (or leave blank to default to your profile)
  }
};
```

Rodd Crowbush has no link field — it's marked "Unreleased" until you're ready to add one (email me back or just ask if you want that added later).

## 3. Publish it with GitHub Pages

1. Create a new GitHub repository (e.g. `anmol-portfolio`).
2. Upload everything in this folder (`index.html`, `README.md`, and the `assets/` folder with your photos/video added).
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
5. GitHub gives you a live link, usually `https://<your-username>.github.io/<repo-name>/` within a minute or two.

That link is what you post in your Instagram bio (`anmol.finance`) and send over email.

## 4. Editing text

All copy — the bio, campaign descriptions, comp-card stats, email — lives directly in `index.html` as plain text, so you can find and edit anything with Ctrl/Cmd+F in VS Code without touching the CSS or layout.
