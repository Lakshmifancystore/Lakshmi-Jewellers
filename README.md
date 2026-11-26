# Lakshmi Jewellers — Full-Stack E-Commerce Platform (Phase 5)

## Stack
- **Frontend:** Responsive HTML + Tailwind CSS + Vanilla JS (`public/index.html`)
- **Backend:** Node.js + Express (`server/index.js`) with `helmet`, `cors`, and rate limiting
- **Database & Auth:** Supabase PostgreSQL + Supabase Auth (`supabase/schema.sql`)

## Quick Setup
1. Create a free Supabase project at https://supabase.com.
2. Open **SQL Editor** in Supabase and run `supabase/schema.sql`.
3. Copy `.env.example` to `.env` and fill in `SUPABASE_URL`, `SUPABASE_ANON_KEY`, and `SUPABASE_SERVICE_ROLE_KEY`.
4. Install dependencies and start the server:
   ```bash
   npm install
   npm start
   ```
5. Open `http://localhost:4000` in your browser.
