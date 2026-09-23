# AGENTS.md — vasiyogam.com

Working instructions for any agent editing this site. Read this file before making changes.

## Project
- Static website for the Tampa Vaasi Yogam chapter (Kriya Yoga / Vaasi Yogam sangam).
- Repo: `Dhineshin/vasiyogam-website`. Hosting: Cloudflare Pages. Production branch: `main`.
- **Every push to `main` auto-deploys to vasiyogam.com.** Keep `main` clean and deployable.
- Pages (as of 2026-09-23): `index.html`, `gatherings.html`, `practice.html`, `siddhars.html`.
  New pages may be added over time — the rules below apply to all of them.

## Design theme (do not drift)
- South Indian Hindu **Siddhar tradition**. Lord Murugan is presented as the **leader of the 18 Siddhars**.
- Palette: **orange, blue, and white**.
- Visual language inspired by **Tiruvannamalai Temple** — sacred, reverent, warm.
- Greeting: **"Vanakkam"** — never "Namaste".
- Language: English primary; Tamil accents welcome (e.g. வாசி யோகம் in headings).
- Devotional imagery must be approved by the site owner before publishing.
  AI-generated devotional images are placeholders until approved/replaced.

## Content rules
- **Never invent lineage, teachers, authority, or spiritual credentials.** Only state what the owner has confirmed.
- Gathering schedule and location are still being decided — do not publish placeholder specifics.
- Contact email: `contact@vasiyogam.com` (forwards to the owner).
- The site owner is the final authority on all spiritual wording and Siddhar descriptions.

## Analytics — mandatory on every page
- **Every HTML page, current and future, must include the GA4 tracking snippet in `<head>`.**
- The snippet is the same on all pages; only the Measurement ID changes per property.

```html
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA4_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA4_MEASUREMENT_ID');
</script>
```

- Active Measurement ID: `G-7W8B18792C` (GA4 property "vasiyogam.com", property ID 555498295, stream ID 15831121910).
- GA4 property is owned by the owner's Google account (dhineshin@gmail.com).
- Bot filtering is enabled in GA4; retention set to 14 months.

## Workflow
- Edit files, commit to `main`, Cloudflare Pages deploys automatically.
- Verify a deploy by loading https://vasiyogam.com (allow ~1 minute after push).

## Site maintenance checklist (every change)
- **New page?** Add the GA4 snippet to `<head>`, add canonical + OG/Twitter meta tags,
  add the page to `sitemap.xml`, and link it from the nav/footer where appropriate.
- **URLs are pretty:** link and canonicalize `/gatherings`, never `/gatherings.html`
  (Cloudflare 308-redirects `.html` → pretty). Same for `/blog/`, never `/blog/index.html`.
- **New blog post?** Copy `blog/_template.html` → `blog/<slug>.html`, fill in every
  PLACEHOLDER, then: add a card to `blog/index.html`, an `<item>` to `blog/feed.xml`,
  and a `<url>` entry to `sitemap.xml`.
- Blog lives at `/blog/` ("Reflections · சிந்தனைகள்"). Topics: Practice, Siddhar Wisdom,
  Meiporul, Dhyanam, Gatherings. RSS feed: `/blog/feed.xml`.
- Never publish placeholder spiritual content — posts and pages carry only
  owner-approved wording.
