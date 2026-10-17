# Security policy

## Reporting
Use GitHub "Report a vulnerability" on this repository to open a private advisory.
Please do not open public issues for security problems. First answer within 5 working days.

## Scope
A static single-page site served from GitHub Pages. No backend, no accounts, no cookies,
no analytics.

## Threat model
- Asset: the visitor's browser session on the Pages origin.
- Entry points: the photo picker and the dossier text fields, all processed locally.
- Risks and mitigations:
  - Script injection through the text fields: values are HTML-escaped before they are
    written into the page.
  - Photo privacy: images are read with `FileReader` and drawn to a canvas; there is no
    `fetch`, XHR, WebSocket or beacon in the code, so nothing is uploaded.
  - Third parties: Google Fonts is the only external origin.
- Not covered: GitHub Pages does not allow custom response headers (CSP, frame-ancestors).
