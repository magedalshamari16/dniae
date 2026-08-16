# AGENTS.md

## Project
Single static landing page for "دبي الوطنية للتأمين" (Dubai National Insurance). Its only purpose is to drive visitors to a WhatsApp chat with the business at +971588439237.

## Architecture
- Plain static site — no framework, no build step. `netlify.toml` publishes the repo root as-is.
- `index.html` — all markup and copy (Arabic, RTL).
- `styles.css` — all styling.
- No backend, no database, no functions. Do not add one unless a new feature genuinely requires persistence.

## Conventions
- Keep the page RTL (`dir="rtl"`) and in Arabic; this is a UAE-market landing page.
- The WhatsApp CTA links to `https://wa.me/971588439237` — keep the number in sync if it ever changes.
- Logo in `index.html` is an inline SVG placeholder (shield icon) because no brand logo file was provided. Replace it with the real logo asset when one becomes available, keeping the same size/placement.

## Domain
The custom domain `dnii.ae` should be set as the site's primary domain in Netlify's site settings (Domain management). This could not be done from within the repo/agent — it requires DNS verification via the Netlify dashboard or DNS provider.
