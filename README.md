# Poolie Start-Up Tool

Quoting, job tracking, and weekly-service follow-up for pool start-ups.
Stack: single-page `index.html` + Supabase (auth + database) + Vercel (hosting).

## Files
- `index.html` — the app (coming in phase 1)
- `config.js` — your Supabase URL + anon key (copy from `config.example.js`)
- `supabase/schema.sql` — run once in the Supabase SQL Editor
- `poolie-logo.png` — embedded in quote PDFs

## Setup
1. Create a GitHub repo and add these files.
2. Create a Supabase project, open SQL Editor, paste `supabase/schema.sql`, Run.
3. Supabase → Authentication → Sign In / Providers: turn OFF "Allow new users to sign up".
   Then Authentication → Users → Invite user for each sales team member.
4. Copy `config.example.js` to `config.js` and fill in URL + anon key (Project Settings → API).
5. Vercel → Add New Project → import the GitHub repo → Framework preset "Other" → Deploy.
6. Supabase → Authentication → URL Configuration: set Site URL to your Vercel URL
   (so invite / password-reset links land on the app).
