# Protein Coffee Crush Tracker

A static Progressive Web App for tracking protein coffee drink ratings.

Live app:

https://coconut-bunch.github.io/protein-coffee-crush/

GitHub repo:

https://github.com/coconut-bunch/protein-coffee-crush

## Local Use

Open `index.html` in a browser, or serve the folder with any static web server.

## Deploy to GitHub Pages

1. Create a GitHub repo under the `coconut-bunch` account.
2. Push this folder to the repo's `main` branch.
3. In GitHub, open the repo's **Settings > Pages** screen.
4. Set **Build and deployment > Source** to **Deploy from a branch**.
5. Set **Branch** to `main` and **Folder** to `/ (root)`.
6. The site will deploy after GitHub Pages finishes publishing the branch.

The project site URL is:

```text
https://coconut-bunch.github.io/protein-coffee-crush/
```

## PWA Install

Open the GitHub Pages URL in Chrome on Android and use **Install app** or **Add to Home screen** from the browser menu.

## Data Storage

Drink data is saved in the browser's `localStorage` for this GitHub Pages origin. It is not sent to a server.

This storage is persistent across normal browser sessions and app restarts, but it can be removed if you clear site data, uninstall the browser/app, switch browsers, or use a different device. The app asks browsers that support the Storage API for persistent storage to reduce the chance of automatic eviction.

Use **Backup data** for the most reliable long-term copy. That exports a JSON file that can be imported later.

## Security Notes

- User-entered drink fields are rendered as DOM text or form values, not injected as HTML.
- Imported JSON backup data is parsed client-side and stored locally.
- CSV export escapes spreadsheet formula prefixes to reduce CSV formula-injection risk when opened in spreadsheet apps.
- The service worker only handles same-origin `GET` requests and caches the static app shell.
