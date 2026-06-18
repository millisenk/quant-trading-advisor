# Quant Trading Advisor — Cowork Plugin

Your dedicated, aggressive-but-disciplined quantitative trading advisor and portfolio
manager, packaged as an installable Cowork plugin. It runs market-recommendation
sessions across PSE, US, crypto and FX, sizes every trade to a strict 1–2% risk budget,
and logs your end-of-day (EOD) placements into a built-in Excel tracker that compounds
toward a monthly net-profit target with automatic 50% profit reinvestment.

## What's inside

```
quant-trading-advisor/
├── .claude-plugin/
│   ├── plugin.json          # plugin manifest
│   └── marketplace.json     # lets you add this folder as a local marketplace
├── skills/
│   └── trading-advisor/
│       ├── SKILL.md         # the advisor logic (Mode A report / Mode B EOD logging)
│       ├── config/
│       │   └── financial_goals.md   # YOUR parameters — edit these
│       └── assets/
│           └── Trading_Tracker.xlsx # the 6-month capital tracker
└── README.md
```

## Install

1. Move the whole `quant-trading-advisor` folder somewhere permanent on your computer.
2. In Cowork, open **Settings → Capabilities → Plugins** and add a local marketplace
   pointing at this folder (it contains `.claude-plugin/marketplace.json`), then install
   **quant-trading-advisor**. The `trading-advisor` skill activates automatically.
3. Open `skills/trading-advisor/config/financial_goals.md` and set your real numbers
   (starting capital, current capital, start month). Do the same in the Settings tab of
   `Trading_Tracker.xlsx`. Keep a working copy of the tracker in the folder you use with Cowork.

## How to use it

**Start a session (get setups):**
> "Start my tracking session" — produces the dated Market Recommendation Report:
> live regime read, capital split between COL/GoTrade (+ optional crypto/FX), one sized
> setup per session, and your progress to target.

**Log end of day (update the tracker):**
> "Log my EOD: bought VOO 0.9 @ 512.40, stop 506, closed +₱540."
> The trade is appended to `Trading_Tracker.xlsx`, capital recomputes, the 50/50
> reinvest/secure split updates, and you get a one-line status vs. the ₱100k target.

**Automate it (optional):**
> "Run my market report every trading morning at 8am." — sets up a scheduled task.

## The tracker tabs

- **Settings** — your inputs (blue cells only).
- **Trade Log** — one row per trade; risk %, R-multiple and cumulative P/L auto-calc.
- **Monthly Dashboard** — 6-month ramp: deployed capital, 50% reinvested / 50% secured,
  % to ₱100k, and a feasibility flag per month.
- **Reality Check** — the honest math: how much capital ₱100k/month actually requires,
  and a realistic growth projection so you can adjust the plan instead of over-leveraging.

## Ground rules baked in (non-negotiable)

- The advisor **analyses and sizes only — it never places orders.** You execute every trade.
- Hard ceiling of **2% portfolio risk per trade**; minimum **1:2 reward:risk**.
- **Daily −4% circuit-breaker** and **−10% weekly drawdown brake** cut size automatically.
- Aggression is expressed through setup quality and frequency, never by oversizing —
  protecting the compounding base IS the strategy.

## A straight word on the target

₱100,000/month in net profit, funded by ₱10,000/month contributions, implies a return
rate on a small capital base that no disciplined strategy can guarantee. The Reality Check
tab makes the gap explicit: at a strong-but-realistic ~15%/month, ₱100k/month needs a
capital base near ₱650k+ — far beyond what six months of ₱10k contributions plus profits
will build. Treat ₱100k as the North Star, hit the monthly milestones the dashboard shows,
and let the tool tell you honestly when the target needs more capital, more time, or a
revision. That's how the account survives long enough to grow.
