# Certificate tools

## Setup (once)

```bash
pip install -r requirements.txt
```

## Add a certificate from a PDF

```bash
python add_cert.py --add "C:\path\to\My Certificate.pdf" --drive "https://drive.google.com/file/d/FILE_ID/view"
```

- Renders page 1 of the PDF to a high-quality JPEG in `../certificates/`
- Updates `certificates/manifest.json` + `manifest.js`
- The website reads the manifest and shows the new card automatically --
  the deck size and the "1 / N" counter update on their own

Options: `--name` (output filename), `--page` (render a different page),
`--width` (default 1600px), `--quality` (default 85), `--title`, `--drive`.

## Naming rule

**The filename IS the caption.** `Anthropic - Claude 101.jpg` shows on the
site as "Anthropic - Claude 101". Name your files exactly how you want them
displayed (spaces and capitals are fine). `--title` overrides it if ever needed.

## Dropped an image in manually? (jpg/jpeg/png/webp)

```bash
python add_cert.py --rescan
```

Then edit the new entry's `title` / `href` in `certificates/manifest.json`
if you want a nicer caption or a proof link, and run `--rescan` again to
regenerate `manifest.js`.

## Remove a certificate

Delete the image from `certificates/`, then run `--rescan`.
