JobFinder Combined V9 - Supabase Backend

Live frontend:
https://logesh0798.github.io/Local-Jobs/

Backend:
Supabase Authentication + PostgreSQL + Row Level Security.

V9 changes:
- Real Supabase email/password authentication.
- Registration creates a real Supabase Auth user and profile.
- No localStorage password storage.
- Home loads the signed-in user's real profile.
- Home loads active jobs from the jobs table.
- Saved jobs use the saved_jobs table.
- My Applications reads the applications table.
- Super Admin access is controlled by profiles.role = 'admin'.
- Admin Users reads profiles.
- Admin Jobs reads/creates/deactivates jobs.
- Admin Applications reads applications.

Important:
- The browser uses the Supabase publishable key. This key is intended for client applications when RLS is correctly configured.
- Never expose a Supabase secret/service_role key.
- Do not store passwords in localStorage.
- Email confirmation should be enabled before public launch.
- Admin user creation for other people should eventually use a secure server/Edge Function; the browser must not receive a secret/service_role key.

Required Supabase setup:
- profiles, jobs, applications, saved_jobs tables created.
- RLS policies created.
- Email provider enabled.
- Your Super Admin user's profiles.role set to 'admin'.
