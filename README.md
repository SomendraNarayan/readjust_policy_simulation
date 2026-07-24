# TIPS — Twin-transitions Integrated Policy Simulator

**READJUST** · EU Horizon Europe · Grant Agreement No. 101132562
**Version 7.0** · Released 24 July 2026 · engine TT-ABM-SYS (calibrated)

A hybrid agent-based simulation of the EU twin transition — the simultaneous green (decarbonisation) and digital transformation of the economy. TIPS exposes a mechanism that conventional aggregate models hide: **the gap between the policy a government sets and the policy that actually reaches firms and citizens**, governed by regional *administrative absorption capacity*.

**Live use:** open `index.html` in any modern browser — the platform is a single self-contained file with no build step, no server and no external dependencies (web fonts are loaded from Google Fonts when online; the platform works offline with system fonts).

## What it does

- **Policy Simulation Laboratory** — configure a location (EU aggregate, member states, regional groupings), a twin-transition strategy, and nine policy instruments (carbon tax, adoption subsidies, R&D matching, reskilling vouchers, emission standards, carbon dividend, infrastructure grants); run the model live and inspect 18 tracked indicators.
- **Scenario Comparison** — four pre-computed policy architectures (Baseline Path · Acceleration w/o Readiness · Reach & Capability Build · Synergy & Regional Balance), 10-seed Monte Carlo with P10–P90 bands, generated on the calibrated engine, with a short reading note under every chart.
- **Parameter Reference** — all parameters with baselines, plausible ranges, calibration status and per-parameter provenance notes; click a row for the full explanation.
- **Reproducibility** — seeded PRNG (Mulberry32); identical seed ⇒ identical run; full run data exports as JSON.

## Model in brief

50 heterogeneous firms and 100 citizens across **six regional archetypes anchored to named NUTS-2 regions** (Innovation Hub — Bayern/Stockholm; Metropolitan Core — Noord-Holland/Île-de-France; Nordic Balanced — Västra Götaland/Pohjanmaa; Industrial Transition — NRW/Śląskie; Southern Intermediate — Campania/Andalucía; Rural Peripheral — Extremadura/Podlaskie). Cobb-Douglas production with endogenous-TFP technology effects; logistic discrete-choice technology adoption; Phillips-curve wages with search-friction matching; learning-curve emissions against an EU-ETS-rate tightening cap; a three-tax fiscal loop with revenue recycling. Every policy instrument is attenuated by absorption capacity before it acts: **effective policy = nominal ambition × absorption**.

## Calibration status

Of the 97 manifest parameters: **24 empirically anchored** to named EU-27/euro-area sources for 2024–2026 (Eurostat, OECD, ECB, IEA, ACEA, European Commission), **26 literature-informed**, **47 structural** (declared model-architecture choices). The full calibrated manifest with per-parameter sources and calibration notes is in [`data/READJUST_Parameter_Manifest_Calibrated_2026-05-29.csv`](data/READJUST_Parameter_Manifest_Calibrated_2026-05-29.csv) — the same dataset deposited on the EC SyGMa portal.

## Epistemic status

Suitable for: theoretical mechanism analysis, scenario comparison, policy-design exploration, teaching, computational social science. **Not** suitable for: point forecasting of specific member-state outcomes or causal claims about actual policy magnitudes. Absolute values are in abstract model units; the analytical product is the relative comparison between scenarios.

## Documentation

The full model specification, indicator framework (MII/MCR/MER), policy-variable-to-indicator crosswalk, verification & validation programme and regional operationalisation are documented in READJUST Deliverable **D1.3** — *Factors driving inequalities in twin transition and mapping equality enablers* (public, available via the [READJUST project website](https://readjust-project.eu)) — Appendices 2–6.

## Version history

See [`CHANGELOG.md`](CHANGELOG.md). Version 7.0 corrects the labour-market accounting (natural-rate employment initialisation, labour-force-based unemployment measurement, one-period search friction) and regenerates all pre-computed comparison data; production, adoption, wage, fiscal and emissions equations are unchanged from the calibrated v6.0 engine.

## Citation

> Narayan, S. (2026). *TIPS — Twin-transitions Integrated Policy Simulator*, version 7.0. READJUST, EU Horizon Europe Grant No. 101132562. https://github.com/SomendraNarayan/readjust_policy_simulation

See [`CITATION.cff`](CITATION.cff).

## Team

**Somendra Narayan** — Lead Developer & Assistant Professor, Amsterdam Business School, University of Amsterdam
**M.T. (Taghi) Ramezan Zadeh** — Project PI & Assistant Professor, Amsterdam Business School, University of Amsterdam

READJUST consortium: University of Amsterdam · Fraunhofer ISI · VTT · EIT Food · EIT Urban Mobility · SOLIDAR · EURICE · YAGHMA

## License & funding

Licensed under the **European Union Public Licence v1.2** (EUPL-1.2) — see [`LICENSE`](LICENSE).

Funded by the European Union (Horizon Europe, GA 101132562). Views and opinions expressed are those of the author(s) only and do not necessarily reflect those of the European Union or the European Research Executive Agency (REA). Neither the European Union nor the granting authority can be held responsible for them.
