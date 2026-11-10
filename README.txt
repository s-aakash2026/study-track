STUDYOS 10 — PROGRESSIVE WEB APP PACKAGE

WHAT'S INCLUDED
- index.html: your existing StudyOS tracker, with syllabus/chapter data and tracker logic preserved
- manifest.webmanifest: installable app metadata
- sw.js: service worker for app-shell offline caching
- icons/: install icons for supported browsers/devices

IMPORTANT: A service worker and PWA installation require HTTPS (or localhost for testing).
Opening index.html directly as a file will still let you use the tracker, but it will NOT enable PWA installation/offline app-shell caching.

QUICK TEST ON A MAC
1. Open Terminal and cd into the unzipped StudyOS10-PWA folder.
2. Run: python3 -m http.server 8000
3. Open http://localhost:8000 in Chrome or Safari.
   (For install testing, Chrome supports the install UI; Safari on macOS can add supported websites to the Dock.)

PUBLISH FOR INSTALL ON OTHER DEVICES
Upload the CONTENTS of this folder to any static host that serves HTTPS (for example GitHub Pages, Netlify, or Cloudflare Pages).
Then visit the HTTPS URL and use the browser's Install/Add to Home Screen option.

OFFLINE NOTES
The app shell is cached after the first successful visit. Google Fonts and third-party GSAP/Chart.js/Lucide CDN assets are not bundled, so those decorative/external enhancements may be unavailable offline. Core tracker behavior and browser-local progress remain available. Progress is stored in that browser's localStorage; it is not automatically synced between devices.

SYLLABUS SAFETY
This PWA conversion only adds app metadata, icons, install handling and service-worker caching. It does not intentionally change the syllabus entries, chapter names, topic descriptions, priority tags or tracking data logic.
