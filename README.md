# P4 Maths Practice Papers

Interactive 2025 End-of-Year Primary 4 maths practice papers with **one question per page**, per-question timing for reports, local auto-marking, parent PIN gate, Gemini method-mark feedback, and Maths Buddy chat.

While a paper is open, a background elapsed timer runs from the moment it starts. Time spent on each question is saved and included in the results summary, marked-paper PDF, and progress report.

## Gemini API key (required for AI marking / Maths Buddy)

The live site reads the key from `config.js`. That file is filled by GitHub Actions from the repository secret **`GEMINI_API_KEY`**.

1. Open [Settings → Secrets and variables → Actions](https://github.com/imBuenoing/p4-math/settings/secrets/actions)
2. Create or update secret **`GEMINI_API_KEY`** with your Google AI Studio / Gemini API key
3. Re-run **Actions → Deploy Processed Files to Main Branch Root → Run workflow** (or push any commit to `main`)

If the secret is missing or empty, the deploy workflow fails on purpose instead of publishing a blank key.

Local preview: put a real key in `config.js`, or leave the placeholder to use local marks only.

## Pages

Enable **GitHub Pages** from the `main` branch root (`/`) → `https://imbuenoing.github.io/p4-math/`

## Access PIN

The landing page and papers stay locked until the 4-digit site access code is entered. Only a hash is stored (`ACCESS_PIN_HASH`). Unlock lasts for the browser tab session; use **Lock** on the landing page to require the code again.

## Parent PIN

Used to mark a paper or clear saved data. Only a hash is stored (`PIN_HASH`). To change either PIN, open the browser console and run `pinHash('your-pin')`, then paste the result into `index.html`.
