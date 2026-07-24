# Changelog

## v7.0 — 24 July 2026
First public release, under the name TIPS (Twin-transitions Integrated Policy Simulator).
- Labour-market accounting corrected: employment initialised at the calibrated natural rate
  (removing the artificial 100%-unemployment start-up transient), unemployment measured over
  the participating labour force rather than the whole population, hiring bounded by
  participation, and a one-period search friction so separated workers re-enter matching the
  following period. Production, adoption, wage, fiscal and emissions equations are unchanged.
  Levels shift relative to v6.0 (scenario orderings are preserved); analyses published from
  v6.0 remain valid as results of that version.
- Scenario-comparison data regenerated on the corrected engine (10 seeds, sampled every third step of a 60-step run), replacing pre-calibration data.
- Scenario naming corrected: S1 "Acceleration w/o Readiness" and S2 "Reach & Capability Build" (the two differ in absorption capacity, not in green-vs-digital emphasis).
- Parameter Reference now generated directly from the calibrated manifest CSV (single source of truth), with calibration-status filter and per-parameter explanations.
- Reading notes added to every Scenario Comparison chart; version chronology added to the About page.
- Licensed under EUPL-1.2; citation metadata added.

## v6.0 — 29 May 2026 (calibrated edition)
- Parameter manifest calibrated: 24 of 97 parameters anchored to named EU-27/euro-area sources (2024–2026); 18 baselines re-set (capital share 0.39, NAIRU 6.3%, MPC 0.856, ETS tightening 4.3%/yr, depreciation 6%, reinvestment 22%, participation 0.74, replacement rate 0.60, among others).
- Region-weighted absorption: policy delivery to each firm blends national absorption with regional administrative capacity.
- Metric classification layer separating direct agent-state measures from derived indices; JSON run export; manifest–code consistency check; advanced mode (seed, steps, population size).

## v5.0 — April 2026
- Single-file public build: 97-parameter engine, six regional profiles, Monte Carlo comparison with P10–P90 bands, EU policy templates, location contexts.

## v4.0 — April 2026
- Engine hardening after internal review: labour-market search frictions, affordability-constrained hiring, bounded innovation accumulation, adoption saturation; regression suite over corrected defects.

## v3.0 — March 2026 (TT-ABM-SYS MVP)
- First complete platform: S0–S3 scenario architecture, eleven-diagnostic testing suite, documentation set.

## v2.0 — November 2025
- Policy instrument set formalised (A1–F1); scenario configuration made data-driven.

## v1.0 — September 2025
- First JavaScript port of the Python model underlying READJUST Deliverable D1.3; single stylised economy, same 97-parameter space.
