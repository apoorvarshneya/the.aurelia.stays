THE AURELIA STAYS — SIMPLE VERCEL REVIEW HELPER

Files:
- index.html: simple page with language dropdown, draft box, square dice and copy icons, and one-line Google Maps button
- api/generate-review.mjs: Vercel serverless function that securely calls the OpenAI API
- aurelia-logo.jpg and room-background.jpg: existing design assets

DEPLOY
1. Upload all files and folders to your GitHub repository (keep the api folder).
2. Import the repository into Vercel. No build command is needed for this plain HTML project.
3. In Vercel Project Settings -> Environment Variables, add OPENAI_API_KEY with your OpenAI API key.
4. Optionally add OPENAI_MODEL; default is gpt-4.1-mini.
5. Redeploy after adding the environment variable.

The dice requests a new draft from the AI. The page asks for 5–35 words and a suitable emoji. Because the guest has not supplied personal details, the AI is instructed not to invent specific experiences. Edit the draft so it honestly reflects your own stay. Google Maps opens separately; the guest must choose their own rating and submit the review.

Never put the OpenAI API key in index.html or commit it to GitHub. API usage is billed separately from a ChatGPT subscription.
