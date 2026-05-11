---
name: options-trade-planner
description: Use when the user asks for an options trade idea, covered call, cash-secured put, spread, hedge, earnings options setup, or risk-defined options plan for stocks or ETFs.
---

# Options Trade Planner

## Purpose

Design options trades with defined risk, explicit entry and exit rules, and scenario analysis. Prefer simple structures unless the user requests complexity.

## Required Research

Use current option chain and market data before giving strikes or expirations. Check:

1. Underlying price and trend
2. Implied volatility and IV rank when available
3. Liquidity: bid-ask spreads, open interest, and volume
4. Earnings, dividends, and major event dates
5. Support, resistance, and expected move
6. Greeks: delta, theta, vega, and assignment risk
7. Maximum gain, maximum loss, breakeven, and buying power impact

## Strategy Selection

Choose based on thesis:

- Bullish conservative: cash-secured put, bull put spread, covered call adjustment
- Bullish aggressive: call debit spread, long call only when liquidity and timing justify it
- Neutral income: covered call, short put spread, iron condor
- Bearish: put debit spread, bear call spread
- Hedge: protective put, collar, index put spread
- Event trade: use defined-risk spreads and size small

Avoid naked short options unless the user explicitly asks and understands margin risk.

## Output Format

Use this structure:

## Thesis

State the directional view, time horizon, and invalidation point.

## Recommended Structure

| Leg | Action | Strike | Expiration | Estimated Price | Delta |
|---|---|---:|---|---:|---:|

## Risk / Reward

Include max gain, max loss, breakeven, probability considerations, and position size.

## Management Plan

State profit target, stop-loss, adjustment rule, and when to close before expiration.

## Alternative

Offer one simpler or more conservative alternative.

## Compliance

Options are high risk. Do not imply guaranteed income or returns. Include assignment and liquidity risk.
