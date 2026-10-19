# P4 Maths Practice Papers

Interactive 2025 End-of-Year Primary 4 maths practice papers with **one question screen at a time** (multi-part questions stay together), per-screen timing for reports, local auto-marking, parent PIN gate, Gemini method-mark feedback, and Maths Buddy chat.

## Gemini API key

The repo secret **`GEMINI_API_KEY`** is injected at **deploy time** into the live Pages site. It is **not** committed to git (GitHub push protection blocks that).

1. Add/update [Settings → Secrets → Actions → `GEMINI_API_KEY`](https://github.com/imBuenoing/p4-math/settings/secrets/actions)
2. Switch Pages to Actions deploy (one-time): [Settings → Pages](https://github.com/imBuenoing/p4-math/settings/pages) → **Build and deployment** → Source = **GitHub Actions**
3. Re-run **Actions → Deploy site with Gemini key → Run workflow** (or push to `main`)

Check: open `https://imbuenoing.github.io/p4-math/config.js` — it should show a real key string, not `__GEMINI_API_KEY_PLACEHOLDER__`.

## Access PIN

Landing and papers stay locked until the 4-digit site access code is entered (`ACCESS_PIN_HASH`). Use **Lock** on the landing page to lock again.

## Parent PIN

Used to mark a paper or clear saved data (`PIN_HASH`).

## iOS keyboard math suggestions

Answer fields use `inputmode="text"` plus autocomplete/autocorrect off to reduce iOS Keyboard Math Results. Device setting (optional): **Settings → General → Keyboard → Math Results → Off**.
