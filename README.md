# VK Digital Question Bank

A small installable PWA prototype built with vanilla HTML/CSS/JS. It has:
- VK splash/brand header and dashboard
- Six subjects (English, Hindi, Mathematics, Physics, Chemistry, Computer Science)
- Subject PDF library
- PDF upload/save to local IndexedDB
- In-app PDF open and download action
- Offline app-shell caching via service worker
- Dark mode

## Run locally
Use a local web server (service workers do not work reliably from `file://`):

```bash
python -m http.server 8080
```
Then open `http://localhost:8080`.

## Deploy to Vercel
1. Import this folder/project into a Git repository and connect it in Vercel, or deploy using Vercel CLI.
2. Framework preset: **Other**; build command empty; output directory `.`.
3. Deploy. HTTPS is required for PWA install and service workers.

## Notes
- PDFs uploaded from Settings are stored in IndexedDB on that browser/device, not in a shared cloud database. They do not automatically sync across users or devices.
- This prototype has no login or cloud admin system yet. For shared PDFs and admin publishing, connect a backend/storage service.
