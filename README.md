# 2023 NCAA March Madness Predictor

*R Markdown notebook predicting NCAA tournament game outcomes from historical team stats. Coursework for DATA 318 Data Mining, Spring 2024.*

Two models built on NCAA data from 2001-2023: a linear regression for predicting point differential and a logistic regression for predicting the winner. Trained on team-level stats like seed, win percentage, Simple Rating System, and points per game.

## Notebook

- **`predictor.Rmd`** — R Markdown with data loading, both models, evaluation, and a small example matchup demo

## Models

- **Model A: Linear regression** — predicts point differential from `seed_diff`, `win_pct_diff`, `srs_diff`, `pts_pg_diff`. Evaluated with R², p-values, and RMSE.
- **Model B: Logistic regression** — predicts winner (team1 vs team2) from `seed_diff` and `win_pct_diff`. Evaluated with ROC / AUC, kappa, and accuracy.

## Data

Historical NCAA tournament data covering the 2001-2023 tournaments, loaded directly from a public dataset URL at the top of the notebook.

## Running

Requires R with these packages:

```r
install.packages(c("tidyverse", "caret", "ROCR", "dplyr"))
```

Then knit `predictor.Rmd` in RStudio, or from R:

```r
rmarkdown::render("predictor.Rmd")
```

## Context

Coursework for DATA 318 Data Mining at Concordia College Moorhead, Spring 2024. The brief was to apply regression and classification methods to a real dataset with appropriate model evaluation.

## License

[MIT](LICENSE)
