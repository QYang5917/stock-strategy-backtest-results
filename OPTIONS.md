# Option tests — results on real option prices

Tests of option trades that use signals from the same research as the stock strategy on the [main page](README.md).

**This page shows results only.** The rules and the code are kept private, so signals are named by letter and exact strikes, holding times and exit levels are left out.

**Only results priced with real traded option prices are shown.** Estimates made with simulated option prices are not on this page.

**These are hypothetical test results, not results from a live account. Nothing here is investment advice. None of these option trades is considered proven.**

## How the trades were priced

- **Same-day options (part 1):** real one-minute traded prices of QQQ and SPY options expiring the same day, February 2024 to November 2026 (about 700 trading days). One contract per trade.
- **Single-stock options (part 2):** real daily prices of weekly, monthly and six-month options, February 2024 to 2026, on 254 US companies with a market cap above 50 billion USD.
- **Costs in part 1:** on every buy and every sell, half a spread of 0.01 USD plus 0.25% of the option price, and 0.65 USD per contract. There is no history of bid and ask quotes, so the spread is an assumption.
- **Dollar figures** are for one contract per trade over the whole period, after costs.

## 1. Same-day options on QQQ and SPY

### With no signal

Buying a same-day at-the-money option with no signal lost 5% to 10% of the premium per trade. Out-of-the-money options lost far more. In every test, in-the-money did better than at-the-money, and at-the-money did better than out-of-the-money.

### The candidates kept

Two signals survived: signal P (used for QQQ puts) and signal C (used for SPY calls). The table also shows the opposite side of each signal. All rows use a strike slightly in the money.

| Trade | Trades | Winners | Average per trade | Total | Total without the 5 best | Worst drop | 2024 | 2025 | 2026 |
|---|---|---|---|---|---|---|---|---|---|
| QQQ puts, signal P | 57 | 36.8% | +14.4% | +3,368 | -979 | -1,432 | +1,057 | +299 | +2,013 |
| SPY calls, signal C | 346 | 47.4% | +1.8% | +2,200 | -916 | -1,344 | +572 | +1,098 | +530 |
| SPY puts, opposite side of signal C | 341 | 39.6% | +2.9% | +3,035 | -736 | -2,964 | +1,517 | +1,589 | -71 |
| QQQ calls, opposite side of signal P | 20 | 40.0% | -11.2% | -565 | -1,757 | -1,180 | -1,059 | +234 | +260 |
| **QQQ puts + SPY calls** | 403 | 45.9% | +3.6% | **+5,569** | +832 | -1,239 | +1,629 | +1,396 | +2,543 |
| QQQ puts + SPY calls + SPY puts | 744 | 43.0% | +3.3% | +8,604 | +3,218 | -2,783 | +3,146 | +2,985 | +2,473 |
| All four | 764 | 42.9% | +2.9% | +8,039 | +2,653 | -2,580 | +2,088 | +3,220 | +2,732 |

Totals are in USD for one contract per trade. "Worst drop" is the largest fall of the running total from an earlier high.

The pair "QQQ puts + SPY calls" at other strikes: at the money +4,441 (35.9% winners), a little further in the money +5,917 (50.5% winners).

### What a small budget does to the pair

One contract cost about 325 USD on average.

| Starting pot, never topped up | Start months tested | Pot ran out |
|---|---|---|
| 500 USD | 28 | 13 |
| 600 USD | 28 | 7 |
| 1,000 USD | 28 | 3 |
| 2,000 USD | 28 | 0 |

A normal losing run was 7 to 12 trades in a row.

### Everything else tested on same-day options

None of these was kept.

| Test | Size | Result on real prices |
|---|---|---|
| Five textbook day-trade methods with out-of-the-money options | 5 methods, 4 strikes | Every one lost. Far out of the money: 62% to 93% of the premium lost per trade. Nearer strikes: 10% to 62%. At the money: 2% to 13%. |
| The same five methods on SPY | 5 methods | The same or worse; one was about flat at the money. |
| A trend method, in-the-money options, both directions | 227 to 690 trades | Every contract lost; -3,694 at best on QQQ, -1,278 at best on SPY. |
| Signal C taken to five large stocks (weekly options) | 2,990 trades | -11,364; every stock negative. |
| Signal C on QQQ instead of SPY | 686 trades | -473. |
| Entry filters for the SPY call | 64 filters | None gave a reliable gain. The best one raised the three-part total to +9,224 on 503 trades with a worst drop of -1,623, but did not hold in earlier years. |
| Other signals for the SPY call | 15 signals | 13 lost or were about zero; the best two made +1,160 and +600. |
| Other exits, stops and strikes for the SPY call | 100 combinations | Nothing reliably better. Holding to the close lost 2,373 to 2,686. |
| Call spreads instead of a single call | 35 versions | None beat the single call; best +153, most -400 to -2,500. |
| Options expiring the next day, same signal | 346 trades | +659, against +2,200 for same-day options. |
| Next-day call held overnight | 347 trades | +6,834 with 48.4% winners, but +3 without the 5 best and a worst drop of -4,385. Not reliable. |
| A signal from unusual option volume | 47 to 62 days | No follow-through; QQQ lost 5% to 20% per trade. |
| Selling premium (spreads, flies, condors) | 192 versions | 191 lost. |
| Other buy rules on SPY, first pass | 47 rules | 46 lost. |
| A combined score of the three nearest filters | 13 rules, 50 nearby settings | No gain on real prices. |

