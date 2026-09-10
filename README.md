# ChaJipsa

Vehicle Care Concierge

## Current
- Customer PWA
- Crew PWA
- Vehicle Scan Demo
- Test Vehicle: `123가1234`
- Current Prototype: v0.4

## Run
```bash
npm install
npm run dev
```

## Build
```bash
npm run build
```

## Status
- OCR: DEMO / Simulation
- Payment: DEMO
- SMS: DEMO
- Push: DEMO or not integrated
- Backend: not production-connected

## Repository Status (2026-09-10)
- PWA source (React 19 + TypeScript + Vite): **NOT YET PUSHED** — the working folder was not available in the remote session that initialized this repository. `npm install` / `npm run dev` / `npm run build` do not work until it lands.
- Current Prototype v0.4 (`prototype/chajipsa_prototype-current-v0.4.html`): **PENDING** — see `prototype/README.md`.
- Test vehicle assets (`prototype/chajipsa_assets/`): **PENDING** — no substitute images were generated.
- `prototype/archive/`: earlier MVP1 click prototype preserved for version history.
- `prototype/reference/crew-vehicle-plate-correction-demo.html`: reference implementation of the Crew Vehicle Identification safety flow (manual plate input → mismatch gate → correction request → approval simulation → work start blocking). Port target: Prototype v0.4 and PWA components `VehiclePlateManualInput` / `VehicleMismatchGate` / `VehicleCorrectionRequest`. Not yet applied to v0.4 or the PWA (sources not available).
