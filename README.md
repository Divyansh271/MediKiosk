# MediKiosk prototype

Static browser prototype for a guided clinical-intake kiosk. It is intentionally a frontend-only preview: all visit state is held in memory and is cleared when the simulated routing flow is complete.

## Included workflow

- Language selection, ABHA marker, family-profile selection, and first/returning visit mode
- Guided voice-or-touch symptom intake with a safety/priority marker
- Optional document upload flow with simulated OCR fields and an interaction-review marker
- Granular consent screen, clinician-controlled editable summary, and simulated FHIR routing
- Session purge control, offline-queue marker, audio guidance, and text-size accessibility control

## Run locally

Open `index.html` directly, or from this folder run a static server such as:

```powershell
python -m http.server 4173
```

## Vercel preview deployment

This is a zero-build static project. Import this folder in Vercel and deploy using the `Other` framework preset. No environment variables or database are required for the prototype.

## Important prototype boundary

The controls intentionally simulate ASR, OCR, FHIR/ABHA routing, and offline sync. A production implementation would place authenticated API services and a consent/audit model behind these screens; no health data should be handled by the static prototype.