## 2. Options on single stocks

Calls on large US companies, bought on a signal (signal S) and held for days to months. Real option prices from February 2024.

### One-week options

About 5,300 trades in total, at-the-money unless stated.

| Trade | Trades | Result |
|---|---|---|
| Call, any day (no signal) | 1,283 | +7.9% per trade at a tight spread, +5.0% at a medium spread, +0.7% at a wide spread |
| Call, on three different signals | 838 to 1,715 each | +8.7% to +10.2%; no signal reliably beat "any day" |
| Puts | same samples | -13% to -23% per trade |
| Out-of-the-money call, any day | about 1,300 | -11.8% per trade; all of the return came from the best 1% of trades |

### One-month calls

All 254 stocks, tight spread.

| Trade | Trades | Winners | Average per trade |
|---|---|---|---|
| At the money, longer hold, any day (no signal) | 2,098 | n/a | +10.1% |
| At the money, longer hold, a simpler form of signal S | 1,150 | n/a | +22.3% |
| Out of the money, any day (no signal) | 1,963 | 33% | +6.2% |
| **Out of the money, signal S** | 440 | 37.5% | **+20.6%** |
| Out of the money, signal S plus a market-wide condition | 175 | 44.0% | +32.8% |
| Out of the money, signal S without the market-wide condition | 265 | 33.2% | +12.6% |
| At the money, signal S | 395 | 44.8% | +7.1% |
| At the money, signal S plus the market-wide condition | 160 | 50.6% | +14.3% |
| In the money, signal S | 314 | 51.6% | +10.0% |
| In the money, signal S plus the market-wide condition | n/a | 56% | +16.8% |

- **Two stock samples agree:** signal S made +19.3% per trade on the 151 stocks it was designed on and +24.4% on 103 other stocks.
- **Concentration:** the best 8 of 111 entry weeks hold 99% of the profit of the signal S trade.
- **A stop on the option price made it worse:** +20.6% per trade without a stop, +10.4% with one (67% of trades were stopped).
- **Early in a weak-market period the trade failed:** 12% winners and -38% per trade (17 trades).
- **The contracts are thinly traded:** median volume was 9 to 69 contracts a day.

### Six-month calls

Rows are for an in-the-money strike. With the profit target, out-of-the-money strikes gave about the same result.

| Trade | Winners | Average per trade | Note |
|---|---|---|---|
| Signal S, held without a target | 59.6% | +29.1% | 25% of trades lost 30% or more |
| Signal S with a profit target | 81% | +16.5% | 13.8% of trades lost 30% or more |
| Signal S with a profit target and the market-wide condition | 83.5% | +20.7% | 10.8% of trades lost 30% or more |
| 17 very large companies only | 76.5% | +46% | 34 trades |
| 50 largest companies only | 72.6% | +51.7% | 95 trades |
| An alternative signal | 55.9% | +64% | 143 trades on 59 days; not kept |

- **Quoted spreads are wide:** 12% to 19% of the option price. Paying them, the profit-target version makes nothing; the version without a target survives.
- **In an account of about 50,000 USD with one contract per signal:** about +5% to +7% a year over 2024 to 2026.
- **Stops, trailing stops and time stops all made the result worse.**
- **Eleven ways of ranking signals on the same day were tested;** none held up on real prices.

## Limits of these results

- **Tests, not a track record.** No real money was traded on these rules.
- **A short, rising period.** Real option prices start in February 2024. Most calls made money in this period whatever the signal, which is why "any day" rows are shown next to the signal rows.
- **Few trades carry the totals.** Most rows are negative or close to zero without their five best trades.
- **Many versions were tried on the same data.** Several hundred variants were tested, so the best rows are flattered by selection.
- **Costs are assumed.** There is no history of bid and ask quotes; spreads on thin contracts can be much wider than assumed.
- **Small samples.** The QQQ put trade has 57 trades; several single-stock rows have fewer than 100.

## Data file

- [`data/options_same_day_real_prices.csv`](data/options_same_day_real_prices.csv) — the table of same-day candidates above.
