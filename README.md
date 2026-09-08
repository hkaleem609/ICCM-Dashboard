# IHHN · Global Fund iCCM — Malaria Surveillance Dashboard

**Zhob District, Balochistan · Jan–Aug 2026 · 12,999 encounters**

Live: https://iccm-dashboard.vercel.app/

A single self-contained HTML file. No build step, no dependencies, no network
requests — it renders offline from `file://` exactly as it does on Vercel.

## Pages

1. **Executive surveillance** — KPI band, monthly volume vs positivity, species split, Tehsil→UC→Facility positivity matrix
2. **Protocol & safety** — species vs drug administered, primaquine referral funnel, exception register
3. **Vulnerable demographics** — age–sex pyramid, pregnancy/lactation/disability, TB module status
4. **Facility / CHW scorecard** — ranked league table, reporting lag, volume vs positivity

## Headline findings

| Metric | Value | Denominator |
|---|---|---|
| Test positivity | 9.09% | 1,176 / 12,936 tested |
| *P. vivax* share of positives | 84.1% | 989 / 1,176 |
| Pf treated with AL | 92.5% | 161 / 174 |
| Pv referred for primaquine | 44.0% | 435 / 989 — **554 unreferred** |
| Pv treated with chloroquine | 1.3% | 13 / 989 |
| Positives with no drug recorded | 7.2% | 85 / 1,176 |
| Mean reporting lag | 34.7 days | n = 12,884 (0–180 d) |

Testing volume falls 2,516 (May) → 1,389 (Aug) while positivity climbs to a
**July peak of 18.88%** — rising positivity on falling test volume.

## Data protection

This is a **de-identified public build**:

- patient initials removed; exception dates coarsened to month; ages banded
- CHW names → `CHW-001…183`, facility names → `FAC-01…13` (stable pseudonyms)
- fact table carries no name, CNIC, mobile number, date of birth or family number

Every aggregate count and rate is unchanged from source and verified
programmatically against an independent recomputation.

## Deployment

Vercel deploys automatically on every push to `main`.
