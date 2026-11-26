# Lab Submission Instructions

---

## Student Details

**Name of the team on GitHub Classroom:** 202604-B2

**Team Member Contributions:**

**Member 1**

| **Details**                                                                                        | **Comment** |
|:---------------------------------------------------------------------------------------------------|:------------|
| **Student ID:**                                                                                    | 147398 |
| **Name:**                                                                                          | Mariam Abdi |
| **What part of the lab did you personally contribute to,** <br>**and what did you learn from it?** | https://github.com/BI-course/tsf-202604-b2/tree/member1-xom-data, https://github.com/BI-course/tsf-202604-b2/tree/member1-nb1-nb2 and https://github.com/BI-course/tsf-202604-b2/tree/member1-nb7-intermediate <br><br> **Contribution:** I chose ExxonMobil (XOM) with the group, downloaded the data on 18 Nov 2026 and set it up for all notebooks. I checked the data quality (2,981 clean trading days, 6 real moves over 10% around March 2020), described the price history and candlestick chart, and explained why each predictor matters for an oil company (Brent had the strongest daily correlation, 0.53). In Notebook 2 I ran the ADF and KPSS tests (price non-stationary, log return stationary), the spurious regression experiments and the GARCH model. I also built `forecast_intermediate.csv` in Notebook 7 (naive, ARIMA, Ridge and gradient boosting 63-day forecasts with the 10–90% range) and set up the team's GitHub repository. <br><br> **What I learned:** stock prices are non-stationary, so we must forecast returns, not prices. Regressing one trending series on another can look "significant" even when they are unrelated, and more data makes this worse. The size of returns is predictable (volatility clusters, alpha + beta ≈ 0.999 in GARCH), but their direction mostly is not. Returns also have fat tails, so a normal distribution underestimates extreme days. |
**Member 2**

| **Details**                                                                                        | **Comment** |
|:---------------------------------------------------------------------------------------------------|:------------|
| **Student ID:**                                                                                    | 166110            |
| **Name:**                                                                                          | Victor Macharia            |
| **What part of the lab did you personally contribute to,** <br>**and what did you learn from it?** | https://github.com/BI-course/tsf-202604-b2/tree/member2-nb4-steps1-4 I tested whether forecasting models could predict ExxonMobil’s (XOM) closing prices better than simply assuming tomorrow’s price will remain the same as today’s. Using 2,981 trading days of historical data, I found that Ridge performed only 0.03% better than the naive model, a difference that was not statistically significant. Gradient boosting performed worse, and our testing confirmed that there was no data leakage. My conclusion is that none of the models reliably outperformed the simple “no change” forecast.           |

**Member 3**

| **Details**                                                                                        | **Comment**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Student ID:**                                                                                    | 166995                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Name:**                                                                                          | Felista Muriungi                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **What part of the lab did you personally contribute to,** <br>**and what did you learn from it?** | https://github.com/BI-course/tsf-202604-b2/tree/member3-nb4-steps11-12 and https://github.com/BI-course/tsf-202604-b2/tree/member3-classical-backtest I contributed to the classical forecasting baselines, hardware benchmarking, and financial back-testing for ExxonMobil (XOM) by evaluating six classical models with Diebold-Mariano tests and generating the 63-day ARIMA forecast path in Notebook 3 (classical_results.csv, fc63_arima.csv), benchmarking TensorFlow CPU vs. T4 GPU training times in Colab for Notebook 6 (0.9s vs. 1.0s lab size; 6.3s vs. 6.5s large), and running the transaction-cost back-test (0, 5, and 10 bp in backtest_costs.csv) alongside the next-day closing price forecast ($163.70, 10%–90% interval $159.53–$167.76 for 2026-11-10) in Notebook 4. Through this work, I learned that realistic transaction costs and turnover quickly erode modest pre-cost trading gains compared to Buy-and-Hold (17.2% vs. -4.3% for Gradient Boosting at 10 bp), lagging external predictors is critical to prevent look-ahead bias, and GPU acceleration adds data-transfer overhead rather than speedups on compact datasets. |

**Member 4**

| **Details**                                                                                        | **Comment** |
|:---------------------------------------------------------------------------------------------------|:------------|
| **Student ID:**                                                                                    |             |
| **Name:**                                                                                          |             |
| **What part of the lab did you personally contribute to,** <br>**and what did you learn from it?** |             |

