# Vaasi Yogam — vasiyogam.com

A static website for the Tampa, Florida Vaasi Yogam sangam, rooted in the South
Indian Hindu Siddhar tradition. Lord Murugan — divine leader of the 18 Siddhars —
is honored in the hero section; the design uses a saffron-orange, deep-temple-blue,
and white palette with Tiruvannamalai-temple-inspired motifs (gopuram silhouettes,
temple-niche arch framing, kolam-inspired ornamental borders).

Pages: `index.html` (home), `siddhars.html` (the 18 Siddhars with Tamil names),
`practice.html` (the Vaasi Yogam sadhana), `gatherings.html` (Tampa schedule +
contact placeholders, marked with `EDIT HERE` comments). Plain HTML/CSS/JS with
zero build step — it opens directly from `file://` and deploys as-is.

## Deploy notes

1. **GitHub:** create a repo (e.g. `vasiyogam-website`), commit this directory's
   contents at the repo root, and push.
2. **Cloudflare Pages:** Dashboard → Workers & Pages → Create → Pages → connect
   the GitHub repo. Framework preset: **None**. Build command: *(leave empty)*.
   Build output directory: `/` (repo root). Deploy.
3. **Custom domain:** in the Pages project → Custom domains → add
   `vasiyogam.com` (and `www` if desired); Cloudflare provisions DNS + SSL
   automatically since the domain is on Cloudflare.
4. Before publishing, fill in the real contact details in `gatherings.html`
   (search for `EDIT HERE`) and confirm the gathering schedule.

Images in `assets/` were generated for this site (temple-mural style, devotional
South Indian art). The 18-Siddhar list follows the commonly cited traditional
list; see the note on `siddhars.html` — lists vary across Tamil sources.
