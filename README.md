# DemaFora You

**Discover you.**

Physician-supervised ketamine therapy — at-home, all 50 states.

## Site Structure

| File | URL | Description |
|------|-----|-------------|
| public/index.html | / | Landing page |
| public/intake.html | /intake | 9-step eligibility intake (Phase 1) |
| public/assessment.html | /assessment | Adaptive clinical assessment (Phase 2) |
| public/documents.html | /documents | Patient documents hub |
| public/consent-treatment.html | /consent-treatment | Informed consent — ketamine therapy |
| public/consent-telehealth.html | /consent-telehealth | Telehealth consent |
| public/hipaa-notice.html | /hipaa-notice | HIPAA notice of privacy practices |
| public/pre-post-instructions.html | /pre-post-instructions | Pre/post-treatment instructions |
| public/financial-agreement.html | /financial-agreement | Financial agreement + cancellation policy |
| public/medical-history.html | /medical-history | Medical history intake form |
| public/patient-faq.html | /patient-faq | Patient FAQ |

## Tech Notes

- All pages are static HTML — no framework, no build step
- Server just needs to serve static files from public/
- Each document page links back to /documents
- Intake routes to /assessment on qualification; soft decline on disqualifiers
- Assessment scores PHQ-9 (depression), GAD-7 (anxiety), PCL-5 (PTSD), numeric pain scale (chronic pain)
- All forms have print-friendly CSS (@media print)

## Brand

- Primary: #4a7c6a (sage green)
- Background: #faf9f6 (cream)
- Font: Georgia (serif) + Arial (sans labels)
- Tagline: "Discover you."

## Status

Currently deployed on Tailscale at http://100.91.83.21:9010

Next steps:
- Register demaforayou.com
- Deploy to Railway or Azure Container App
- Wire document routes to server.js
- Add form submission backend (DB, physician review queue, email triggers)
- Karpa API integration for clinical intake