**Member 5**

| **Details**                                                                                        | **Comment** |
|:---------------------------------------------------------------------------------------------------|:------------|
| **Student ID:**                                                                                    |    168657         |
| **Name:**                                                                                          |    Lisa Mburu         |
| **What part of the lab did you personally contribute to,** <br>**and what did you learn from it?** | Multi-Horizon Forecasting & Baseline Exports (Notebook 7, Steps 1–6): Ran the multi-horizon forecasting pipeline on ExxonMobil (XOM) across 1-, 5-, 21-, and 63-day horizons using leak-free walk-forward splits (gap=horizon to prevent overlapping target label leakage). Added Diebold-Mariano tests against the naive baseline across horizons, analyzed forecast skill decay as horizon length increases and effective independent sample size shrinks, and documented how the 10–90% prediction interval widens over the 63-day path. Exported and verified data/forecast_basic.csv (63 future business days with date, forecast, lower, and upper on XOM price levels) and data/forecast_backtest.csv (achieving 75.1% 1-day empirical coverage against the 80.0% target) for downstream modeling and Power BI reporting. Prediction Interval Calibration & Volatility Regimes (Notebook 4, Step 10): Implemented walk-forward quantile regression (q = 0.10 and q = 0.90) on XOM returns (runtime: 37.6s), achieving 74.3% empirical coverage against the 80.0% nominal target (a -5.7 percentage point shortfall) with an average interval width of 0.0399 (3.99%). Splitting the test window by median VIX_level (2.9145) showed 75.1% coverage on calm days versus 73.6% coverage on stormy days, reflecting volatility clustering and sharper tail swings during high-volatility regimes.   |




**Member 6**

| **Details**                                                                                        | **Comment** |
|:---------------------------------------------------------------------------------------------------|:------------|
| **Student ID:**                                                                                    |             |
| **Name:**                                                                                          |             |
| **What part of the lab did you personally contribute to,** <br>**and what did you learn from it?** |             |

**Member 7**

| **Details**                                                                                        | **Comment** |
|:---------------------------------------------------------------------------------------------------|:------------|
| **Student ID:**                                                                                    |             |
| **Name:**                                                                                          |             |
| **What part of the lab did you personally contribute to,** <br>**and what did you learn from it?** |             |

---

## Our Stock, Data and Results

| **Key**                    | **Value**                                                                                 |
|:---------------------------|:------------------------------------------------------------------------------------------|
| **Stock:**                 | ExxonMobil (XOM)                                                                          |
| **Data:**                  | Daily prices from Yahoo Finance, 2 Jan 2015 to 9 Nov 2026 (`SNAPSHOT_END = "2026-11-10"`) |
| **Date of download:**      | 18 November 2026                                                                          |
| **Power BI report:**       | `outputs/XOM_dashboard.pbix`                                                              |

## Written Verdict

**Does the model beat the naive forecast? No.** Over 1,781 test days (9 Oct 2019 to 9 Nov 2026), our best model, Ridge regression, missed the next day's closing price by $1.5806 on average (RMSE). The naive forecast "tomorrow equals today" missed by $1.5811. That gap is 0.03%. The Diebold-Mariano test gives p = 0.67, so Ridge is **not significantly** better than naive. ARMAX ($1.5920, p = 0.58) is not significantly different either. Gradient boosting ($1.5884, p = 0.036) is **significantly worse**. Ridge called the direction right on 52.2% of days, but XOM simply rose on 51.9% of them, so this is no real skill. Tuning chose a very strong penalty (alpha = 100,000), which shrinks Ridge's forecast almost to zero change, so it ends up behaving like the naive forecast. For daily returns of a large stock, this is the expected and honest result.

**How we know the test was fair.** [VICTOR: paste your "How we kept the test honest" paragraph here, shortened to about 80 words. Draft from the notebooks for you to confirm: Every model was tested walk-forward. It trained on the first 1,000 days, forecast the next 63, then moved forward (29 folds), so it never saw the days it was scored on. Nothing was shuffled. Scalers and tuning used only training data, and Ridge was tuned on the first 1,000 days only. Market predictors were lagged one day. `check_no_lookahead` passed on all 48 features, including our added `volume_ratio_10_60`. When we planted a deliberately leaky feature, R² jumped from –0.05 to 0.80, and the check caught it.]

