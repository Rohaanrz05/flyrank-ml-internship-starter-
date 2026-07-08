# 📊 Signal Audit

## 🏷️ Project Information

| Item | Details |
|--------|--------|
| Project | Global Market AI Investment Prediction System |
| Phase | Build |
| Deliverable | Signal Audit |
| Dataset | Global Market AI Investment Dataset |
| Rows | 120,000 |
| Columns | 35 |

---

# 🎯 Objective

The purpose of this audit is to test whether commonly assumed market signals are actually visible in the data.

Rather than assuming a relationship exists, each signal is evaluated using exploratory data analysis (EDA).

### Verdict Definitions

| Verdict | Meaning |
|----------|----------|
| ✅ CONFIRMED | Data supports the hypothesis |
| ⚠️ MIXED | Some evidence exists, but results are inconsistent |
| ❌ FALSE | Little or no evidence supports the hypothesis |
| 🔄 OPPOSITE | Data suggests the reverse relationship |

---

# 📈 Dataset Distribution

## Investment Decision Distribution

![Decision Distribution](decision_distribution.png)

### Observations

- The target variable contains three classes:
  - Invest
  - Monitor
  - Avoid
- The dataset is heavily dominated by the **Avoid** class.
- The **Invest** class represents the smallest proportion of observations.
- This class imbalance should be considered during model development.

---

# 🧪 Signal Test 1 — Liquidity Score

## Hypothesis

> Higher liquidity scores are associated with Invest recommendations.

## Results

| Decision | Average Liquidity Score |
|-----------|-----------|
| Avoid | 0.5025 |
| Invest | 0.4982 |
| Monitor | 0.4992 |

![Liquidity Score](liquidity_vs_decision.png)

## Verdict

❌ **FALSE**

## Interpretation

The average liquidity scores are nearly identical across all recommendation categories.

While liquidity is often considered an important financial indicator, the dataset does not provide strong evidence that liquidity alone differentiates Invest opportunities from Avoid opportunities.

---

# 🧪 Signal Test 2 — Volatility Index

## Hypothesis

> Higher volatility is associated with Avoid recommendations.

## Results

| Decision | Average Volatility Index |
|-----------|-----------|
| Avoid | 42.57 |
| Invest | 42.80 |
| Monitor | 42.39 |

![Volatility Index](volatility_vs_decision.png)

## Verdict

❌ **FALSE**

## Interpretation

Volatility levels remain very similar across all recommendation categories.

The analysis does not support the assumption that higher volatility consistently produces Avoid recommendations.

---

# 🧪 Signal Test 3 — Social Sentiment

## Hypothesis

> Positive social sentiment is associated with Invest recommendations.

## Results

| Decision | Average Social Sentiment |
|-----------|-----------|
| Avoid | 0.00058 |
| Invest | 0.01360 |
| Monitor | 0.00232 |

![Social Sentiment](sentiment_vs_decision.png)

## Verdict

✅ **CONFIRMED**

## Interpretation

Invest recommendations show the highest average sentiment values.

This suggests that positive sentiment may be associated with favorable investment recommendations within this dataset.

---

# 🧪 Signal Test 4 — Market Trend

## Hypothesis

> Uptrend markets are more likely to receive Invest recommendations.

## Results

| Market Trend | Avoid | Invest | Monitor |
|-------------|--------|--------|--------|
| Downtrend | 32,800 | 952 | 6,511 |
| Sideways | 32,406 | 930 | 6,397 |
| Uptrend | 32,678 | 1,007 | 6,319 |

## Verdict

⚠️ **MIXED**

## Interpretation

Uptrend markets contain slightly more Invest recommendations.

However, the differences are relatively small and do not provide strong evidence of a standalone relationship.

---

# 📋 Summary of Findings

| Signal | Verdict |
|----------|----------|
| Liquidity Score | ❌ FALSE |
| Volatility Index | ❌ FALSE |
| Social Sentiment | ✅ CONFIRMED |
| Market Trend | ⚠️ MIXED |

---

# 💡 Practical Takeaways

### Key Findings

1. Social Sentiment was the strongest signal identified in the dataset.
2. Liquidity Score showed minimal separation between recommendation classes.
3. Volatility Index did not demonstrate a strong standalone relationship.
4. Market Trend showed weak evidence and may be more useful when combined with additional features.

### Implication

Investment recommendations appear to be influenced by combinations of variables rather than any single signal.

---

# ⚠️ Limitations

- Correlation does not imply causation.
- Historical market behavior may not reflect future conditions.
- Individual signals were evaluated independently.
- Some relationships may only emerge when multiple features are analyzed together.
- Results should not be interpreted as financial advice.

---

# 🏁 Conclusion

This signal audit demonstrates the importance of testing assumptions before model development.

While some commonly cited indicators showed limited standalone value, **Social Sentiment** displayed a measurable association with investment recommendations.

These findings support further investigation using multivariate machine learning models while maintaining careful interpretation of results.
