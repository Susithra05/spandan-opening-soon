# Spandan 2026 — Coming Soon (holding page)

Minimal static site shown temporarily on jipmerspandan.site while the
main Spandan 2026 app is finished. Completely separate Vercel project
from the main app — no shared code, no risk of touching the real build.

## Deploy (dashboard, no CLI needed)
1. Push this folder to its own GitHub repo (e.g. `spandan-coming-soon`).
2. On vercel.com → "Add New… → Project" → import that repo.
   Framework preset: "Other" (it's plain static HTML, no build step needed).
3. Deploy. You'll get a URL like `spandan-coming-soon.vercel.app`.
4. Go to that project's Settings → Domains → add `jipmerspandan.site`
   (and `www.jipmerspandan.site` if you use it).
   Vercel will tell you this domain is currently assigned to your other
   project — click through to reassign it here. DNS itself doesn't
   need to change since it's already pointed at Vercel.

## Switch back to the main site later
1. Go to your MAIN project's Settings → Domains → add `jipmerspandan.site` again.
   This reassigns it back from the coming-soon project.
2. Optionally delete the coming-soon project, or just leave it idle —
   it costs nothing sitting unused on the free tier.

## Deploy (CLI alternative)
```bash
npm i -g vercel
cd spandan-coming-soon
vercel          # first deploy, follow prompts, choose a NEW project
vercel --prod   # promote to production
vercel domains add jipmerspandan.site
```

## Before going live
- Replace the `BROCHURE_URL` placeholder in index.html with the real brochure link.
- Double check the Instagram handle in index.html matches your live account.
