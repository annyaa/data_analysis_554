# An analysis of Anscombe data

#Goal: analyze the data, make visualizations, decide what to do next with the data

## Implementation

- First, Obtain data from anscombe_quartet.tsv
- Seond, examine the data then generate descriptive statistics
- Next, create a Jupyter Light Notebooks in whch you generate plots
- Afterwards, Propose different types of plots that would work if generated for the data
- Then, Save this proposal to the end of the file so I can have a look at it
- I need to approve the plan and tell you to go ahead before we actually do anything. Please ensure the plan is appended to the end of this file for me to review.


---

## Proposed Analysis Plan (awaiting approval)

### Data Overview
- 4 datasets (I, II, III, IV), each with 11 (x, y) observations
- This is Anscombe's Quartet — a dataset designed so all four groups share nearly identical summary statistics but have very different visual patterns

### Descriptive Statistics to Generate (per dataset)
- Count, mean, standard deviation, min, max, median for both x and y
- Pearson correlation coefficient between x and y
- Linear regression coefficients (slope, intercept)
- Key finding to highlight: all four datasets produce nearly identical stats

### Jupyter Notebook Structure
The notebook (`analysis.ipynb`) will be organized as:
1. **Data loading** — read `anscombe_quartet.tsv` with pandas
2. **Descriptive statistics** — `df.groupby('dataset').describe()` and per-group correlation/regression summary table
3. **Plots** — see section below
4. **Commentary** — brief interpretation of why the datasets look so different despite identical stats

### Proposed Plot Types

| Plot | Purpose | Notes |
|---|---|---|
| **Scatter plot (2x2 grid)** | Show raw (x, y) distribution per dataset | The essential Anscombe visualization |
| **Scatter + regression line (2x2 grid)** | Overlay OLS line on each scatter plot | Illustrates how the same regression line fits very different shapes |
| **Residual plots** | Plot residuals vs. fitted values per dataset | Reveals non-linearity (II), outlier influence (III), and degenerate variance (IV) |
| **Box plots** | Compare x and y distributions across datasets side-by-side | Highlights that marginal distributions also look similar |
| **Violin plots** | Same as box plots but with kernel density shape | More informative about distribution shape than box plots |
| **Q-Q plots** | Check normality of residuals per dataset | Shows normality holds for I but not for II, III, IV |

### Recommended Primary Plots
For a concise notebook, the most informative combination is:
1. Scatter + regression line (2x2) — the classic view
2. Residual plots (2x2) — the diagnostic view
3. A summary statistics table showing how identical the numbers are across all four groups


## Iteration 1
- go ahead to execute your plan
- save it all in a jupyter notebook I can start in this instance of vs code
- explain to me how to start a jupyter notebook so I can validate your results

## Iteration 2
- plots should be more colorful - each panel should have different colors
- export all output as png files 