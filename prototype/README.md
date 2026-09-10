# Prototype Archive

Purpose: keep the HTML prototypes that preceded the PWA, for regression comparison and Owner review.

| Slot | File | Status |
|------|------|--------|
| Current Prototype v0.4 | `chajipsa_prototype-current-v0.4.html` | PENDING — not present in the remote workspace on 2026-09-10; add the file here without modification |
| Test vehicle assets | `chajipsa_assets/test-vehicle-123ga1234.png`, `chajipsa_assets/test-plate-123ga1234.png` | PENDING — use the bundle delivered by 성재님 / ChatGPT PM; do not substitute other images |
| Earlier version | `archive/chajipsa_prototype-mvp1-click-2026-09-10.html` | ARCHIVED — MVP1 click prototype (D-015 Screen Map basis), exported from the Claude Code artifact "차집사 프로토타입" on 2026-09-10. This is **not** v0.4; example plate in it is `12가 3456`. |

Rules
- Do not rewrite v0.4 when adding it; commit the file as delivered.
- Prototypes here are static HTML and are not part of the PWA build.

## Reference implementations

| File | Purpose | Status |
|------|---------|--------|
| `reference/crew-vehicle-plate-correction-demo.html` | Crew 차량번호 입력·정정 요청 Flow (P0) reference demo. Fixtures `123가1234` (SUV, 브라운·그레이), `26모2057` (승용 BMW 520d, 흰색) and `228나5331` (승용 BMW 520d, 다크그레이), all DEMO, switchable on the Work Order screen; mismatch examples `123가5678` / `26모2075` / `228나5313`. States: `VEHICLE_CORRECTION_REQUESTED / APPROVED / REJECTED`. Approval applies to one Work Order only; Master Vehicle never changes from the crew screen. | DONE as standalone reference. NOT yet merged into v0.4 HTML or the PWA. |
