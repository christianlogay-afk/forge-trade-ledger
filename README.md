# Forge Trading public trade ledger

Every live automated trade taken by the Forge Trader Crypto model, published as a plain CSV that anyone can check.

The point of this repo is receipts. Instead of screenshots of good weeks, this is the raw log: what was bought, what was sold, at what price, and exactly what the exchange charged in fees. Red weeks stay in the file forever, and the commit history makes the timing unfakeable.

## Files

- `trades.csv` is the ledger. Columns: `timestamp_utc`, `token`, `side`, `price_usd`, `fee_usd`
- Updated automatically once a week, every Monday

## What is in here

- Every live trade the model executes on the five token markets: BTC, ETH, SOL, XRP, ADA
- The exact fee charged by the exchange on each trade
- Trades in both directions, including stop losses and losing exits

## What is deliberately NOT in here

- Account balances, equity, deposits, or withdrawals
- Position sizes in dollars, and running profit and loss
- Any strategy logic, thresholds, or source code

Those are private, and none of them are needed to verify the trade record. The claim being published is about discipline and execution, not about returns.

## How to verify it yourself

1. Download the CSV and check any row
2. Watch the commit dates. New trades only ever get appended going forward, and past rows never get edited
3. Compare the dates with the market: trades cluster in volatile windows, which is what an oversold buying model looks like

## Honest limits

- The ledger starts October 2, 2026. Earlier trades exist but predate fee capture, so they are not published here
- A ledger proves what happened, not that it will happen again
- This is not investment advice. Crypto can and does go down, and automated trading carries real risk of loss

## Product

Forge Trader Crypto free paper mode and live plans: https://forgetrading.org
