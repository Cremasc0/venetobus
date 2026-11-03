# Busitalia Tickets — demo web app

A mobile-first mockup of the Busitalia Veneto ticket flow, built as a static site for GitHub Pages.

## Flow

1. **Tickets** — ticket catalogue with search, accordions and a cart. Tapping a price/cart pill adds the ticket; the bottom **Buy** bar turns Busitalia red and shows the running total.
2. **Ticket options** — review the selected tickets, set the direction for one-way tickets (passes have no direction), and choose *Activate now* or *Schedule activation*.
3. **Active ticket** — the existing QR/validation ticket screen, now filled from the purchase (ticket name, route or zone, price, validity timer, code).

Everything is client-side; no real ticket, payment or reservation is created.

## Project structure

```text
index.html      # The whole app (ticket select, options, active ticket)
busLogo.svg     # Busitalia vector logo
finalQr.svg     # QR code used on the active ticket
appimage.png    # PWA / home-screen icon
manifest.json   # PWA manifest (relative paths for GitHub Pages)
```

## Run locally

Open `index.html` directly, or serve the folder:

```bash
python -m http.server 8080
```

Then visit <http://localhost:8080>.

## Deploy on GitHub Pages

The repo is ready to publish from the `main` branch root:

1. Push to `main`.
2. In the repository: **Settings → Pages → Build and deployment**.
3. Source: **Deploy from a branch**, branch **main**, folder **/ (root)**.
4. The site will be available at `https://<user>.github.io/venetobus/`.

Fonts are loaded from Google Fonts (Jost) and Tailwind is loaded from its CDN, so the page needs an internet connection for the styled active-ticket screen.
