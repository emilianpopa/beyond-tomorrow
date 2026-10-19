# Beyond Tomorrow

The one repo for everything built for Beyond Tomorrow (Julian Issa, Noa): The Forum site and the
seed raise workspace. Express on Railway, auto-deploys from `main`.

Layout

    public/index.html                 The Forum landing page, served at /
    public/workspace/index.html       Investor workspace (story, numbers, guide), /workspace
    public/workspace/financial-model.html   Rendered model, /workspace/financial-model
    public/workspace/model.xlsx       Live formula-driven model, the editable source
    public/workspace/model.pdf        Model as PDF
    public/workspace/deck.pdf         Seed deck
    server.js                         Static server, application form (/api/register), admin readback

Only `public/` is served. Anything outside it (server.js, data/) is not reachable over HTTP.

/workspace is ungated on purpose so Julian can forward it, and sends noindex + no-store headers.

Moved here on 19 Oct 2026 from expandhealthio (views/beyond-tomorrow*), where it was served at
expandhealth.io/deck/beyond-tomorrow. That URL still works until it is redirected here.

Env vars: RESEND_API_KEY, FROM_EMAIL, NOTIFY_TO, DATA_DIR (Railway volume), ADMIN_KEY.