**How much to trust the 63-day forecast.** The model puts XOM at $188.86 on 4 Feb 2027 (up 15% from $163.70), with an 80% range of $151.95 to $209.57. That range is $57.61 wide, about 35% of today's price. Treat the central line with caution: at the 63-day horizon the model's error ($13.08) was larger than naive's ($11.83), with R² of –0.26 and DM p = 0.11. Its expected rise is therefore not supported by evidence. The range is also too narrow. The next-day 80% range contained the actual price 75.1% of the time (73.6% on high-VIX days), and at 63 days only 59.0%. In practice the realistic range is wider than shown. A trading test agrees: buy and hold earned 17.2% a year, while trading long/short on gradient boosting (the better of the two back-tested models) earned 7.4% before costs and –4.3% after 10 bp costs. Ridge lost money even before costs. [STEPHANIE: one sentence on whether any neural network beat naive on XOM, with RMSE and DM p-value.]

**For the client:** we cannot forecast XOM's daily moves better than "no change". The useful output is the range, which shows how far the price could move, and even that should be read as a minimum.


## Notebook Exercises

### Notebook 1: Market Data and Candlesticks (Member 1)

1. **Most worrying line:** `non_positive_prices`. We take logs of prices to get returns, and you can't take the log of zero or a negative number. For XOM it is 0.
2. **What's missing:** timing. The 0.7 is a same-day correlation, but to forecast tomorrow we only know today's S&P 500. Same-day correlation doesn't mean it predicts the next day.
3. **Volume in a sharp fall (2020):** volume jumped to several times its normal level. Investors panic-sell, and some are forced to sell to cover losses.
4. **+50% then −50%:** simple return 1.5 × 0.5 = 0.75, so **−25%**. Log return ln(1.5) + ln(0.5) = **−0.288**.
5. **Risk decision:** real returns have more extreme days than the normal curve shows. Using the normal curve for Value-at-Risk would underestimate big losses, so too little money would be kept aside.

### Notebook 2: Stationarity and Returns (Member 1)

1. **ADF results:** the price's large p-value (0.996) means it wanders with no fixed level, so we can't forecast it directly. The log return's tiny p-value (0.000) means it moves around a stable mean, so it can be modelled and forecast.

2. **What the log did:** it didn't make the price stationary (ADF p = 0.950), but it made price moves proportional to the price level, so the spread no longer grows as the price rises. It also makes returns add up over time.

3. **n_steps 100 vs 5000:** with 100 steps, 79% of level regressions looked "significant"; with 5000, 96% did (1000 gave 92%). Changes stayed at about 6%, close to chance. More data makes spurious regression worse, not better. The fix is to use changes, not more data.

4. **Another predictor (S&P 500 vs gold):** the levels regression looks equally impressive for both (R² ≈ 0.56), yet gold has almost no daily link with XOM (changes R² = 0.0004, p = 0.30), while the S&P 500 does (changes R² = 0.24, p ≈ 0). So the levels R² tells us nothing; only changes show the real link.

5. **Where the log return sits:** with the stationary series. In Step 3 its rolling mean stays flat at about zero. Its rolling spread changes (about 0.01 normally, up to 0.05 in 2020) but has no trend, so it is stationary in its mean, with calm and stormy periods.

6. **GARCH normal vs Student-t:** with normal errors, alpha rises (0.069 → 0.079) and beta falls (0.930 → 0.918), but volatility stays very persistent. Student-t fits better: its log-likelihood is about 48.5 higher (−5351 vs −5400). Its nu of 7.2 shows XOM's returns have fat tails, so extreme days happen more often than a normal distribution allows.

---

## Scenario

Your client is a portfolio manager at a financial institution. The manager wants to know what the **closing price of one stock** is likely to do over the next trading day, the next week, the next month and the next quarter (63 business days). The manager has been disappointed before by forecasts that looked excellent on a chart and failed in practice, so the client has set one condition:

> Show me that your forecast beats the simplest possible forecast ("tomorrow will be the same as today") on days that your model never saw, and tell me honestly how uncertain it is.

You will answer that question using **real market data** and **several predictors at once**, with the methods taught in the notebooks.

---

## Dataset

