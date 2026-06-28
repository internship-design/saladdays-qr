# Salad Days — Dynamic QR Code System

Self-hosted dynamic QR code manager. Create QR codes that redirect to any URL, and change the destination anytime without reprinting.

## How it works

1. Create a QR code at `/admin` — it generates a stable URL like `qr.saladdays.co/menu`
2. The QR image always encodes that stable URL
3. When scanned, the system looks up the current destination in the database and redirects
4. Change the destination anytime via the admin panel — the QR image never changes

## Setup

1. Create a Supabase project and run the SQL in the setup
2. Deploy to Vercel
3. Add environment variables (see `.env.local.example`)
4. Point `qr.saladdays.co` CNAME to Vercel

## Environment Variables

- `NEXT_PUBLIC_SUPABASE_URL` — Your Supabase project URL
- `NEXT_PUBLIC_SUPABASE_ANON_KEY` — Your Supabase anon key
- `ADMIN_PASSWORD` — Password to access the admin dashboard
