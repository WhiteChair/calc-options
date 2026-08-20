# Option Odds

A noob-friendly calculator for warrants/options that translates strike, time decay, ratio, FX and volatility into plain-English break-even and probability views.

## MVP test case

- ISIN: `DE000FG1EVX4`
- Underlying: Moderna (MRNA)
- Issuer: Société Générale
- Type: Call warrant
- Strike: $90
- Expiry: 18 Dec 2026
- Ratio: 0.1
- Example ask: €4.68

The first version intentionally keeps spot price, EUR/USD and implied volatility editable until a reliable live market-data source is connected.

## Model

The expiry payoff is:

`ratio × max(underlying - strike, 0)`

Before expiry, the app uses a Black–Scholes style call estimate, adjusted by the warrant ratio and EUR/USD. Probability outputs are model estimates for educational use, not forecasts.