1. Your group must forecast **a stock that is different from NVDA**. Choose a company whose price history is available on Yahoo Finance (for example MSFT, JPM, TSLA, NVDA, KO, or a company listed on another exchange).
2. Download the data with the helper script:

    ```shell
    python download_data.py --target MSFT
    ```

    and then set `TARGET_TICKER = "MSFT"` in `tslab/config.py`, so that the notebooks load your stock.
3. If your stock is not available on Yahoo Finance (many Nairobi Securities Exchange shares are not), download the daily prices by hand from another site and let the script clean the file:

    ```shell
    python download_data.py --target SCOM --from-csv "data/Download Data - STOCK_KE_XNAI_SCOM.csv"
    ```

    Check the quality report that the script prints. Missing days, repeated prices (no trading), and very short histories will limit what you can do, and you must say so in your report. A history shorter than about four years cannot support the walk-forward settings used in the notebooks; reduce `INITIAL_TRAIN` in `tslab/config.py` and explain your choice.
4. The predictors (S&P 500, a technology fund, VIX, 10-year yield, US dollar, Brent crude, gold) are downloaded for you. You may add or replace predictors if you can justify why they would matter for **your** stock (for example, a local index for a local stock). Predictors must be known **before** the day you forecast.
5. State the **date on which you downloaded your data**. Market data providers revise history, so the date matters.

---

## What Every Tier Must Respect

These rules apply to Baseline, Intermediate and Advanced alike. They are the reason this lab exists.

1. **Forecast the return, then convert to a price.** A one-day-ahead prediction of the closing price is the last close multiplied by `exp(predicted log return)`.
2. **Never shuffle time.** Use walk-forward (expanding window) validation, as in Notebook 3. A random train/test split on a time series is a serious error.
3. **Fit every scaler and every model on the training block only.**
4. **Tune on data that is before your test period**, never on the test period.
5. **Compare every model with the naive forecast**, and report whether the difference is statistically significant (Diebold-Mariano test). A model that does not beat the naive forecast is a valid finding. You will not lose marks for an honest negative result. You will lose marks for hiding it.
6. **Run the look-ahead test** (`check_no_lookahead`) on every feature that you add.

---

## Baseline (Required)

1. **Prepare and understand your data**
   - Run the data quality report for your stock, and plot a candlestick chart for a period of your choice.
   - Test the closing price and the log return for stationarity (ADF and KPSS), and state the conclusion.

2. **Forecast with multiple predictors**
   - Build the forecast of the next-day log return using the feature set of Notebook 4 (or an improved one), with **at least one** model from this list: ARMAX, Ridge regression, gradient boosting.
   - Evaluate it with walk-forward validation, and report RMSE, MAE, the out-of-sample R2 and the directional accuracy **next to the naive forecast**.

3. **Produce the 63-day forecast**
   - Produce a forecast of the closing price for the next 63 business days, **with a lower and an upper bound**.
   - Save it as `./data/forecast_basic.csv` (columns: `date`, `forecast`, `lower`, `upper`).

4. **Power BI**
   - Import the CSV file and create a line chart that shows the last year of actual closing prices, the forecast, and the range.

5. **A short written verdict** (about half a page, in this file or in a separate file) that a portfolio manager could understand: does your model beat the naive forecast, how do you know, and how much should the client trust the 63-day forecast?

---

## Intermediate Level (Recommended)

Everything in Baseline, and:

1. **Compare at least three forecasts**
   - The naive forecast, one classical model (ARIMA, ARMAX or exponential smoothing), and one machine learning model (Ridge or gradient boosting) with many predictors.
   - Use the Diebold-Mariano test for each model against the naive forecast.

2. **Feature ablation**
   - Run a feature group ablation (Notebook 4, Step 8) and explain, in your own words, which group of predictors helps and which does not. Remember that a very small R2 difference is not a finding.

3. **Prediction intervals**
   - Estimate a 10% to 90% range with quantile regression, and report the **coverage** (the share of actual outcomes inside the range). Comment on whether the model is overconfident.

4. **Multi-horizon results**
   - Report the skill of your model at horizons of 1, 5, 21 and 63 days (Notebook 7), and explain why it changes with the horizon.

5. **Save and visualise**
   - Save all the forecasts in one CSV file, with a separate column for each method (`./data/forecast_intermediate.csv`).
   - Create a Power BI dashboard with a line chart comparing the methods, a table of the forecast values, and a card or table that shows the error metrics of each method.

---

## Advanced Level (Optional)

