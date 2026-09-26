JobFinder Combined V10 - Supabase Logout Fix

Fixes:
- Logout now uses Supabase local sign-out and redirects even if network sign-out encounters an error.
- Logout button shows "Logging out..." while processing.
- Home job loader now targets the actual jobs section, so database jobs can render correctly.

Backend:
Supabase Authentication + PostgreSQL + Row Level Security.

Live frontend:
https://logesh0798.github.io/Local-Jobs/

Important:
The Supabase publishable key may be present in browser code when RLS is configured. Never expose a Supabase secret/service_role key.
