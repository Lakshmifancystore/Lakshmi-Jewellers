# Lakshmi Jewellers — Complete Full-Stack E-Commerce Platform (Phases 1–10)

## Architecture
- **Frontend:** Mobile-first responsive HTML + Tailwind CSS + Vanilla JavaScript (`public/index.html`)
- **Backend:** Node.js + Express (`server/index.js`) with `helmet`, `cors`, and tiered `express-rate-limit`
- **Database, Auth & Storage:** Supabase PostgreSQL + Supabase Auth (`supabase/schema.sql`)
- **Payments:** Razorpay server-side order creation & HMAC-SHA256 signature verification (`server/routes/checkout.js`)
- **WhatsApp Channel:** Configured for `+91 82475 07275` across product, cart, checkout, and bridal/wholesale inquiries

## Step-by-Step Deployment Guide
1. **Create Supabase Project (Free Tier):**
   - Go to https://supabase.com and create a project.
   - Open **SQL Editor** and run `supabase/schema.sql`.
   - Note: Supabase free tier includes 500 MB DB, 1 GB storage, and 50K monthly active users (projects pause after 7 days of inactivity unless upgraded or pinged).
2. **Configure Razorpay (Online Payments Only — No COD):**
   - Create an account at https://razorpay.com and complete KYC for live UPI, Card, and NetBanking payments (~2% per transaction, ₹0 monthly fee).
   - Start with Test Keys (`rzp_test_...`) before switching to Live Keys.
3. **Environment Variables:**
   - Copy `.env.example` to `.env` and fill in `SUPABASE_URL`, `SUPABASE_ANON_KEY`, `SUPABASE_SERVICE_ROLE_KEY`, `RAZORPAY_KEY_ID`, `RAZORPAY_KEY_SECRET`, and `FRONTEND_URL`.
   - Never commit `.env` or expose secret keys in frontend files.
4. **Promote Your Admin Account:**
   - Sign up on `/#/account`, then run in Supabase SQL Editor:
     ```sql
     update public.profiles set role = 'admin' where email = 'your-email@example.com';
     ```
5. **Run Locally or Deploy (Render / Railway / Vercel):**
   ```bash
   npm install
   npm start
   ```
   Open `http://localhost:4000`.
6. **SEO & Google Setup:**
   - Replace `https://lakshmifancystore.in` in `public/robots.txt`, `public/sitemap.xml`, and canonical meta tags.
   - Verify your domain in Google Search Console and submit `/sitemap.xml`.
