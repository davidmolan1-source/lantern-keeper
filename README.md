# The Lantern Keeper

A small phone-first web game for Arianna. Two islands, a starlit bridge between, and a small lantern that brightens with truth, kindness, and courage.

## What's in this folder

- `index.html` — the whole game
- `vendor/jszip.min.js` — for the admin backup export
- `keepsakes/videos/Ln/` — drop family video files (`.mp4`) into the matching lesson folder for them to play in the Keepsake Box
- `server.js` — tiny static file server for local dev (`node server.js`)

## Local development

```sh
node server.js
# open http://localhost:8765
```

## Hosting

Any static host works. Tested with GitHub Pages and Netlify.

If you fork or deploy a copy, **add the deployed URL to your Google OAuth client** (Google Cloud Console → Credentials → your client → Authorized JavaScript origins) so the Drive sync admin feature works from the hosted version.

## Privacy

All recordings (Arianna's reflections) are stored locally on her device in IndexedDB. Family videos under `keepsakes/videos/` are excluded from version control by default (see `.gitignore`) so they never get pushed to a public host by accident. The admin backup exports a ZIP that stays local unless the user explicitly uploads it (Drive sync, share sheet, manual download).

No analytics. No notifications. No demand. The game waits for her.
