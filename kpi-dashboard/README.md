# KPI Dashboard

A self-updating KPI page that refreshes itself when you open it — with plain-
language commentary on what moved and why, not just charts that redraw.

Built by MBL Partners (https://mblpartners.com) — part of the Thrive with AI
skill library.

---

## What It Does

Operates in two modes, detected automatically:

**Setup (first run)** — asks three questions:
- Which three to five KPIs do you actually report on?
- Where do these numbers live?
- How often do you report: weekly, monthly, or quarterly?

Saves those answers as a config block and builds the initial dashboard page.

**Refresh (later runs)** — reads the saved config, pulls current numbers from
each source, recomputes metrics versus the prior period, rewrites the
commentary, and regenerates the page. Tells you what changed since last time
in two or three sentences.

The output is a single self-contained HTML page. The commentary under each
chart is the product — one honest sentence per metric on what moved and the
likely why, same structure every period so trends are comparable.

---

## Install

1. Download `kpi-dashboard.skill`
2. Open Cowork
3. Drag the `.skill` file into your Cowork window
4. The skill installs automatically and is ready to run

---

## How to Run It

Once installed, trigger it by saying any of the following:
- "Build my KPI page"
- "KPI dashboard"
- "Make my metrics dashboard"
- "Dashboard that updates itself"

---

## Output

A single self-contained HTML page with:
- Each KPI as a number, its trend versus the prior period, and a small chart
- One sentence of plain-language commentary per metric
- Three to five configured metrics only — no vanity clutter
- A config block at the top so Refresh runs know what to pull

---

## Learn More

This is one page. The full operating system that runs your briefings, recaps,
and reviews the same way:
https://mblpartners.com/thrive-individual
