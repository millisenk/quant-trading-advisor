# financial_goals.md — cee's trading parameters

> The advisor reads this file at the start of every session. Edit the values here as
> your capital and situation change; you do not need to touch the skill logic.

## Objective
- **Monthly net-profit target:** ₱100,000 (PHP) — stretch goal, targeted after a 6-month ramp-up.
- **Horizon for ramp:** 6 months from program start.
- **Program start month:** <set, e.g. 2026-06>

## Capital
- **Monthly capital contribution:** ₱10,000 (added at the start of each month).
- **Current total tradable capital:** <update each session, e.g. ₱10,000>
- **Secured (withdrawn / safe) bucket to date:** ₱0
- **Realized profit this month so far:** ₱0

## Profit handling
- **Reinvest:** 50% of realized profit → back into tradable capital (compounding).
- **Secure:** 50% of realized profit → moved to the safe bucket, never risked.

## Risk profile — moderately-aggressive
- **Max risk per trade:** 2% of total portfolio (use 1% in choppy/neutral regimes).
- **Minimum reward:risk:** 1:2.
- **Daily loss circuit-breaker:** stop the session at −4% realized for the day.
- **Weekly drawdown brake:** at −10% from weekly equity high, cut size to 0.5%/trade until a new high.

## Markets & platforms
- **COL Financial** — PSE equities (Asian session).
- **GoTrade** — US fractional equities & ETFs (US session).
- **Extended scope** — crypto / FX allowed to bridge sessions, only when the setup's expected value beats the equity alternatives.
- **Frequency:** up to 1 trade per session, tuned weekly by the advisor's performance review.

## Default capital split (when edges are comparable)
- GoTrade (US): 60%
- COL Financial (PSE): 40%
- Shift toward whichever market shows the stronger weekly regime.

## Notes / constraints
- Advisor provides analysis only and never executes trades — cee places all orders manually.
- <add any broker minimums, untradeable tickers, tax notes, or personal rules here>
