# CFPE Risk Register

> **Project:** CFPE Paradigm Forecast | **Created:** 2026-07-18 | **Protocol:** research v2.4 §Phase 0.2

## Risk Matrix

| ID | Risk | Probability | Impact | Mitigation | Owner | Status |
|:---|:-----|:------------|:-------|:-----------|:------|:-------|
| R-01 | CMB-S4 null result kills Era 3-4 cascade | Medium (40%) | CRITICAL | Pre-register falsification conditions; diversify into NV-center pathway | QNFO Research | MONITOR |
| R-02 | arXiv verification pipeline drifts (no quarterly checks) | High (60%) | HIGH | Automated cron + alert on missed check; next check: 2026-10-13 | QNFO Research | MONITOR |
| R-03 | FCI thesis empirically refuted by gate-based QC scaling past 10k qubits | Medium (30%) | HIGH | Era 1 already priced at 8% optimistic; falsification register covers this | QNFO Research | ACCEPTED |
| R-04 | Methodology paper never updated after v2.0 (stale calibration) | Medium (40%) | MEDIUM | Schedule annual recalibration cycle; next: 2027-07-16 | QNFO Research | MONITOR |
| R-05 | Single-point-of-failure: one GitHub repo, one Zenodo DOI | Low (10%) | HIGH | R2 mirror active; multi-pinner IPFS distribution pending (Phase 7-8) | QNFO Research | MITIGATED |
| R-06 | Dashboard (cfpe-dashboard.pages.dev) down — forecast inaccessible | Medium (30%) | MEDIUM | Papers-server (papers.qnfo.org) serves as fallback; now live | QNFO Research | MITIGATED |
| R-07 | Institutional inertia correction (15-50yr) is untestable until decades pass | High (90%) | LOW | Calibration register entries dated; can only assess retrospectively | QNFO Research | ACCEPTED |
| R-08 | NV-center alternative pathway competes for attention, splits validation effort | Low (20%) | LOW | Falsification register covers both FCI and NV-center pathways | QNFO Research | ACCEPTED |

## Risk Summary

| Severity | Count |
|:---------|:-----|
| CRITICAL | 1 (R-01) |
| HIGH | 3 (R-02, R-03, R-05) |
| MEDIUM | 2 (R-04, R-06) |
| LOW | 2 (R-07, R-08) |

*Template: research v2.4 §Phase 0.2 | risk-register-template.md*
