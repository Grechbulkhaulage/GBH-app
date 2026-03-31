# Grech Bulk Haulage Production App

This package is a **production-ready codebase scaffold** for a real GBH operations app.

## What it includes

- Next.js mobile-first web app
- GBH logo on every page
- Sunday to Saturday roster page
- Daily docket form
- Driver clock in / clock out page
- Group chat page
- Photo upload page
- Admin management page
- Supabase SQL schema for live data
- Vercel-ready deployment config

## Important

This package gives you the **real app codebase and database schema**, but I **cannot directly connect your live domain, hosting, DNS, or database from inside this chat** because I do not have access to your Vercel, GoDaddy, Apple, Google Play, or Supabase accounts.

## Recommended live setup

- **Frontend hosting:** Vercel
- **Database / Auth / Storage / Realtime:** Supabase
- **Domain:** `app.grechbulkhaulage.com.au`
- **Support email:** `admin@grechbulkhaulage.com.au`

## Deploy steps

### 1) Create a Supabase project
Create a new Supabase project, then run:

- `supabase/schema.sql`

This creates tables for:
- drivers
- trucks
- customers
- roster shifts
- dockets
- time entries
- chat messages
- photo uploads

### 2) Add environment variables
Copy `.env.example` to `.env.local` and fill in:

- `NEXT_PUBLIC_SUPABASE_URL`
- `NEXT_PUBLIC_SUPABASE_ANON_KEY`
- `SUPABASE_SERVICE_ROLE_KEY`
- `NEXT_PUBLIC_SITE_URL=https://app.grechbulkhaulage.com.au`

### 3) Install and run locally
```bash
npm install
npm run dev
```

### 4) Deploy to Vercel
- Create a new Vercel project
- Import this folder
- Add the same environment variables in Vercel
- Deploy

### 5) Connect your real domain
In Vercel:
- add `app.grechbulkhaulage.com.au` as a custom domain

In GoDaddy DNS:
- point the subdomain to Vercel using the DNS records Vercel gives you

## What still needs account access

To make it truly live and synced, someone with your account access needs to do these last connection steps:

- create the Supabase project
- add environment variables
- deploy to Vercel
- update GoDaddy DNS
- optionally add Apple/Android install prompts
- optionally publish wrapped native versions later

## Best next move

Give this package to your web developer, or use it in Vercel + Supabase yourself.

If you want me to take it further after that, the next build phase should add:

- real authentication screens
- row-level security in Supabase
- realtime chat
- photo storage bucket rules
- PDF docket generation
- dashboard reporting
- push notifications
- payroll/export integration

## Default seeded data

Drivers:
- Timothy Grech
- Barry Kibblewhite
- Thomas Harvey
- Lyam Drummond
- Orkhan Combe
- John Gurdler

Trucks:
- TGRECH
- TIMMYG
- XP17NK

## Generated
Generated on 2026-03-31.
