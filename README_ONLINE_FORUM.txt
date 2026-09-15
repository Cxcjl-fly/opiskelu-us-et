OPISKELU — ONLINE FORUM

This version keeps the site on GitHub Pages but stores forum posts in Supabase.
GitHub Pages is static, so a hosted database/backend is required for shared online posts.

SETUP
1. Create a Supabase project.
2. Open SQL Editor and run supabase-schema.sql.
3. In Project Settings -> API, copy the Project URL and the publishable/anon key.
4. Edit supabase-config.js and replace the two placeholders.
5. Upload index.html and supabase-config.js to the root of the GitHub repository.
6. Keep supabase-schema.sql in the repository only if you want it as documentation; it is not loaded by the website.
7. Open the GitHub Pages site.

Realtime is enabled: when one visitor posts, other open forum pages receive the new post automatically.

IMPORTANT SECURITY
- Put only the public/publishable (anon) key in supabase-config.js. Never put a service_role/secret key in the website.
- This setup allows anonymous reading and posting. It is intentionally simple. For a public production forum, add authentication, anti-spam/rate limits, and moderator controls.
