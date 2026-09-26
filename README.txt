JobFinder Combined V11 - Robust Logout Fix

Logout now uses a real navigation fallback to index.html?logout=1, signs out of the local Supabase session when possible, and removes Supabase browser-session keys as a fallback. The login page recognizes the logout flag so it will not immediately redirect back to Home.

Upload all files to the repository root and hard-refresh with Ctrl+F5.
