# BEGIM — coming soon

The teaser site for **BEGIM**, a house of gold jewelry. Single-file, dependency-light,
deployed as a static site on GitHub Pages.

**Live:** https://begim.jewelry · **Opening:** September 2026

## What it is

A scroll-driven, cinematic landing page:

- A 3D gold **B·G** monogram jewel (Three.js) that leads the journey.
- Seven natural-colour animal worlds (full-bleed video), ordered as a colour journey
  — hummingbird → peacock → cobra → owl → puma → fox → flamingo.
- **Elemental transitions** between worlds — water (ripple + refraction), air (wind +
  pollen), light (bloom), fire (burn + embers). The corner jewel channels each force.
- A **Coming Soon** finale on a powder backdrop with a debossed wordmark and a waitlist form.
- EN / RU, smooth inertia scroll (Lenis), reduced-motion fallbacks.

## Structure

```
index.html        the page (HTML + CSS + JS inline)
scenes/           7 animal videos (.mp4) + poster frames (.jpg)
lenis.min.js      smooth-scroll (vendored, no CDN dependency)
favicon.svg       B·G mark
og.jpg            social share card
CNAME             custom domain (begim.jewelry)
```

Three.js is loaded from a CDN (esm.sh); everything else is local.

## Run locally

Any static server from the repo root, e.g.:

```
python3 -m http.server 8777
# open http://localhost:8777/
```

## Deploy

Pushed to GitHub → served by **GitHub Pages** (root of the default branch).
The waitlist form currently stores e-mails in `localStorage`; wire it to
Klaviyo / Shopify / Mailchimp before launch (see the `joinWaitlist` TODO in `index.html`).
