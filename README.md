# Budget

Compare what you actually spent against your monthly plan. Download a CSV from your bank, drop it in, and it sorts each transaction into a category.

- **App:** one static page (`index.html`) on GitHub Pages, with Google sign-in or an email code.
- **Data:** the private **Personal** Supabase project, in tables prefixed `budget_`. Row-level security means only your account can see your rows.
- **Banks:** SoFi and Capital One (Discover) export links are added on first sign-in. Edit them under **Plan**.
- **Keep-alive:** `.github/workflows/supabase-keepalive.yml` pings the Supabase projects daily so the free tier doesn't pause them.

## Use it
1. **Import**: tap a bank button, export a CSV, choose it, check the preview, then tap **Import**. Re-importing the same file is safe because duplicates are skipped.
2. **Transactions**: pick a category for anything uncategorized. Tap **+rule** to sort that merchant automatically from now on.
3. **Overview**: your spending vs. plan for the month.

Exporting: on SoFi, use the website (Banking → transactions → Export); the app can't export. On Capital One, open the card → View transactions → Download Transactions → CSV.

## Setup
Turn on Pages (Settings → Pages → `main`, `/ (root)`), and add `https://mattkrnr.github.io/budget/**` to Supabase → Authentication → URL Configuration → Redirect URLs in the Personal project.
