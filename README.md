# The Aurelia Stays — QR Review Helper

Static mobile page: pick a language, roll a draft review, copy it, and open The Aurelia Stays on Google Maps.

## Structure
`index.html` · `css/style.css` · `js/` (`languages.js`, `reviews.js`, `clipboard.js`, `app.js`) · `assets/` (logo, room background, favicon)

## Deploy
1. Upload the whole folder (not just `index.html`) to https://app.netlify.com/drop, or push to GitHub Pages.
2. Open the HTTPS URL on your phone and test.
3. Make a QR code pointing to that URL, then scan-test the printed code.

Clipboard copy works most reliably over HTTPS.

## Limits
Google doesn't let a separate page pick a star rating, fill, or submit the review form. Guests paste the text, choose their own rating, and submit. If the review box doesn't open, tap Reviews → Write a review. Drafts are generic examples; guests should post only what reflects their own stay.

## Edit
- Reviews: `js/reviews.js` has, per language, 10 openers, 10 middle sentences and 10 closers. Each review is a random mix (openers/closers optional) plus an emoji: 6,050 combinations, 5–25 words. Dice never shows the same review twice in a session.
- Add a language: `js/languages.js` + a matching key in `reviews.js`
- Maps link: `mapsUrl` in `js/app.js`
