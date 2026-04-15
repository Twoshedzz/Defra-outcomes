# Defra Outcomes Framework (accessible prototype)

This repository demonstrates that **an accessible version of the Defra Outcomes Framework**—proper headings, lists, expandable sections, and outcome owners in plain text—is **straightforward to publish** using the [GOV.UK Prototype Kit](https://prototype-kit.service.gov.uk/) and structured content. It contrasts with flipbook or image-heavy formats that are harder to use with assistive technology, search, and reflow.

## What’s here

- **`/outcomes`** — readable page built from `app/data/outcomes.json` (owners, EIP notes, SoS pillars, resilience outcomes).
- **`content/`** — Markdown reference extracts and an **infographic** screenshot for visual hierarchy (`content/reference/defra-outcomes-framework-infographic.png`).

## Run locally

```bash
npm install
npm run dev
```

Open [http://localhost:3000/outcomes](http://localhost:3000/outcomes).

## Deploy on Render

The kit is a **Node web app** (not static hosting). On [Render](https://render.com), use a **Web Service** wired to this repo.

1. **Build command:** `npm ci` (or `npm install` if you prefer). Avoid mixing **Yarn** with `package-lock.json` — Render may default to Yarn if no lockfile is detected; this repo includes `package-lock.json`, so npm is the right choice.
2. **Start command:** `npm start` (runs `govuk-prototype-kit start`, same as production serve).
3. **Defaults in this repo (`app/config.json`):** `useAuth` and `useHttps` are set to **`false`** so the site is **reachable without a kit password** and **without HTTPS redirect loops** behind Render’s proxy (logs like `Password is not set` and `Redirecting request to https` should stop after redeploy). This suits a **public accessibility demo**; do not use that pattern for sensitive prototypes.

To **protect** the deploy with a password instead: remove `useAuth` / set `"useAuth": true`, set environment variable **`PASSWORD`** on Render, and typically set **`USE_HTTPS=false`** there as well (or rely on config). See [kit publishing](https://prototype-kit.service.gov.uk/docs/publishing-on-the-web).

Optional: use the included `render.yaml` as a Blueprint or copy its `buildCommand` / `envVars` into an existing service.

## Licence

See `LICENCE.txt` (GOV.UK Prototype Kit starter licence). Confirm any Defra-specific content against official sources before wider publication.
