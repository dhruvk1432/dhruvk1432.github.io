# Dhruv Kohli Personal Site

Static personal website for GitHub Pages. The first version includes:

- Profile copy
- Research papers section for selected academic papers and research systems
- Dedicated cross-asset portfolio paper page for the June 2026 admission-audit build
- Option-only portfolio optimization paper entry with PDF, public source
  repository link, and bounded quantitative summary
- Simple projects section for forecasting, options, rates, and event-study work
- IAQF result bubbles without embedded charts or image-heavy sections
- Resume and contact links

## Files

```text
index.html
cross_asset_portfolio_cashflow_engineering.html
styles.css
assets/
  papers/
    option_only_portfolio_optimization_dhruv_kohli.pdf
    cross_asset_portfolio_cashflow_engineering_dhruv_kohli.pdf
    Cross_Asset_Portfolio_Construction_Cashflow_Engineering.pdf
    cross_asset_portfolio_cashflow_engineering/
      oos_equity_curve.png
      oos_drawdown.png
      objective_comparison.png
  resume/
```

The canonical cross-asset PDF filename is
`assets/papers/cross_asset_portfolio_cashflow_engineering_dhruv_kohli.pdf`.
The older `Cross_Asset_Portfolio_Construction_Cashflow_Engineering.pdf`
filename is kept as a compatibility copy and should be refreshed whenever the
canonical paper asset changes.

The canonical option-only portfolio optimization PDF filename is
`assets/papers/option_only_portfolio_optimization_dhruv_kohli.pdf`.

Source repository:
`https://github.com/dhruvk1432/Option_Portfolio_Greek_Risk_Premia`

Website summary: the paper develops a portfolio theory for books built entirely
from listed options (premium weights, Greek-induced covariance plus regularized
residual risk, structural risk-premium means, conic max-Sharpe allocation with
stress/margin/liquidity budgets inside the optimizer) and validates it under a
contract-level cost stack, volume-aware caps, exact VRO/SOQ VIX settlement, and
whole-contract execution. The headline book (56 equity-option names plus
VIX) earns a full-cost net Sharpe of 1.63 (2.01 gross) with net Sortino 4.38,
beats both a stock-Markowitz baseline and a capped naive option book (+1.34
Sharpe vs naive, p < 0.001), and holds up out of sample (rolling 36-month
refits 1.27 net Sharpe, positive purged CPCV in both designs, MC resampled and
refit p05 above 1.0, DSR 0.996); the eight-name VIX book confirms at 1.38 net.
Capacity holds at $1M NAV and fails at $5M, and a 386-check verifier re-audits
every reported number.
The site should continue to frame these as historical research simulation
results, not broker-executed alpha claims.

## Cross-Asset Paper Release

Current website build: June 2026 admission-audit rewrite.

Source repository:
`https://github.com/dhruvk1432/Cross_Asset_Portfolio_Optimization`

Current source build:
`https://github.com/dhruvk1432/Cross_Asset_Portfolio_Optimization/tree/main`

Core reproduction commands:

```bash
make reproduce
make validate
make audit
make qa
make test
make paper
```

## Publish On GitHub Pages

1. Create a GitHub repository named `dhruvk1432.github.io`.
2. Push these files to the repository's `main` branch.
3. GitHub Pages will serve the site at `https://dhruvk1432.github.io`.

If using a different repository name, enable Pages in the repository settings and publish from the `main` branch root.
