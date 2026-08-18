# LTT Analytics — Customer Churn Prediction Dashboard

**لوحة تنبؤ بتسرب العملاء — LTT Analytics**

A single-page, front-end-only analytics dashboard for predicting customer churn and acting on it in time. Built in Arabic (RTL) for LTT's analytics team, it surfaces at-risk customers, the model's top churn drivers, and one-click retention actions — all as a static HTML/CSS/JS mockup with no build step or backend required.

## Table of contents

- [Overview](#overview)
- [Features](#features)
- [Tech stack](#tech-stack)
- [Project structure](#project-structure)
- [Getting started](#getting-started)
- [Data](#data)
- [Browser support](#browser-support)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)

## Overview

Customer churn — when subscribers stop using or cancel a service — is one of the most expensive problems for a telecom/subscription business to leave undetected. This dashboard gives analytics and retention teams a single view of who is at risk, why, and what to do about it, so intervention can happen before the customer leaves rather than after.

## Features

- **Executive KPIs** — total customers, current churn rate, at-risk customer count, and monthly revenue at risk, each with period-over-period trend indicators.
- **Churn trend & forecast chart** — actual vs. predicted churn rate over time, rendered as an inline SVG line chart with hover tooltips.
- **Risk distribution** — donut chart breaking customers into high / medium / low churn risk, clickable to filter the customer table.
- **Top churn drivers** — ranked list of the factors most influencing the prediction model (usage decline, complaint frequency, late payments, network quality).
- **Retention opportunities** — high-value, high-risk customers flagged for priority intervention, with estimated recoverable revenue and a one-click "start retention campaign" action.
- **Segment breakdown** — churn rate compared across customer segments (business/consumer tiers).
- **Customer risk table** — the customers most likely to churn, filterable by time period, region, plan, and risk level, with a live search box and per-customer suggested actions.
- **AI insight callout** — a highlighted, model-generated observation about emerging churn patterns (e.g. usage drop + open complaint correlating with higher churn probability).
- **Fully RTL Arabic UI** — built with the Alexandria font and right-to-left layout throughout.

## Tech stack

- Plain HTML5, CSS3, and vanilla JavaScript — no framework, no build tooling, no package manager required to run it
- [Font Awesome](https://fontawesome.com/) for icons
- [Google Fonts – Alexandria](https://fonts.google.com/specimen/Alexandria) for Arabic/Latin typography
- Charts rendered directly as inline SVG (no charting library dependency)

## Project structure

```
.
├── index.html   # Dashboard markup and layout
├── styles.css   # Styling (RTL-aware)
├── app.js       # Sample data, rendering logic, filters, and interactions
└── README.md
```

## Getting started

This is a static site with no dependencies to install. To run it locally, either:

1. Open `index.html` directly in a browser, or
2. Serve the folder locally, e.g.:

   ```bash
   npx serve .
   # or
   python3 -m http.server 8080
   ```

   then visit `http://localhost:8080` (or the port shown).

No environment variables, API keys, or backend services are required — everything renders from the mock data bundled in `app.js`.

## Data

All customer, driver, and trend data in `app.js` is sample/mock data for demonstration purposes and does not represent real LTT customer information.

## Browser support

Built and tested against current versions of Chrome, Edge, and Firefox. It relies on modern CSS (flexbox/grid) and inline SVG, so it should work in any evergreen browser; no support is targeted for Internet Explorer.

## Roadmap

Ideas for evolving this from a static mockup into a real tool:

- Wire the UI up to a live churn-prediction API/backend instead of hardcoded sample data
- Persist filter state and support exporting the customer table (CSV/PDF)
- Add authentication and role-based views (analyst vs. account manager)
- Localize the interface for additional languages alongside Arabic

## Contributing

This is currently an internal LTT Analytics project. If you have access and want to propose a change, open a pull request or reach out to the maintainer listed below.

## License

TBD.

---

Maintained by LTT Analytics.
