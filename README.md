# ORBIT — Score. Draw. Give. ⛳

A fully client-side web application that combines golf Stableford scoring, monthly prize draws, and charity giving into a single subscription platform.

> **Built with:** React 18 (UMD) · Vanilla CSS · Babel Standalone · HTML · No build step required.

---
## Launch App 

Link : orbit-subscription-driven-web-appli.vercel.app

## Live Demo

Open `index.html` directly in any modern browser — no server, no dependencies to install.

---

## What is ORBIT?

ORBIT is a concept platform for UK golfers where:

- **Subscribers log their last 5 Stableford scores** after each round.
- **A monthly draw** picks 5 numbers (1–45). Matching 3, 4, or all 5 of your scores wins a prize.
- **10%+ of every subscription** goes to the subscriber's chosen charity partner.
- **60% of subscription revenue** funds the monthly prize pool.

---

## Features

### Subscriber Dashboard
- Log, edit, and delete Stableford scores (max 5, most recent kept)
- View upcoming draw entry status
- Track past draw results and prize matches
- Select and adjust charity contribution percentage (10–50%)
- View full winnings history with payout status

### Draw System
- Monthly draws with 5 numbers from 1–45
- Three prize tiers: 5-match Jackpot (40%), 4-match (35%), 3-match (25%)
- Jackpot rolls over if unclaimed
- Scores must be logged (1–45 range) — naturally map to draw numbers

###  Charity Partners
| Charity | Category | Impact |
|---|---|---|
| Clean Water Initiative | Humanitarian | 12,400 people served |
| Mental Health Matters | Health | 8,200 sessions funded |
| Reforestation Trust | Environment | 2.1M trees planted |
| Food Futures | Humanitarian | 3,600 families supported |
| Ocean Guardians | Environment | 140 tonnes removed |

### 🛠️ Admin Panel *(admin login required)*
| Tab | Functionality |
|---|---|
| Users | View, edit, delete all users; change plan/status |
| Draw Manager | Simulate draws (random or weighted), publish results |
| Charities | Add/remove charity partners |
| Winners | Verify winners, mark payouts as paid |
| Reports | Subscription stats, revenue estimates, charity breakdown |

---

## Demo Credentials

| Role | Email | Password |
|---|---|---|
| **Subscriber** | `demo@orbit.com` | `demo123` |
| **Admin** | `admin@orbit.com` | `admin123` |

Additional seed users: `sarah@example.com`, `tom@example.com`, `priya@example.com`, `mike@example.com` — all with password `pass123`.

---

## Project Structure

```
index.html       ← Entire application (single file)
README.md            ← This file
LICENSE              ← MIT License
.gitignore           ← Standard web project ignores
```

---

## Technical Notes

| Detail | Info |
|---|---|
| Framework | React 18 via CDN (UMD build) |
| Transpiler | Babel Standalone (in-browser) |
| Fonts | Syne (headings) + DM Sans (body) via Google Fonts |
| Storage | `localStorage` for user sessions and data persistence |
| Build | None — open the HTML file directly |
| Dependencies | Zero npm packages |

### Data Persistence
- User accounts and scores are saved to `localStorage` under the key `orbit_users`.
- Session is persisted under `orbit_session`.
- Clearing browser storage resets all data to the built-in seed data.

### Draw Logic
```
Prize pool = 60% of (active subscribers × £9.99/month)
  Jackpot  = 40% of pool  (5-number match)
  4-match  = 35% of pool
  3-match  = 25% of pool
```

---

## Subscription Plans

| Plan | Price | Notes |
|---|---|---|
| Monthly | £9.99/month | Cancel anytime |
| Yearly | £99.99/year | Saves ~£19.89 vs monthly |

---

## Design System

The UI uses a custom dark design system with CSS variables:

| Token | Value | Usage |
|---|---|---|
| `--bg` | `#07090D` | App background |
| `--amb` | `#E8A020` | Primary amber accent |
| `--grn` | `#1DBE8B` | Green / charity |
| `--red` | `#E85040` | Destructive actions |
| `--blu` | `#4A9EE8` | Info / 4-match prize |
| `--tx` | `#F0EDE8` | Primary text |
| `--mu` | `#7A8BA0` | Muted text |

---

## License

MIT — see [LICENSE](LICENSE) for details.

---

*ORBIT — A sample project · © 2026 ORBIT For Good Ltd*
