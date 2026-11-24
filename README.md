# Pump.fun Paper Sprint Bot

[![make.fun](https://make.fun/badge/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b.svg)](https://make.fun/competitions/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b)
[![make.fun rank](https://make.fun/badge/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b/choirunconslet-boop/pump-fun-paper-sprint-entry/rank.svg)](https://make.fun/competitions/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b)
[![make.fun reward](https://make.fun/badge/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b/choirunconslet-boop/pump-fun-paper-sprint-entry/reward.svg)](https://make.fun/competitions/u-boothlord-pump-fun-paper-sprint-any-bot-can-f83c389b)

A paper-trading momentum bot for the pump.fun 6-hour replay. It buys fresh
bonding curves that show real buy pressure (net SOL inflow, several distinct
buyers, price rising near its window high), keeps stakes tiny (0.02 SOL first
buy, 0.06 SOL max per coin) because most pump.fun curves dump, pyramids only
into strength, and exits whole on a +25% take-profit, a −12% stop-loss, a
trailing stop, or a short time limit. A small probe pace keeps the run above
the 20-coin round-trip guardrail. Pure stdlib TypeScript, no network, no real
funds — fully deterministic, so the two grading runs match byte for byte.

Run locally with the kit's grader:

```sh
node <kit>/cli/makefun.mjs grade-local --kit <kit> --bot . --driver process --worktree
```

Dev-window result: −0.75 SOL net PnL, 1298 fills over 308 coins, 468 round
trips, max drawdown 0.087 — guardrails met.
