# Artist Webpage

Static, responsive artist website built with plain HTML, Tailwind (CDN), and vanilla JS. Includes Spotify embeds, social links, an About section, and a Booking form that submits via Web3Forms (no local mail client required). Auto i18n switches between English and German based on the browser language.

## Features
- Modern hero with background image and subtle reveal animations
- Music section with Spotify artist embed and CTA
- Social links grid (Spotify, Apple Music, Instagram, YouTube Music, TikTok)
- About section with copy and highlights
- Booking form that sends via Web3Forms
- EN/DE i18n applied to labels, placeholders, messages

## Project structure
- `index.html` – main page
- `impressum.html` – legal page
- `js/main.js` – animations, smooth scroll, i18n, booking submission (Web3Forms)
- `artist_pictures/` – images

## Local preview
Open `index.html` directly in your browser, or run a tiny local server (optional):

PowerShell (if you have Python):
```powershell
cd "c:\Users\tonis\OneDrive\Dokumente\artist webpage project"
py -m http.server 8080
```
Then open http://localhost:8080 in your browser.

## Web3Forms (booking)
Submission lives entirely client-side. In `js/main.js`:
- Update `WEB3FORMS_KEY` with your key (https://web3forms.com/)
- Adjust `replyto`/`from_email`/`subject` if you want different behavior

If you rotate the key, just update it in `main.js` and redeploy.

## i18n
The site auto-switches to German if `navigator.language` starts with `de`, otherwise uses English. IDs are mapped to strings in `js/main.js` within the `i18n` object.

## Tailwind notes
- Uses Tailwind CDN; no build step.
- You can use arbitrary values like `mt-[21px]` or `translate-y-[12px]` where needed.

## License
No license specified. Add one if you plan to open source.

A minimal, fast, mobile‑first artist landing page for Finn. Built with plain HTML, Tailwind via CDN, tiny vanilla JS, and Spotify embeds.

## Tech choices
- Plain HTML + Tailwind CDN: zero build, perfect for a single‑page site.
- Vanilla JS: small enhancements (scroll reveal, parallax, mailto form).
- Spotify embeds: official, lightweight integration.

## Customize
- Replace hero image src in `index.html` with Finn’s Spotify profile image URL or a local `assets/finn.jpg`.
- Update highlight and brand colors in `:root` inside `index.html` if needed.
- Change social links to the official ones (already added from your brief).
- Replace `booking@example.com` in `js/main.js` with the real booking email.
- Optional: Add more featured cards in the Music section.

## Optional form backends
Easiest path without servers:
- Formspree: create a form endpoint, replace JS submit handler with a fetch to the endpoint.
- Netlify Forms: add `netlify` attributes on `<form>` and deploy on Netlify.

## Run locally
Just open `index.html` in a browser.

On Windows, you can also serve with a simple server for clean URLs:

```powershell
# Python 3
python -m http.server 8000

# Or with Node (if installed)
npx http-server . -p 8000
```

Then open http://localhost:8000/index.html

## License
Personal use for Finn’s promo site.
