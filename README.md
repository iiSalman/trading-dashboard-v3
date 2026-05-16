# trading-dashboard-v3 — SaaS Basic-tier preview

UI preview of the planned subscription product. v2 stays live at
[iisalman.github.io/trading-dashboard-v2](https://iisalman.github.io/trading-dashboard-v2/);
v3 explores what the **Basic plan** interface would look like for paying customers.

Live preview: **[iisalman.github.io/trading-dashboard-v3](https://iisalman.github.io/trading-dashboard-v3/)**

## What's different from v2

- Tier badge ("Basic Plan") in the header
- Fake account chip + "Upgrade to Pro" CTA
- Locked **Pro Features** section (Custom Watchlists, Alerts, Backtest, API)
- Pricing modal with Free / Basic / Pro comparison
- Visible "Preview build" disclosure that data still comes from v2's free pipeline

## Data

v3 fetches the same JSON snapshot served by v2 at
`https://iisalman.github.io/trading-dashboard-v2/data/snapshot.json`
— GitHub Pages sends `Access-Control-Allow-Origin: *`, so cross-origin fetch
works with no backend changes.

No workflow, no Render proxy, no commits to v3 from the cron — every refresh in
v2 automatically appears in v3 within 5 min.

## Roadmap

- Pro-tier interface mockup (next milestone) — same repo, same URL, separate
  view toggled by the Upgrade CTA.
- When the paid SaaS ships for real, swap `DATA_URL` for the licensed
  real-time WebSocket feed.
