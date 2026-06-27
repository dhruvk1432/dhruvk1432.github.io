# Dhruv Kohli Personal Site

Static personal website for GitHub Pages. The first version includes:

- Profile copy
- Research papers section for selected academic papers and research systems
- Dedicated cross-asset portfolio paper page for the v1.0.1 public release
- Option-only portfolio optimization paper entry with PDF and public
  source repository links
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

The canonical option-only Markowitz PDF filename is
`assets/papers/option_only_portfolio_optimization_dhruv_kohli.pdf`.

Source repository:
`https://github.com/dhruvk1432/Option_Only_Markowitz_Cashflow_Engineering`

## Cross-Asset Paper Release

Current website version: `v1.0.1`.

Source repository:
`https://github.com/dhruvk1432/Cross_Asset_Portfolio_Optimization`

Release tag:
`https://github.com/dhruvk1432/Cross_Asset_Portfolio_Optimization/tree/v1.0.1`

Core reproduction commands:

```bash
PYTHONPATH=src python -m xasset_portfolio.run --config configs/base.yml
python scripts/paper_qa.py
python -m pytest
FULL_RAW_REBUILD=1 make audit
make paper
```

## Publish On GitHub Pages

1. Create a GitHub repository named `dhruvk1432.github.io`.
2. Push these files to the repository's `main` branch.
3. GitHub Pages will serve the site at `https://dhruvk1432.github.io`.

If using a different repository name, enable Pages in the repository settings and publish from the `main` branch root.
