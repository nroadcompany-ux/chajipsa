# CHA-APP-CREW-DEMO-DRAFT-2026-09-10

Status: **DRAFT / WORKING REFERENCE — NOT CANONICAL**

Project: ChaJipsa
Date: 2026-09-10
Owner: 성재님
PM Review: ChatGPT PM
Implementation Source: Claude Code handoff

## Purpose

This document preserves the current Crew mobile vehicle-identification demo as a **working draft/reference for subsequent product planning and development**. It must not be treated as the final product specification, final UI, or canonical business rule set.

## Current Demo

- Production demo URL: https://chajipsa.vercel.app/
- Repository: `nroadcompany-ux/chajipsa`
- Crew demo path: `apps/crew-demo/index.html`
- Reported implementation commit: `0e176d1ed8215be77c1080434fcba0b426d83452`
- Branch target: `main`

## Current Demo Scope

- Mobile-only Crew vehicle-identification click demo
- Assigned vehicle vertical list
- Manual vehicle plate input
- Scan simulation
- Match confirmation
- Vehicle-number mismatch gate
- Correction request flow
- Demo approval/rejection simulation
- Work-start blocking until match or approval
- 375 / 390 / 420 px mobile review target
- Designed to support 10+ assigned vehicles through vertical scrolling

## Current Assigned Vehicle Fixtures

1. `123가1234` — SUV — 브라운·그레이 — 지하 1층 B-27
2. `26모2057` — 승용 · BMW 520d — 흰색 — 지하 1층 B-31
3. `228나5331` — 승용 · BMW 520d — 다크그레이 — 지하 2층 C-08
4. `314주4191` — 차종/색상 미확정 — 지하 2층 C-14

`314주4191`의 차종·색상은 Owner 확정 전 임의로 결정하지 않는다.

## Working Flow

Assigned Vehicle
→ Vehicle Detail
→ Vehicle Locate
→ Scan Simulation or Manual Plate Input
→ Match
→ Work Start

Mismatch path:

Plate Mismatch
→ Work Start Blocked
→ Customer Input Error Suspected / Correction Request
→ Evidence Photo Placeholder
→ `VEHICLE_CORRECTION_REQUESTED`
→ Demo Approval / Rejection
→ Approved: proceed for that Work Order only

## Guardrails

- Crew may directly input the plate number.
- Crew must not directly overwrite Customer/Master Vehicle data.
- Plate mismatch must block work start.
- Approval in this demo applies only to the relevant Work Order.
- OCR is simulation unless separately implemented and verified.
- This demo must not be interpreted as a production backend implementation.

## Owner / PM Decisions Still Open

1. `314주4191` vehicle type and color
2. Whether the non-synthetic vehicle numbers remain visible on the public demo URL
3. Repository visibility: current public vs private
4. Whether this Crew demo UX is promoted into the actual Crew PWA production baseline

## Usage Rule

Use this document and the deployed demo as **planning input / draft material** for the next Crew App design and development work.

Do not treat it as:
- final PRD
- final Screen Specification
- final Business Rule
- final Data Model
- final Production Release baseline

Any promotion to Current/Canonical requires explicit PM/Owner review.
