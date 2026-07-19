# Fourth Dynasty Constraint Engine — Quick Start

**What it answers:** *Could the attested supply capacity of Old Kingdom Egypt actually have built the six Fourth Dynasty pyramids in their historical timelines?* Short version: under every published capacity estimate, the model still shows a shortfall against the historical timelines.

**Open it:** double-click `giza-constraint-engine_V4_1.html` in any browser. No install, no internet. That's it.

---

### 30-second orientation

- **Left sidebar = the inputs** (capacity sliders, workforce, labour split, per-structure params).
- **Top cards = the headline answer.** The one that matters is **Accumulated Deficit** — if it's above zero, the programme *cannot* be built in the stated timeline at these settings.
- **Tabs = the detail** behind that answer.
- Changed too much? Hit **RESET** (top right) to return to defaults.

### The four buttons up top

| Button | What it does |
|---|---|
| **CANNIBALISE** | Tests the overbuild-then-carve hypothesis. Watch the deficit — it gets *worse*, not better. |
| **NON-LINEAR** | Realistic demand curves (core early, casing late, granite mid-build). Leave it on. |
| **SEASONAL** | Akhet / Peret / Shemu — flood boosts labour & boats, harvest cuts them. Leave it on. |
| **PRESENT** | Projector mode — see below. |

### The presets (sidebar, top)

- **Lehner** — the orthodox baseline. Start here. → ~12.4 Mt deficit.
- **Stocks** — more conservative rates. → bigger deficit.
- **High** — generous rates + 40k workers. → still short.
- **Best Case** — 800 t/d, 100k workers, 350 days. → the *only* setting that closes it, at rates beyond any published estimate.
- **Scope is yours** — **Solo** any single build (Meidum → Menkaure), toggle structures **On/Off**, or use **Sneferu Only / Giza Only / Full Dynasty**. Run one monument or any combination, not just the whole programme.

### Reading the top cards

- **Accumulated Deficit** — total stone the programme falls short by. **>0 = infeasible.**
- **Core Util** — average core-chain load. **>100% = over-committed.**
- **Bottleneck** — the subsystem that binds most often. *This is what to attack.*
- **Longest Structure** vs **Programme Completion** — one build vs the whole end-to-end programme (they differ; that's expected).

### The seven tabs

1. **Deficit** — the headline curve. Rising = systemic failure.
2. **Demand/Cap** — annual demand vs the capacity ceiling.
3. **Bottlenecks** — *which* subsystem fails, and how often (the binding-frequency bars).
4. **Material Flow** — core / casing / granite demand over time.
5. **Sensitivity** — auto stress-test; the **◀ KEY LEVER** row is the input worth changing.
6. **Reverse Solver** — set a target duration, see the annual throughput each subsystem would need.
7. **Scenarios** — SAVE a setup (persists across refreshes) and compare side by side.

### Try this in two minutes

1. Load **Lehner** (default). Note **Accumulated Deficit ≈ 12.4 Mt**.
2. Open the **Bottlenecks** tab — see what's binding (placement / core quarry early on).
3. Drag **Peak Workforce** up to 100,000. Deficit drops… but *doesn't* hit zero — it plateaus. Boat-limited Tura/Aswan supply and granite dressing don't scale with people.
4. Toggle **CANNIBALISE** on — watch the deficit get *worse*. That's the headline result.

### Presentation Mode (for showing others)

Click **PRESENT** for big numbers and a plain-English status line ("*Required throughput exceeds capacity by X Mt, with Y binding for Z years*"). Six key levers only, the binding subsystem auto-highlighted, a live *baseline → changed → consequence* readout, and a one-click **Orthodox Baseline** reset.

### Gotchas

- **Labour % must total 100** (sidebar warns in red if not).
- **Programme Demand should equal your entered masses** — it's mass-conserving now (v4.1); if it doesn't match, a structure param is off.
- Export the year-by-year table with **⬇ EXPORT CSV**.

*Full detail: [`README.md`](README.md) · [`giza-engine-user-guide_V3.md`](giza-engine-user-guide_V3.md)*