Everything in Intermediate, and:

1. **A neural network**
   - Train at least one recurrent or convolutional network (LSTM, GRU or CNN) on windows of your features, using the protocol of Notebook 6: scalers fitted on the training block only, a validation share taken from the **end** of the training block, early stopping, and a fixed random seed.
   - Report the **zero-forecast baseline** loss next to your validation loss, so that a reader can see whether the network learned anything.

2. **Tuning and stability**
   - Tune at least two hyperparameters (for example the window length, the number of units, or the dropout rate) using the validation data **only**, and show the results in a table.
   - Train with at least three different seeds and report the spread of the results. Explain what the spread tells you.

3. **Save and visualise**
   - Save all the forecasts, with a column for each model and each neural network configuration, in a single CSV file (`./data/forecast_advanced.csv`).
   - Create a Power BI dashboard with comparative charts for all the models, a summary table, and a visual that highlights differences between models (for example error metrics, or the cumulative back-test curves).

4. **A back-test with costs**
   - Run the long/short experiment of Notebook 4 (Step 11) for your best model, with transaction costs of 0, 5 and 10 basis points, and compare it with buy and hold. Explain why the result is not a trading recommendation.

5. **Use of an NVIDIA GPU (optional)**
   - If you have access to an NVIDIA GPU, explain what is needed to use it for training (see the note in Notebook 6), and document the effect on training time and on the results.

---

## General Instructions

- Every CSV file must contain a date column for the forecast period.
- Use the notebooks and the `tslab` package as your guide. You may copy and adapt code from them. You must be able to **explain every line** that you submit.
- Use your own words in the written parts. Describe what **your** results show, not what the notebooks said about the NVDA data.
- Keep your results reproducible: set the random seed, state the download date of your data, and make sure the notebooks run from top to bottom after a restart of the kernel.

### Video Demonstration

For all three tiers, submit the link to a short video (not more than 4 minutes) that shows:

1. Your stock and the data quality report.
2. Your main result table, with the naive forecast in it, and what you conclude from it.
3. Your Power BI report or dashboard with the forecast and the range.

| **Key**                | **Value** |
|:-----------------------|:----------|
| **Link to the video:** | [VIDEO LINK: must open without a login] |

---

## How Your Submission Will Be Marked (Out of 100)

| #   | What you need to show                                                                                                                | Marks |
|:----|:-------------------------------------------------------------------------------------------------------------------------------------|------:|
| 1   | **Data**: a justified stock, a data quality check, a stated download date, and a stationarity analysis                               | 10    |
| 2   | **Honest validation**: walk-forward validation, no look-ahead, tuning before the test period, scalers fitted on the training block   | 25    |
| 3   | **Evaluation against the naive forecast**: metrics, the Diebold-Mariano test, and a correct reading of the result                    | 20    |
| 4   | **Modelling quality** for your tier (see the tier descriptions above)                                                                | 15    |
| 5   | **Uncertainty**: a forecast range, and (Intermediate and Advanced) the coverage of the range                                          | 10    |
| 6   | **Power BI** report or dashboard for your tier, readable by a manager                                                                | 10    |
| 7   | **Written verdict and video**: clear, honest, in your own words, within 4 minutes                                                    | 10    |

### Caps (these apply to the whole submission)

- **No naive forecast as a comparison**: your total is capped at 50.
- **Randomly shuffled train/test split, or any scaler or model that was fitted using the test period**: your total is capped at 50.
- **Features that use future information** (look-ahead bias) in the final model: your total is capped at 60.
- **Same stock as the notebooks (NVDA)**: your total is capped at 60.
- **No individual contribution documented** for a team member: minus 5 for each such member.

### Grading Approach

- Baseline = Pass >= 60%
- Intermediate = Merit 75 to 85%
- Advanced = Distinction >= 86%

A model that does **not** beat the naive forecast does not lose marks for that reason. A claim that it does, without the evidence, does.

### Before You Submit, Check

- [ ] The notebooks run from top to bottom after restarting the kernel.
- [ ] The naive forecast appears in every result table.
- [ ] The CSV files for your tier are in the `data` folder and open correctly in Power BI.
- [ ] Your written verdict says plainly whether the model beats the naive forecast.
- [ ] The video is not longer than 4 minutes and the link works without a login.
- [ ] The contribution of every team member is filled in at the top of this file.
