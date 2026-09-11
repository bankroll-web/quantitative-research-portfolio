# Quantitative Research Portfolio

Self-directed quantitative research focused on market microstructure, participant behavior, probabilistic modeling, walk-forward validation, and systematic experimentation.

## About Me

I am a self-taught quantitative researcher with nine years of hands-on crypto trading experience. My research approach is math-first: statistics, probability, market microstructure, machine learning, calibration, out-of-sample testing, and forward validation rather than discretionary technical analysis.

My Python work is heavily AI-assisted, but I focus on the research layer: defining hypotheses, structuring experiments, validating data, preventing leakage, interpreting results, diagnosing failures, and deciding what should or should not survive to the next research stage.

## Research Principles

- Statistics and probability over discretionary technical analysis
- Walk-forward and out-of-sample validation
- No look-ahead bias
- Historical and paper testing before capital deployment
- Negative and inconclusive results are documented
- Data quality and measurement semantics are treated as first-class research problems
- Reproducibility before complexity

## Featured Research

### 1. BTC Quantitative Market Ecology Research

A participant-ecology framework that treats retail, institutional, and other participant classes as distinct, testable components rather than a single market signal.

Highlights:
- ~26 numbered retail-positioning experiments using FXSSI data
- Statistical/probabilistic hypothesis testing
- ML ensembles and calibration
- Walk-forward testing
- 20-120 minute chronology and mechanism studies
- Prospective/live validation
- Explicit diagnosis of backtest/live mismatch rather than hiding it

[Read the project summary](projects/btc-market-ecology.md)

### 2. BTC Market Microstructure & Order-Book Research Lab

High-frequency BTCUSDT research built around trade flow and L2 order-book structure.

Highlights:
- Processed ~24.2 million raw trades into 44,640 complete one-minute July bars
- Built OFI, OBI, spread, depth, weighted midpoint, and microprice features
- Designed snapshot + incremental-update L2 reconstruction
- Added sequence validation, gap detection, resynchronization logic, and valid-state flags
- Built leakage-safe feature/label and walk-forward research scaffolding
- Used negative or inconclusive results to redesign experiments instead of optimizing around noise

[Read the project summary](projects/btc-market-microstructure.md)

### 3. Systematic Weather Forecasting & Polymarket Research

A machine-learning weather forecasting project that later expanded into prediction-market research.

Highlights:
- Historical observation pipelines
- Lag and rolling feature engineering
- Multiple model families and ensemble forecasts
- Walk-forward evaluation
- Cape Town temperature-market research on Polymarket
- Reverse-engineered Weather Underground daily-maximum reporting and Fahrenheit-to-Celsius conversion/rounding mechanics to formulate testable pricing-edge hypotheses

[Read the project summary](projects/weather-polymarket.md)

## Technical Stack

Python, pandas, NumPy, scikit-learn, DuckDB, CSV/Parquet pipelines, APIs, gradient boosting, logistic regression, time-series analysis, calibration, walk-forward validation, order-flow imbalance, order-book imbalance, spread/depth analysis, microprice, and L2 reconstruction.

## Research Status

This portfolio is active. Some projects are complete, while others are still in forward-validation or hypothesis-diagnostic stages. Research status is stated explicitly inside each project page.

## Contact

**Thabang Mahlangu Blessing**  
South Africa  
Email: blessingmahlangu729@gmail.com

Open to quantitative research, trading research, data science, and related internship or junior opportunities.
