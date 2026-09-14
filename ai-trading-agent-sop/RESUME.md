# AI Trading Agent — RESUME (for a fresh chat)

Last updated: 2026-09-14. Copy the prompt at the bottom into a new chat to continue the loop, once this account is funded and trading has actually begun.

## Current state (snapshot)
- **Account:** Robinhood Agentic account, nicknamed "Agentic", ••••6751 (`822956751`), account type `limited_margin`, `agentic_allowed: true`. NEVER trade the other two accounts on file — ••••3991 (`515523991`, margin, default) or ••••6422 (`439656422`, cash, nickname "Brody G") — both `agentic_allowed: false`, read-only to the agent.
- **Funding:** NOT YET FUNDED. Balance confirmed $0 (cash, equity, buying power) as of 2026-09-14. Do not evaluate or place any trade until funding is confirmed via `get_portfolio` on ••••6751.
- **Authorization:** No autonomy override granted. Default SOP Phase 1 applies — every buy/sell proposal requires explicit approval before any order is placed. Robinhood's own "review before action" gate should be kept ON.
- **Portfolio:** No positions. No trade history on this account.

## Live positions (entry → synthetic stop / take-profit)
None yet — account is unfunded and no trades have been placed.

## Standing config
- **Social layer:** not yet authorized. Per the SOP default, decide on and log a social-layer authorization decision before relying on it (see SKILL.md's "Operating discipline" section for the model this was adapted from — a live news/social layer, if authorized, can disqualify or trigger an exit but never originate a buy).
- **Watchlists:** none created yet.
- **Loop cadence:** not yet started. Loop runs only while a session is live — no overnight/unattended monitoring, per the SOP.

## Hard limits (never waived)
Long US equities/ETFs only; no options/crypto/leverage/penny/<$5/<$2B/OTC; ≤35% per position; ≥5% cash; no chase >15% since source buy; no earnings within 2 trading days; EDGAR code-P + non-10b5-1 + 2+ insiders required for every insider buy. Loop runs ONLY while a session is live — no overnight/unattended monitoring.

---

## COPY THIS INTO A FRESH CHAT:

```
Resume the AI trading agent. FIRST read these for full state:
- ai-trading-agent-sop/RESUME.md (current positions, stops, config — start here)
- ai-trading-agent-sop/SKILL.md (the SOP + hard rules)
- ai-trading-agent-sop/trade-log.md (full history)

Trade ONLY the Robinhood Agentic account 822956751 (••••6751). NEVER touch the
other two accounts on file (••••3991, ••••6422). No autonomy override is active —
Phase 1 (explicit approval required before every trade) applies unless I've told
you otherwise in this chat.

Then run one check now to confirm clean resume: get_accounts + get_portfolio on
822956751 to confirm current funding and any positions, and report status. If
still unfunded, stop there and report — do not run signal discovery or propose
trades against an unfunded account.
```
