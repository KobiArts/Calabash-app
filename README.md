# Calabash – GitHub Pages Offline App

This folder contains the Calabash app prepared as an installable Progressive Web App (PWA).

## Publish on GitHub Pages
1. Create a GitHub repository (for example `calabash-app`).
2. Upload **all contents of this folder** to the repository root. `index.html` must be at the root, not inside another folder.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Choose branch `main` and folder `/ (root)`, then Save.
6. Wait for GitHub Pages to publish, then open the provided HTTPS URL.

## Install and use offline
1. Open the published HTTPS link in Chrome or Edge while online.
2. Wait for the app to finish loading, then use the browser's **Install Calabash** option.
3. Open the installed app once while online. The service worker caches the app shell and subsequently loaded HTTPS assets.
4. Disconnect from the internet and test the app.

## Important notes
- The first visit must be online so the app can be downloaded and cached.
- Keep the app open online after publishing a new version once, so the updated files can be cached.
- Calabash's existing records remain in that browser's local storage. They are not automatically shared between computers or users.
- GitHub Pages does not provide a central registration database or user dashboard.
- External fonts may need an initial online load; the app should still display using fallback fonts when offline.
- Do not rename or move `service-worker.js`, `manifest.json`, or the `icons` folder unless you also update their paths in `index.html`.
