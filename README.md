# Eco Bros Plumbing: website

A one-page website for Eco Bros Plumbing (owner Daniel Savage), an eco-minded plumber serving Toronto and the GTA. It's plain HTML, CSS and JavaScript with no build step, so it runs on GitHub Pages as-is.

Live: https://jdix22.github.io/eco-bros/

## Highlights
- **Before/after slider** in the hero: it sweeps across by itself the first time it scrolls into view, then visitors can drag, swipe or use the arrow keys. The pair is an AI-generated illustration (labelled "Illustrative example" on the page). Swap in a real before/after from one of Daniel's jobs when he has one.
- **"What's going on?" finder:** visitors pick a symptom (dripping tap, running toilet, no hot water…) and get the likely service, a safe "while you wait" tip, and a button that pre-fills the request form.
- **Water savings estimator:** sliders for household size, drip rate, toilet and showerhead show litres saved per year, with an animated water level.
- **Job-site gallery** of Daniel's own Instagram photos, with a full-size viewer.
- All seven services from his flyer, plus the bathroom/basement/kitchen line from his Instagram flyer.
- Request form, FAQ, sticky Call/Request bar on phones, `Plumber` structured data (JSON-LD) and Open Graph tags.

## Email
Everything goes to **EcoBrosPlumbing@gmail.com**. The address is set once at the top of the script in `index.html`:

```js
var EMAIL = 'EcoBrosPlumbing@gmail.com';
var FORM_ENDPOINT = '';
```

Also update the `"email"` line in the JSON-LD block in `<head>` if it changes.

- **As shipped:** the request form opens the visitor's email app with a pre-written message (name, phone, service, urgency, details) addressed to that inbox. No account or server needed.
- **Straight to his inbox (recommended once he's on board):** make a free form at Formspree (or similar) pointed at EcoBrosPlumbing@gmail.com and paste its URL into `FORM_ENDPOINT`, e.g. `'https://formspree.io/f/abcdwxyz'`. Submissions then arrive in Gmail without the visitor's email app. If the service is ever down, the form falls back to the email-app method.

## Files
- `index.html`: the whole site
- `assets/img/hero-before*.jpg`, `hero-after*.jpg`: the illustrative slider pair (full size and phone size)
- `assets/img/job-*.jpg`: Daniel's job photos from Instagram (@ecobros_plumbing_and_drains)

## Editing
- **Phone:** search `index.html` for `6475261671` and `647 526 1671`.
- **Colours:** CSS variables at the top of `<style>` (`--ink` navy, `--leaf` green, `--water` blue, matched to his flyer).
- **Finder answers:** the `problems` array in the script.
- **Estimator assumptions:** `compute()` in the script; the fine print under the estimator lists them.
