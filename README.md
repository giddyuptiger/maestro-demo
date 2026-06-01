# Maestro — Demo Command Center

A live, single-page demonstration of **Maestro**, the AI manager that runs the
operational layer of a creative practice. This build is personalized for
photographer / director / composer **Saam Gabbay** to show what Maestro looks
like when it's pointed at a working creative director's day.

It is an illustrative demo populated with sample data — not affiliated with Saam.

## What's on it

- **Morning brief** — a plain-language digest of where everything stands, plus the few things that genuinely need a human decision today.
- **Handled overnight** — the automation log: footage backed up & proxied, replies drafted, multicam synced, teasers cut, stills culled, invoices chased.
- **Production pipeline** — a kanban across *Pre-Production → Shoot → Edit → Score / Sound → Deliver*, with live progress and due dates.
- **This week** — the shoot/session/deadline schedule.
- **Inbox triage** — incoming mail sorted by Client / Opportunity / Press / Admin with a suggested next action on each.
- **Deliverables** — progress bars against deadlines.
- **Analytics** — time allocation, festival circuit, asset vault, billings.

## How it works

The page renders entirely from [`maestro-status.json`](./maestro-status.json) —
the same "single source of truth" pattern the real Maestro command center uses.
Swap the JSON and the whole dashboard re-paints. An inline fallback copy means it
renders even when opened directly as a file.

Pure static HTML + Tailwind (CDN) + inline SVG charts. No build step.

## Local preview

```bash
cd maestro-demo
python3 -m http.server 8000   # then open http://localhost:8000
```
