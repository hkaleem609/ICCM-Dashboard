# IHHN · Global Fund iCCM — Malaria Surveillance Dashboard

**Nushki & Zhob Districts, Balochistan · Jan–Sep 2026 · 22,148 encounters**

Live: https://iccm-dashboard.vercel.app/

A single self-contained HTML file. No build step, no dependencies, no network
requests — it renders offline from `file://` exactly as it does on Vercel.

## Pages

Sidebar navigation across five dashboards, one global filter bar (period, district,
tehsil, union council, facility, result, age band, sex), click-to-filter charts, shareable
filter URLs, CSV export, print, and light/dark themes.

1. **Executive overview** — KPIs with trends, monthly volume vs positivity, species mix, positivity by union council, auto-generated key signals
2. **Case management & safety** — treatment by species, primaquine referral cascade, monthly adherence, referral vs average by UC, exception register
3. **Patient demographics** — age–sex pyramid, positivity by age, vulnerable groups, TB module status
4. **Facility & CHW performance** — facility workload, CHW score distribution, reporting lag, CHW scorecard
5. **Data quality** — completeness, missing fields, lag spread, benchmark reconciliation

## Headline findings

| Metric | Value | Denominator |
|---|---|---|
| Test positivity | 6.98% | 1,542 / 22,086 tested |
| *P. vivax* share of positives | 85.3% | 1,315 / 1,542 |
| Pf treated with AL | 95.3% | 204 / 214 |
| Pv referred for primaquine | 45.2% | 595 / 1,315 — **720 unreferred** |
| Pv treated with chloroquine | 1.1% | 15 / 1,315 |
| Positives with no drug recorded | 4.0% | 61 / 1,542 |
| Mean reporting lag | 35.8 days | n = 21,962 (0–180 d) |

| District | Tehsil | Encounters | Positives | TPR | PQ referral |
|---|---|---|---|---|---|
| Nushki | Nushki | 7,523 | 175 | 2.3% | 35.3% |
| Zhob | Zhob | 13,253 | 1,117 | 8.4% | 45.8% |
| Zhob | Kaker Khurasan | 1,372 | 250 | 18.2% | 50.2% |

Positivity rises from 2.5% (Mar) to a **July peak of 12.56%** while monthly volume falls
from 3,765 (May) to 1,967 (Sep). Kaker Khurasan runs at twice Zhob tehsil's positivity
and nearly eight times Nushki's.

## Data protection

This is a **de-identified public build**:

- patient initials removed; exception dates coarsened to month; ages banded
- CHW names → `CHW-001…291`, facility names → `FAC-01…26` (stable pseudonyms)
- fact table carries no name, CNIC, mobile number, date of birth or family number

Every aggregate count and rate is unchanged from source and verified
programmatically against an independent recomputation.

## Deployment

Vercel deploys automatically on every push to `main`.
