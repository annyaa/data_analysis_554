# data_analysis_554
Data analysis tutorials for lecture 12 bmmb 554

## Anscombe's Quartet Analysis

An exploration of Anscombe's Quartet — four datasets with nearly identical summary statistics that look completely different when visualized.

### Files

| File | Description |
|---|---|
| `anscombe_quartet.tsv` | Source data — 4 datasets (I–IV), 11 (x, y) observations each |
| `analysis.ipynb` | Jupyter notebook with full analysis, statistics, and plots |
| `plan.md` | Iterative planning log |

### Notebook contents

1. **Data loading** — reads `anscombe_quartet.tsv` with pandas
2. **Descriptive statistics** — per-dataset summary (mean, std, min/max, median) and a correlation/regression table showing how similar all four datasets are numerically
3. **Scatter + regression line plots** — 2×2 grid with OLS line overlaid per dataset
4. **Residual plots** — 2×2 grid of residuals vs. fitted values
5. **Box plots** — marginal distributions of x and y across all four datasets
6. **Violin plots** — kernel density shape added to box plot information
7. **Q-Q plots** — normality check on residuals per dataset
8. **Commentary** — interpretation of what each dataset reveals

### Exported plots

Each plot is saved as a PNG (150 dpi) in the project directory:

- `scatter_regression.png`
- `residual_plots.png`
- `box_plots.png`
- `violin_plots.png`
- `qq_plots.png`

Each of the four datasets is assigned a consistent color across all plots (blue, pink/red, green, orange).

### Running the notebook

Open `analysis.ipynb` in VS Code and select the **Python 3 (ipykernel)** kernel (Python 3.12.1). Click **Run All** or press `Ctrl+Shift+P` → `Run All`.

### Key finding

All four datasets share the same mean, variance, correlation (~0.816), and regression line (~y = 0.5x + 3.0), yet their scatter plots reveal fundamentally different structures: a clean linear relationship (I), a curve (II), a linear trend with one outlier (III), and a degenerate case driven by a single leverage point (IV).
