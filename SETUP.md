# SkillSwap – Setup
1. Install Bun (or Node 20+), then run `bun install`.
2. Copy `.env.example` to `.env` and fill in your backend URL and publishable key.
3. Apply the SQL files in `drizzle/migrations/` to your database (in order).
4. Run `bun run dev` and open http://localhost:8080.
5. Deploy: push to GitHub and import into your hosting provider; add the same env variables there.
