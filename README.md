# Speaker Realm — Speaker Stage Pipeline Funnel

Design handoff for Terrence / Lovable. Source: the approved four-page handoff assembled in ChatGPT on October 16, 2026.

## Pages

- `index.html` — marketing landing page
- `apply.html` — multi-step speaker application (DESIGN / DEMO, not wired to a database or delivery endpoint)
- `schedule.html` — consultation scheduling design, Calendly iframe and fallback booking link
- `confirmed.html` — confirmation design (DO NOT treat as evidence of an actual successful Calendly booking)

These are self-contained HTML pages with inline styling and scripts. They can be opened locally or hosted on a static site. Preview-only iframe navigation interception from the combined design handoff has been removed so regular page links work as standalone files.

## Production integration work remaining

1. Import/rebuild the approved layouts in Lovable, preserving visual treatment and copy; validate responsive behavior.
2. Connect the application form to a real backend/CRM and configure secure storage, consent, validation, anti-spam, notification and error/success states. Current form is a frontend demonstration; do not collect real applications through it.
3. Confirm the correct Calendly consultation event URL (`https://calendly.com/mannywolfe/30min` is the URL embedded in the source), test embedded booking across browsers/mobile, and preserve the fallback “Open booking link.”
4. Wire the booking confirmation view to a verified Calendly booking event/redirect/webhook before claiming an appointment is confirmed; avoid showing it just because someone navigates there.
5. Test every CTA, form field, internal link, accessibility behavior, analytics, and live deployment. Remove design-preview banners and copy before production as appropriate.
6. Audit for external image/font dependencies and replace unavailable assets with approved production assets.

## Security / credentials

Do not commit Calendly API secrets, CRM credentials, webhook signing keys, or environment values into this public repository. Use server-side secrets and provider-authorized integrations. No production authentication or credential handling has been implemented in these static pages.

## Preview

Open `index.html` and navigate using the links. For a local server, run `python3 -m http.server 8000` from the repository root and visit `http://localhost:8000`.

## Repo

https://github.com/etcwolfe67-web/Speaker-stage-pipeline-landing-page-funnel
