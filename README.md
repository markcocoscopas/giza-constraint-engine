# Fourth Dynasty Constraint Engine

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

A browser-based throughput model that tests whether the supply-side capacity of Old Kingdom Egypt could have delivered the Fourth Dynasty pyramid programme within its historically attested timelines.

The engine treats six major pyramids — Sneferu's three (Meidum, Bent, and Red) and the three at Giza (Khufu, Khafre, and Menkaure), c. 2610–2510 BCE — as a single constrained system, applying Theory of Constraints to quarrying, transport, workforce, and block placement. It also implements the Cannibalisation Hypothesis (after Choi, presented via Lee, 2026), letting you test whether deliberately overbuilding structures and then carving them down eases the programme deficit or, in fact, worsens it.

## Running it

No installation, no server, and no internet connection required. Download or clone the repository and double-click **`giza-constraint-engine_V4_1.html`** in any modern browser (Chrome, Firefox, Edge, Safari, or Vivaldi). Everything runs locally with zero external dependencies; fonts fall back gracefully when offline.

## What it does

- **Four capacity presets** — Lehner (1997), Stocks (2003), High, and Best Case — spanning the orthodox baseline through to every parameter at its maximum plausible value.
- **Labour allocation** across quarrying, transport, and placement that prevents double-counting: the same worker cannot simultaneously quarry, transport, and set a block.
- **Three modelling toggles** — cannibalisation, non-linear demand curves, and an Egyptian three-season workforce and water-transport model (Akhet, Peret, and Shemu).
- **Seven analysis tabs** — accumulated deficit, demand versus capacity, per-subsystem bottlenecks, material flow, an automatic sensitivity stress-test matrix, a per-structure reverse solver, and side-by-side scenario comparison.
- **Duration calculator** for each structure that reports real build time at current capacity and names the binding constraint.

## Documentation

The full user guide — controls, presets, calculation methods, parameter sources, and recommended workflows — is in **[`giza-engine-user-guide_V3.md`](giza-engine-user-guide_V3.md)**.

## Key findings the tool reproduces

Anyone running the tool can reproduce the following:

1. **Internal inconsistency.** Lehner's own capacity estimates cannot deliver the Giza programme within the attested timelines; the accumulated deficit at Lehner defaults exceeds nine million tonnes.
2. **Cannibalisation failure.** The overbuilt-then-carved hypothesis increases the programme deficit by roughly 3–43% (depending on capacity assumptions), because the overbuilt masses add more demand than recycling recovers, and the first structure in any chain bears the full cost with zero recycled stone.
3. **Workforce requirements.** Reaching zero deficit at Lehner's daily rates needs roughly 70,000–100,000 workers, three to four times the orthodox estimate of 25,000.
4. **Best-case feasibility only.** The programme closes only at capacity levels (800 t/d quarrying, 100,000 workers, and 350 working days) that no Egyptologist has proposed or defended.
5. **Sneferu front-loading.** The overlapping construction of Meidum, Bent, and Red saturates the supply chain before Giza construction begins.

## Methodology and research context

This engine is a computational instrument for the **Constraint-Based Evidence Framework (CBEF)**, an approach to evaluating disputed claims in archaeology through supply-side throughput and Theory of Constraints rather than assertion. The framework and its application to the Fourth Dynasty are set out in the accompanying methodology papers (Copas, 2026). Parameter defaults are drawn from Lehner (1997), Stocks (2003), Arnold (1991), Verner (2001), Stadelmann (1997), and Hawass (2003); overbuilt masses follow Choi/Lee (2026).

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
