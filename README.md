# Rivanshh Ecosystem — PWA starter

A responsive, installable, local-first web app foundation for the Rivanshh Ecosystem.

## Included modules
- **Home** — dashboard and module navigation
- **Music** — play audio files selected from the device, play/pause, seek, skip and session favourites
- **Tubes** — save and open video URLs
- **Social** — local posts, likes and comments
- **Connect** — local notes/chat UI (not live multi-user messaging)
- **Study with Abhivansh** — tasks, completion checklist and focus timer
- **Rivanshh AI** — prompt workspace placeholder (no model connected)
- **Rivanshh Pay** — safe UI placeholder (no transactions or banking data)
- **Rivanshh Link** — add/open/delete links and copy a link list
- **Profile** — edit name/handle/bio and upload cover/avatar images
- **Settings** — export/clear local data and compact UI preference
- PWA manifest and service worker

## Run locally
You can open `index.html` for a basic preview. For PWA/service worker behaviour, run through an HTTP server, e.g.:
```bash
python -m http.server 8000
```
Then open `http://localhost:8000`.

## Deploy to GitHub Pages
Upload the contents of this folder to the repository root (or the configured Pages folder) and enable GitHub Pages. Since the app is static, no build step is required.

## Important boundaries
This is a **functional front-end foundation**, not a fully connected production platform. Data is saved in localStorage on the current browser. Selected audio files play locally and are not uploaded. Live authentication, cross-device sync, public social feed, real-time messaging, AI responses, cloud media hosting, notifications, and payment processing require secure backend services and configuration. Do not put private API keys in `app.js`.

## Profile cover
The profile screen supports uploading a cover image. The exact previously discussed cover image was not available in the current build inputs, so upload that image in **My Profile → Upload cover image** or add it as an asset and wire its path.

## Suggested production backend
A Supabase project can provide Auth, Postgres, Storage and Realtime. Add row-level security policies before exposing user data. For AI, use a server-side Edge Function to keep provider keys secret. For payments, use a compliant payment provider and verify transactions server-side.
