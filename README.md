# Predicting House Prices with Linear Regression

How much of a house's price can a straight line explain? This notebook uses the classic **Boston housing** data to build intuition for linear regression: fitting a line, measuring how good it is, and, most importantly, checking it on data it has never seen.

## What the notebook does

1. **One-feature regression.** Fit a line to a single predictor and find the parameters θ that minimise the mean squared error (MSE). This makes the idea concrete: the best line is the one with the smallest squared distance to the data.
2. **Another way to measure performance.** MSE is in squared units and hard to interpret, so the notebook also uses the **R² score**, the fraction of the variance in prices the model explains (1 is perfect, 0 is no better than predicting the mean).
3. **Splitting the data.** The data is divided into a **training** set (used to fit) and a **test** set (used only to evaluate). This is the step that separates "memorised the data" from "learned something general".

## What the results show

| Measure | Value |
|---|---|
| MSE (before splitting) | 21.9 |
| R² on the test set | **0.714** |
| MSE on the test set | 23.5 |

The test MSE is slightly worse than the one measured on the full data, which is what we expect: a model almost always looks better on the data it was fitted to. An R² of about 0.71 says that the linear model explains roughly 71 % of the variation in house prices on unseen data: a good result for such a simple model, but not the whole story.

## What you can take from this

- A linear model is the right first baseline: fast, interpretable, and often surprisingly strong.
- Always report performance on held-out data; training error is optimistic.
- MSE and R² answer different questions. MSE tells you the typical size of the errors, R² tells you how much of the variation you captured.

## Files

- `master.ipynb`: the full analysis with code, plots and commentary
