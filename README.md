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

## Licence

See `LICENCE.txt` (GOV.UK Prototype Kit starter licence). Confirm any Defra-specific content against official sources before wider publication.
