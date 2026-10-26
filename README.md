# TNAC Beta Signup

The landing page for TNAC's beta tester signup, live at https://tnacapp.netlify.app.

## What's here

| File | What it is |
| --- | --- |
| `index.html` | The whole page: layout, styles and the signup form code |
| `images/` | The logo and the app screenshots |
| `netlify.toml` | Tells Netlify to serve this folder as-is (no build step) |

## How signups work

Both forms on the page save the visitor's first name, email, where they came from and (optionally) where they heard about TNAC to the `trial_signups` table in the **Fit App** Supabase project.

- Visitors can only add a signup. They can't read, change or delete the list.
- Duplicate and malformed emails are rejected by the database.
- The key in `index.html` is Supabase's *publishable* key, which is meant to be public. Never put the secret/service-role key in this repo.

To see signups: Supabase → Table Editor → `trial_signups`. Export to CSV from there.

## Tracking where people come from

Add `?src=` to each link you share. It's saved in the `source` column.

- Instagram bio: `https://tnacapp.netlify.app/?src=instagram`
- TikTok bio (once you have 1,000 followers): `https://tnacapp.netlify.app/?src=tiktok`

## Making changes

Edit `index.html` (or swap a file in `images/`), commit, and push to `main`. Netlify redeploys automatically in under a minute.
