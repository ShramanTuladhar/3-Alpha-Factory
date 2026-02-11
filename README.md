# Multi-Strategy Alpha Factory

## Overview

This project explores the design, evaluation, and portfolio construction of multiple systematic trading strategies across different market regimes.

The objective was to:

- Design orthogonal alpha signals
- Evaluate each strategy independently
- Combine them into a diversified portfolio
- Reduce drawdowns while maintaining risk-adjusted returns
- Apply volatility targeting for controlled risk exposure

The focus was on robustness, diversification, and risk management rather than maximising raw returns.

---

## Strategy Components

### 1. Mean Reversion (MR)
Short-horizon reversal strategy based on recent return deviations from rolling averages.

### 2. Trend Following (TF)
Medium-horizon momentum strategy capturing persistent directional moves.

### 3. Cross-Sectional Momentum (CSM)
Relative strength strategy ranking assets and allocating capital cross-sectionally.

Each strategy was evaluated independently using time-based validation.

---

## Portfolio Construction

Strategies were combined using:

- Equal-weight allocation
- Risk-adjusted allocation
- Volatility targeting

The goal was to reduce correlation between signals and stabilise portfolio performance.

---

## Performance Summary

### Individual Strategies

| Strategy | Total Return | Sharpe | Max Drawdown | Annual Vol |
|----------|-------------|--------|--------------|------------|
| CSM      | 6.59        | 1.14   | -31%         | 29%        |
| TF       | 0.38        | 0.42   | -23%         | 13%        |

### Combined Portfolios

| Portfolio                  | Total Return | Sharpe | Max Drawdown | Annual Vol |
|----------------------------|-------------|--------|--------------|------------|
| CSM + TF                   | 3.11        | 1.14   | -22%         | 19%        |
| CSM + TF + MR              | 2.77        | 1.14   | -20%         | 18%        |
| Volatility Targeted (3α)   | 6.49        | 1.14   | -31%         | 29%        |

Key observation:

Combining orthogonal signals reduced drawdowns from ~31% (single strategy) to ~20% (combined portfolio) while preserving Sharpe ratio stability (~1.14).

Volatility targeting scaled exposure while maintaining consistent risk-adjusted performance.

---

## Methodology

- Time-series validation (no lookahead bias)
- Independent evaluation before combination
- Risk-adjusted performance metrics (Sharpe, drawdown, volatility)
- Portfolio-level risk contribution analysis
- Volatility scaling for controlled exposure

---

## Key Insights

- Diversification across strategy types improves stability.
- Sharpe ratio can remain stable even when portfolio volatility changes.
- Drawdown reduction is often more important than raw return maximisation.
- Volatility targeting preserves signal quality while controlling risk.

---

## Future Improvements

- Walk-forward optimisation
- Dynamic allocation across regimes
- Monte Carlo robustness testing
- Transaction cost modelling
- Multi-asset universe expansion


