# Digital NGO AI Software — fresh starter

This is a clean Next.js + TypeScript starter intended to be uploaded to a new GitHub repository and deployed with Vercel.

## What's included
- Responsive landing page with NGO module overview
- Login setup information page
- Supabase client helper (inactive until environment variables are configured)
- Environment variable example file
- Basic project configuration

## Important status
This starter is **not yet a production NGO management system**. Member database, admin authentication, document generation, QR verification, payments, and AI are planned next steps and are not implemented in this first stage. Do not store real member, identity, or donation data until authentication, database policies, and backups are configured and tested.

## Run locally
Requires Node.js 20.9 or later.

```bash
npm install
cp .env.example .env.local
npm run dev
```

Open http://localhost:3000.

If you do not have Supabase values yet, leave the two environment variables blank; the landing page still works.

## Deploy to Vercel
1. Push this project to a new GitHub repository.
2. In Vercel, choose Add New → Project and import that repository.
3. Use the default Next.js settings.
4. Deploy. The landing page does not require Supabase environment variables.
5. Add Supabase variables later when connecting the database:
   - `NEXT_PUBLIC_SUPABASE_URL`
   - `NEXT_PUBLIC_SUPABASE_ANON_KEY`

Only use the publishable/anon key in the browser. Never put a Supabase service-role key or other secret in a `NEXT_PUBLIC_` variable or in GitHub.
