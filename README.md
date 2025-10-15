# Vibe_Bingo Bingo

A real-time Bingo game (Players + Admin) designed for GitHub Pages. Uses **Supabase** (Postgres + Realtime). No Google Apps Script.

## Quick Start
1. **Create Supabase project** → copy `schema.sql` contents into SQL Editor and run.
2. In **both** `index.html` and `admin.html`, replace:
   - `SUPABASE_URL = "https://YOUR-PROJECT.supabase.co"`
   - `SUPABASE_ANON_KEY = "YOUR-ANON-KEY"`
3. Commit these files to a repo and enable **GitHub Pages** (branch: `main`, folder: `/`).
4. Open:
   - Players: `https://<username>.github.io/<repo>/index.html`
   - Admin:   `https://<username>.github.io/<repo>/admin.html`

## Admin Flow
- Enter **Game Code** (default suggestion: `Vibe_Bingo`) and a **PIN**, click *Create/Update Game*.
- Add themes, click *Allow for Game*, choose **Active Theme**.
- Click **Initiate** (players can pick & fix boards), then **Start Game** to begin.
- Use **Command Box** to broadcast words/numbers.

## Player Flow
- Enter name and optional avatar → pick a theme → shuffle board → **Fix**.
- When admin calls an item, click the exact matching cell to score (faster = more points).
- Leaderboard updates live; top 3 winners are recorded automatically.

## Notes
- RLS policies here are permissive for internal events. Lock down for public use.
- This stack scales to 100+ players on Supabase Realtime (light traffic).

Good luck and have fun! 🎉
