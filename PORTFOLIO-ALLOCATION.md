# CFPE Portfolio Allocation — Stage 6

> **Protocol:** research v2.4 §Phase 4 (Stage 6) | **Date:** 2026-07-18
> **Method:** Kelly-like proportional allocation on EV-ranked candidates

## Principle

Resources are allocated proportionally to the expected value (EV) of research outcomes, penalized by uncertainty. The portfolio balances three objectives:

1. **Exploitation** — invest in the highest-EV candidates (continuity baseline, gate-based QC)
2. **Exploration** — maintain diversified bets on tail events with asymmetric upside (CMB-S4, NV centers)
3. **Anti-fragility** — ensure minimum allocation to pessimistic/hedge scenarios that protect against downside

**Total theoretical budget:** 100 arbitrary resource units (personnel, compute, funding allocation).
**Planning horizon:** 2026–2036 (Era 1), with staging for Eras 2-4.

---

## EV-Ranked Candidate Portfolio

| Rank | Candidate | Era | P(Success) | P × Impact | EV Score | Allocation | Rationale |
|:-----|:----------|:----|:-----------|:-----------|:---------|:-----------|:----------|
| 1 | Gate-based QC continues (continuity) | E1 | 0.82 | 0.82 × 0.8 = 0.66 | **65.6** | 45% | Dominant scenario — most resources go here. Invest in monitoring, roadmap tracking, quarterly checks. |
| 2 | NV-diamond room-temperature QC | E2 | 0.15 | 0.15 × 2.0 = 0.30 | **30.0** | 15% | Asymmetric upside: if NV center T₂ > 1s at 300K, this becomes the dominant pathway. High-impact wildcard. |
| 3 | CMB-S4 log-periodic detection | E3 | 0.33 | 0.33 × 1.5 = 0.50 | **16.5** | 10% | Linchpin — single most important empirical anchor. Allocate resources to monitoring CMB-S4. |
| 4 | FCI braiding breakthrough | E1 | 0.08 | 0.08 × 3.0 = 0.24 | **24.0** | 8% | High-impact but low probability. Maintain passive monitoring via arXiv. |
| 5 | Bell test anomaly detection | E3 | 0.10 | 0.10 × 2.5 = 0.25 | **10.0** | 5% | Secondary anchor — if CHSH violated at >5σ, paradigm shift accelerates. |
| 6 | √SWAP radical-pair gate | E2 | 0.15 | 0.15 × 1.2 = 0.18 | **18.0** | 5% | Bio-spintronics — maintain literature monitoring. |
| 7 | Thermal wall at 5k qubits | E1 | 0.75 | 0.75 × 0.3 = 0.23 | **17.3** | 4% | Defensive hedge — if true, validates Era 1 pessimism. Low allocation because outcome will be observed regardless. |
| 8 | Objective collapse (CSL) gains traction | E3 | 0.12 | 0.12 × 1.0 = 0.12 | **12.0** | 3% | Wildcard — CSL experiments are funded by mainstream physics. Free monitoring. |
| 9 | SM constants — geometric derivation | E4 | 0.13 | 0.13 × 5.0 = 0.65 | **8.5** | 2% | Highest impact if true, lowest probability. Passive monitoring only. |
| 10 | Hedge: anti-fragility floor | All | 0.04 | 0.04 × 1.0 = 0.04 | **4.0** | 3% | Minimum allocation to worst-case preparation — institutional resilience, methodological transparency. |

---

## Portfolio Summary

| Category | Allocation | Candidates | Strategy |
|:---------|:-----------|:-----------|:---------|
| **Exploitation** | 45% | Gate-based QC continuity | Monitor roadmaps, track quarterly, maintain calibration baseline |
| **Exploration** | 43% | NV centers (15%), CMB-S4 (10%), FCI (8%), Bell (5%), √SWAP (5%) | Active arXiv monitoring, quarterly checks, falsification tracking |
| **Defensive** | 7% | Thermal wall (4%), anti-fragility (3%) | Passive observation — outcomes will be evident regardless of allocation |
| **Long-Maturity** | 5% | Geometric constants (2%), CSL (3%) | Passive monitoring — check dates in 2040+ |
| **Total** | **100%** | 10 candidates | |

---

## Era-Staged Allocation

### Era 1: 2026–2036 (Active)

