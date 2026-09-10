# SNITCH

**Everything your browser gives away, read back to you.**

## What it is

One HTML file that runs the same reads a tracker's script runs the moment a page loads (IP, location, device, GPU, canvas / audio / font fingerprint, and a few dozen more), then shows you the answers instead of shipping them off. No prompt, no click needed. That is the point.

## What it reads

Network · Location · Device · Display · Browser · GPU · Fingerprint (composite + canvas + WebGL + audio + fonts + math) · Capabilities · Session

Plus a **"What actually helps"** section: seven collapsible cards with a bunch of plain-language notes on how to give out less fingerprints.

## Privacy

- Nothing is uploaded, logged, or stored **by SNITCH**. No backend, no database, no analytics.
- Exports (`.html` / `.json` / `.txt` / `.png`) are built in your browser and handed straight to you.
- One `localStorage` key powers the "return visit" row. Clear site data and it forgets you.
- Honest caveat: IP, geo and weather come from third-party APIs (ipify, ipapi.co, ipinfo.io, ipwho.is, open-meteo), so those lookups do leave your browser, carrying your IP the way any request does.

## Run it

Static file. Open `index.html` in a browser, or serve the folder:

```bash
npx http-server . -p 8080
# or: python3 -m http.server 8080
```

No build step, nothing to install. `snitch.html` is an identical copy of `index.html`.

## One file, no server

Markup, styles and logic are all in the one document. `Ctrl`+`U` shows the exact code your browser is running, which is the entire app.

---
_Part of [014.ca](https://014.ca)_
