# The Aurelia Stays — Review Helper

One page: language dropdown, a review box (5–35 words, emoji added automatically), 🎲 new review, 📋 copy, and "Copy review & open Google Maps ↗".

## How reviews are made
- 🎲 / language change → asks the OpenAI API (through `netlify/functions/generate-review.mjs`, so the key stays secret).
- If the API isn't available (no key, GitHub Pages, offline), the page falls back to the built-in phrase bank in `js/reviews.js`, so the box always fills.
- The first review on page load comes from the built-in bank, so scans cost nothing.

## Deploy (Netlify)
1. Put this whole folder in a GitHub repo and import it into Netlify (build command blank, publish directory `.`).
2. Site settings → Environment variables: add `OPENAI_API_KEY` (optional `OPENAI_MODEL`, default `gpt-4.1-mini`). Redeploy.
3. Open the site on your phone, test, then make the QR code from the Netlify URL.

Never put the API key in any file. API billing is separate from a ChatGPT subscription.
GitHub Pages can't run the function; the page still works there using the built-in bank.

## Edit
Languages: `js/languages.js` (+ `L` in the function). Built-in phrases: `js/reviews.js`. Maps link: `mapsUrl` in `js/app.js`.