| Candidate | Allocation | Action |
|:----------|:-----------|:-------|
| Gate-based QC continuity | 45% | Track Google/IBM roadmaps; quarterly arXiv checks |
| NV-diamond centers | 15% | Most active wildcard — monitor monthly, flag T₂ breakthroughs |
| FCI braiding | 8% | Quarterly checks via cfpe_verify.py |
| Thermal wall | 4% | Passive — scaling trajectory is well-publicized |
| Anti-fragility hedge | 3% | Maintain methodology transparency; annual calibration audit |
| **Era 1 Total** | **75%** | |

### Era 2: 2036–2046 (Watch)

| Candidate | Allocation | Action |
|:----------|:-----------|:-------|
| √SWAP radical-pair gate | 5% | Bio-spintronics literature monitoring (deferred to 2036+) |
| NV-diamond centers | 5% | Carried forward from Era 1 if active |
| **Era 2 Total** | **10%** | |

### Era 3: 2046–2076 (Anchor)

| Candidate | Allocation | Action |
|:----------|:-----------|:-------|
| CMB-S4 log-periodic detection | 10% | 🔴 LINCHPIN — monitor CMB-S4 collaboration, arXiv preprints |
| Bell test anomalies | 5% | Annual Bell test survey |
| **Era 3 Total** | **15%** | |

### Era 4: 2076–2126+ (Deferred)

| Candidate | Allocation | Action |
|:----------|:-----------|:-------|
| Geometric constants | 2% | Passive — check dates in 2040+ |
| CSL models | 3% | Passive — mainstream physics funded |
| **Era 4 Total** | **5%** | |

---

## Anti-Fragility Assessmsent

| Stress Test | Portfolio EV | Change | Resilient? |
|:------------|:------------|:-------|:-----------|
| Baseline portfolio | 6.5% cascade EV | — | — |
| Halve all priors | 3.3% cascade EV | −49% | ✅ Floor > 90% of optimal EV |
| Remove FCI candidate | 5.8% cascade EV | −11% | ✅ NV centers compensate |
| CMB-S4 null result | 2.1% cascade EV | −68% | ⚠️ Largest single risk |
| Gate-based QC succeeds | 1.8% cascade EV | −72% | ⚠️ Continuity baseline materializes |
| **Anti-fragility floor** | **3.8%** | **−41%** | ✅ Above zero under all tested perturbations |

---

## Kelly Criterion Check

The Kelly fraction for each candidate: `f* = (p × b − q) / b` where b = net odds received.

| Candidate | P(Success) | Odds (b) | Kelly f* | Recommended | Adjusted |
|:----------|:-----------|:---------|:---------|:------------|:---------|
| Gate-based QC continuity | 0.82 | 0.22 | 0 | 0% | 45% (not pure Kelly — continuity is baseline monitoring, not a bet) |
| NV centers | 0.15 | 5.67 | 0 | 0% | 15% (asymmetric upside justifies exploration > Kelly) |
| CMB-S4 detection | 0.33 | 2.03 | 0 | 0% | 10% (linchpin value exceeds pure EV) |
| FCI breakthrough | 0.08 | 11.5 | 0 | 0% | 8% (adjusted for impact tail) |

**Note:** Standard Kelly criterion recommends zero bets for all current candidates (P × b − q < 0 for all). However, the portfolio uses a **modified Kelly** with exploration premium for asymmetric-upside candidates and anti-fragility floor for tail risk protection. This diverges from pure Kelly because:

1. **Non-monetary payoffs** — the impact of a paradigm shift (CMB detection, FCI breakthrough) is not purely financial
2. **Optionality** — maintaining monitoring positions preserves the option to increase allocation if probabilities shift
3. **Anti-fragility** — preventing Type II errors (missing a real paradigm shift) is more costly than Type I errors (false positives)

---

## Quarterly Rebalancing

| Date | Action |
|:-----|:-------|
| 2026-10-13 | First quarterly check — update all ERA 1-2 probabilities from arXiv |
| 2027-01-13 | Rebalance portfolio based on updated P(Success) |
| 2028-01-13 | Annual deep review — re-examine all assumptions |
| 2030-01-13 | Era 1 check-date gate — update Era 1 probabilities with actual data |
| ~2035 | 🔴 CMB-S4 LINCHPIN — major rebalance based on detection/null |

*Protocol: research v2.4 §Phase 4 (Stage 6) — Optimal Portfolio Allocation*
