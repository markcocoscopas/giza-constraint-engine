# Fourth Dynasty Constraint Engine

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
![Version](https://img.shields.io/badge/version-4.1-d4a855.svg)

A browser-based throughput model that tests whether the supply-side capacity of Old Kingdom Egypt could have delivered the Fourth Dynasty pyramid programme within its historically attested timelines.

The engine treats six major pyramids — Sneferu's three (Meidum, Bent, and Red) and the three at Giza (Khufu, Khafre, and Menkaure), c. 2610–2510 BCE — as a single constrained system, applying Theory of Constraints to quarrying, dressing, transport, workforce, and block placement. The scope is yours to set: analyse the whole programme, a group (Sneferu or Giza), or a single monument in isolation — solo any one build (Meidum through Menkaure), or toggle any combination of structures on and off. It also implements the Cannibalisation Hypothesis (after Choi, presented via Lee, 2026), letting you test whether deliberately overbuilding structures and then carving them down eases the programme deficit or, in fact, worsens it.

## Running it

No installation, no server, and no internet connection required. Download or clone the repository and double-click **`giza-constraint-engine_V4_1.html`** in any modern browser (Chrome, Firefox, Edge, Safari, or Vivaldi). Everything runs locally with zero external dependencies; fonts fall back gracefully when offline. Saved scenarios persist in the browser between sessions.

## What it does

- **Four capacity presets** — Lehner (1997), Stocks (2003), High, and Best Case — spanning the orthodox baseline through to every parameter at its maximum plausible value.
- **Per-stream capacity** across quarrying, dressing, transport, and placement, with a **labour allocation** split that prevents double-counting: the same worker cannot simultaneously quarry, dress, transport, and set a block.
- **Three modelling toggles** — cannibalisation, non-linear demand curves, and an Egyptian three-season workforce and water-transport model (Akhet, Peret, and Shemu).
- **Mass-conserving demand.** Non-linear and linear demand profiles are normalised per structure and per material stream, so displayed Programme Demand equals the entered masses exactly.
- **Seven analysis tabs** — accumulated deficit, demand versus capacity, per-subsystem bottlenecks, material flow, an automatic sensitivity stress-test matrix, a per-structure reverse solver, and side-by-side scenario comparison.
- **Two distinct duration metrics** — *Longest Structure* (the longest single build at current capacity) and *Programme Completion* (end-to-end length from earliest start to latest overrun-adjusted finish), each naming the binding constraint.
- **Reverse solver** that reports the annual throughput each subsystem would need to hit a target duration, compared against the same effective capacity the forward engine uses.
- **Presentation Mode** — a projector-friendly view with enlarged headline numbers, six key levers, an automatically highlighted binding subsystem, a live *baseline → changed value → consequence* readout, and a one-click Orthodox Baseline reset.

## Documentation

- **Quick start** — a one-page cheat sheet: **[`QUICKSTART.md`](QUICKSTART.md)**. A styled, printable version (open in any browser) is in **[`field-guide.html`](field-guide.html)**.
- **Full user guide** — controls, presets, calculation methods, parameter sources, and recommended workflows: **[`giza-engine-user-guide_V3.md`](giza-engine-user-guide_V3.md)**.

## Key findings the tool reproduces

Anyone running the tool can reproduce the following (figures below are non-linear, seasonal, over the 101-year programme window):

1. **Internal inconsistency.** Lehner's own capacity estimates cannot deliver the programme within the attested timelines. At Lehner defaults the accumulated deficit is roughly **12.4 million tonnes**, with about **74 of 101 years** in deficit and average core utilisation near **136%**.
2. **Cannibalisation failure.** The overbuilt-then-carved hypothesis **increases** the programme deficit in every realistic scenario — by roughly **10%** at Lehner rates, **9%** at Stocks rates, and **32%** at High capacity — because the overbuilt masses add more demand than recycling recovers, and the first structure in any chain bears the full cost with zero recycled stone.
3. **Labour alone hits a wall.** Adding workers helps but cannot close the gap at Lehner daily rates: even **100,000 workers** leaves roughly **1.8 million tonnes** of deficit, and the residual binding constraints become the boat-limited Tura and Aswan supply and transport, and granite dressing — none of which scale with workforce. Closing the programme requires higher per-channel rates, not merely more people.
4. **Best-case feasibility only.** The programme reaches essentially zero deficit only under the Best Case preset — 800 t/d quarrying, 100,000 workers, 350 working days, and correspondingly elevated transport and dressing rates — a configuration beyond any published estimate.
5. **Sneferu front-loading.** The overlapping construction of Meidum, Bent, and Red saturates the supply chain before Giza construction begins.

## Version 4.1 changes

Version 4.1 corrects several defects in the material model and reworks the interface. The numerical corrections **raise the reported deficits** relative to earlier builds (demand was previously under-counted for some streams), and they revise the workforce conclusion in finding 3 — earlier builds suggested workforce scaling alone could close the deficit, which the corrected, mass-conserving model no longer supports.

- Demand profiles are normalised per structure and per stream, so Programme Demand conserves the entered masses exactly (previously 68–106% per stream).
- Programme-year counting is inclusive and consistent (rows = years), fixing binding-frequency percentages.
- The reverse solver compares required annual throughput against the same effective capacity (workforce, labour split, and seasonal scaling) as the forward engine.
- *Longest Structure* and *Programme Completion* are reported as separate metrics.
- Added Presentation Mode; scenarios now persist to local storage; tooltips open on tap as well as hover; the CSV export uses RFC-4180 quoting and includes an active-structures column.

## Methodology and research context

This engine is a computational instrument for the **Constraint-Based Evidence Framework (CBEF)**, an approach to evaluating disputed claims in archaeology through supply-side throughput and Theory of Constraints rather than assertion. The framework and its application to the Fourth Dynasty are set out in the accompanying methodology papers (Copas, 2026). Parameter defaults are drawn from Lehner (1997), Stocks (2003), Arnold (1991), Verner (2001), Stadelmann (1997), and Hawass (2003); overbuilt masses follow Choi/Lee (2026). Dressing rates are treated as provisional pending a per-block audit against Stocks (2003); the fine casing-smoothing correction follows Haase (2012, via Arnold).

## Citation

If you use this tool, please cite it:

```bibtex
@software{copas_fourth_dynasty_engine_2026,
  author  = {Copas, Mark},
  title   = {Fourth Dynasty Constraint Engine},
  version = {4.1},
  year    = {2026},
  url     = {https://github.com/markcocoscopas/giza-constraint-engine}
}
```

## Licence

Released under the MIT Licence — see [`LICENSE`](LICENSE). The software is provided as-is, with no warranty. Note that MIT covers the code; if you wish to place different terms on the accompanying documentation and research content, consider a separate Creative Commons licence (for example CC BY 4.0) for those files.

## Author

Mark Copas, independent researcher.
