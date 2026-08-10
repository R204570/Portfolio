# Raj Patel — Portfolio

Personal portfolio of **Raj Patel** — AI Engineer & Full-Stack Vibe Code Developer.
Dark editorial single-page site focused on Agentic AI, AI Engineering (PyTorch / NLP / LLMs), Full-Stack development and Data Science.

## What's inside

- **`index.html`** — the entire website in one self-contained file.
  Fonts (Anton, Archivo, IBM Plex Mono), the avatar and live-app screenshots are
  embedded as data URIs, so there are no external requests and no build step.
- **`Raj-Patel-Resume.pdf`** — served by the "Resume" links in the nav and
  contact section. Replace this file to update the downloadable resume.
- **`Intel-Internship-Report.pdf`** — the GTU summer-internship (PMMS) report,
  linked from the PCB Inspection AI project card. Replace the file to swap in
  a different report; keep the same filename.
- **`certificates/`** — certificate images + `manifest.json`/`manifest.js`.
  The Vault deck builds itself from the manifest: card count and the
  "1 / N" counter update automatically. To add a certificate, use
  `tools/add_cert.py` (converts a PDF and updates the manifest), or drop
  an image in and run `python tools/add_cert.py --rescan`. See `tools/README.md`.
- **`tools/`** — `add_cert.py` PDF-to-JPEG converter + manifest generator.

## Deploy

Any static host works — the whole site is one file.

**Netlify (fastest):** drag the `raj-portfolio` folder onto https://app.netlify.com/drop

**Vercel:**
```bash
npm i -g vercel
vercel --prod
```

**GitHub Pages:** push this repo to GitHub → Settings → Pages → deploy from `main`.

## Editing

Everything is in `index.html`:

- **Colors / fonts** — CSS custom properties in the `:root` block (`--ink`, `--bone`, `--amber`, `--violet`).
- **Projects** — each `<article class="project">` block; badges are the `<span>`s inside `.p-tags`.
- **Certifications marquee** — the `.cert-chip` spans (the set is duplicated once for the seamless loop — edit both copies).
- **Milestones** — the `.mile` cards.
- **Contact** — search for `rajpatel9408019@gmail.com`.

## Sections

Hero → About + skill pillars → Certifications marquee → Projects (6) → Open-to-work CTA → Milestones → Contact footer.

## Let's Connect !
Portfolio Website: https://portfolio-raj-25.netlify.app/
Linkedin: https://www.linkedin.com/in/raj-patel5/
Github: https://github.com/R204570
