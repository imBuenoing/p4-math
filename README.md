# P4 Maths Practice Papers

Interactive 2025 End-of-Year Primary 4 maths practice papers with local auto-marking, parent PIN gate, Gemini method-mark feedback, and Maths Buddy chat.

## Setup

1. Repository secret `GEMINI_API_KEY` must be set (already configured for this repo).
2. On each push to `main`, `.github/workflows/deploy.yml` injects the key into `config.js`.
3. Enable **GitHub Pages** from the `main` branch root (`/`) so the site is served at `https://imbuenoing.github.io/p4-math/`.

## Local preview

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

Optional: put a real key in `config.js` locally to try Gemini marking/chat. Leave the placeholder to use local marks only.

## Access PIN

The landing page and papers stay locked until the 4-digit site access code is entered. Only a hash is stored (`ACCESS_PIN_HASH`). Unlock lasts for the browser tab session; use **Lock** on the landing page to require the code again.

## Parent PIN

Used to mark a paper or clear saved data. Only a hash is stored (`PIN_HASH`). To change either PIN, open the browser console and run `pinHash('your-pin')`, then paste the result into `index.html`.
