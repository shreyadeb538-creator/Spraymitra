# SprayMitra – Smart Spray Monitoring (Prototype)

Hackathon prototype for **NESFIC-I-06: Smart Monitoring of Manual / Operator-Carried Spraying**.

## What this is
A single-file web app (`index.html`) that **simulates** four sprayers working a 12-row tea section. It shows the live coverage map, alerts, worker scores, rewards and a row-by-row audit. All sensor, GPS and worker data is simulated. There is no backend, real sensor or field data.

## Run it
1. No install needed. Double-click `index.html`, or drag it into Chrome, Edge, Firefox or Safari.
2. Optional local server: `python3 -m http.server 8000` in this folder, then open http://localhost:8000.
Works offline. Mobile friendly.

## Using it
- **Live field**: coverage map, sprayer cards, alerts (Acknowledge button).
- **Sprayer kit**: pick a sprayer on Live field, then inject faults: low pressure, rushing, over-spraying, nozzle off.
- **Team & rewards**: leaderboard and badges. **Coverage audit**: per-row result and "Generate audit summary".
- Header: pause, 4×/8×/16× speed, restart round, light/dark theme.

## Simulated vs real
| Simulated in prototype | Not built yet |
|---|---|
| Sensor readings, GPS, pace, battery | Real sensors and firmware, BLE |
| Alert rules, scoring, audit logic (real code, demo thresholds) | Backend, database, auth, offline sync |

Thresholds (for example 2.2 bar minimum, 1.1 m/s maximum pace) are demo placeholders, not validated agronomic values.

## Rebuild the PDF (optional)
`build_pdf.py` needs `reportlab`, `pillow` and screenshots in `shots/` (not included). The finished PDF is `SprayMitra_Solution_Proposal.pdf`.
