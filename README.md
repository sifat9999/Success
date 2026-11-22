# NEXORA STUDIO — Complete website project
A responsive Next.js 15 / React 19 website with cinematic dark styling, animated CSS/Framer Motion chrome sculpture, mobile navigation, service pages, concept portfolio, pricing, contact form, and client/admin preview routes.

## Run locally
Requires Node.js 20.9+.
```bash
npm install
cp .env.example .env.local
npm run dev
```
Open http://localhost:3000. The public pages render without Supabase. The contact endpoint validates the form but only stores enquiries after Supabase is connected. Client/admin pages are clearly labelled previews, not production account systems.

## GitHub + Vercel
1. Extract this ZIP.
2. Create a GitHub repository named `nexora-studio`.
3. Upload the extracted files and folders to the repository root (not the ZIP itself).
4. Import the repo into Vercel and deploy as a Next.js project.
5. Add the Supabase environment variables in Vercel settings if you want enquiry storage.

## Supabase lead storage
1. Create a Supabase project and run `supabase/schema.sql` in SQL Editor.
2. Set `NEXT_PUBLIC_SUPABASE_URL` and `SUPABASE_SERVICE_ROLE_KEY` in `.env.local` and Vercel.
3. Redeploy. Keep the service role key server-only. Never commit `.env.local` or secrets to GitHub.

## Before production
Replace the sample email, add rate limiting and bot protection, test the form, configure your domain, and implement real auth, project management, uploads, invoices and payment webhooks before advertising the client/admin portals. Portfolio pieces are labelled as concept work; replace them with real work or retain the disclaimer. Run `npm run build` before launch.

## Routes
`/` home · `/about` studio · `/services` capabilities · `/work` concept portfolio · `/pricing` pricing · `/contact` enquiry · `/login` client access · `/client` portal preview · `/admin` admin preview.
