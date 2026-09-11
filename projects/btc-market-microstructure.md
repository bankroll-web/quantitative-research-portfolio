# BTC Market Microstructure & Order-Book Research Lab

## Objective

Build a reproducible high-frequency research environment for studying whether trade flow and order-book state contain short-horizon information about BTCUSDT price behavior.

## Trade-Data Pipeline

An early stage of the project processed approximately **24.2 million raw BTCUSDT trades** into **44,640 one-minute bars**, corresponding to complete July coverage.

Quality checks included:

- full minute coverage
- missing-minute detection
- NaN checks
- trade-side activity checks
- timestamp validation

The pipeline became the foundation for order-flow and short-horizon feature research.

## Microstructure Features

Research features include:

- Order Flow Imbalance (OFI)
- Order Book Imbalance (OBI)
- bid/ask spread
- depth
- midprice
- weighted midpoint / microprice
- trade intensity
- volume and trade count
- average trade size
- realized volatility
- liquidity-state features

## L2 Order-Book Reconstruction

A separate Binance Futures BTCUSDT order-book pipeline was designed around snapshots and incremental updates.

The reconstruction logic includes:

1. Initialize book state from a valid snapshot.
2. Apply incremental bid/ask updates in sequence.
3. Validate update identifiers.
4. Detect sequence discontinuities.
5. Mark the book invalid when continuity cannot be trusted.
6. Resynchronize from the next valid snapshot.
7. Calculate microstructure features only from valid reconstructed states.

Sample analysis found updates arriving on roughly 100-130 ms cadence, snapshots around 13 seconds apart, and a small but material fraction of real sequence discontinuities requiring resynchronization.

## Modeling Work

The research moved beyond simple correlation tests into expanding walk-forward probability models using features such as:

- order flow
- returns and range
- volume
- trade count
- average trade size
- rolling OFI
- realized volatility

Gradient boosting and logistic regression were benchmarked using probabilistic evaluation including AUC and Brier-score skill.

Weak or near-zero predictive results were retained rather than discarded. They motivated the move toward richer microstructure state, better timing semantics, and independent validation.

## Research Lessons

A central lesson from this project is that a statistically weak result is not automatically a failed project. A well-designed negative result can eliminate a hypothesis, expose measurement problems, or redirect research toward a more appropriate data-generating process.

The project therefore emphasizes effective sample size, overlapping-window bias, leakage prevention, sequence validity, and independent replication.

## Status

Active research. The microstructure lab provides infrastructure for testing increasingly precise hypotheses without relying on discretionary technical analysis.
