Signal Audit
Project Information

Project: Global Market AI Investment Prediction System

Phase: Build

Deliverable: Signal Audit

Dataset: Global Market AI Investment Dataset

Rows Analyzed: 120,000

Columns Analyzed: 35

Objective

The purpose of this audit is to evaluate whether commonly assumed market signals are actually visible in the data.

Rather than assuming a relationship exists, each signal is tested using exploratory data analysis (EDA). Results are reported using evidence-based verdicts:

CONFIRMED – Data supports the hypothesis.
MIXED – Some evidence exists, but results are inconsistent.
FALSE – Little or no evidence supports the hypothesis.
OPPOSITE – Data suggests the reverse relationship.

The analysis focuses on practical interpretation rather than causal claims.

Dataset Distribution
Investment Decision Distribution

Observations

The target variable contains three classes:

Invest
Monitor
Avoid

The dataset is heavily dominated by the Avoid class, while Invest represents the smallest proportion of observations.

This imbalance should be considered during later modeling stages.

Signal Test 1: Liquidity Score
Hypothesis

Higher liquidity scores are associated with Invest recommendations.

Method

Average liquidity scores were compared across:

Invest
Monitor
Avoid
Results
Decision	Average Liquidity Score
Avoid	0.5025
Invest	0.4982
Monitor	0.4992

Verdict
FALSE
Interpretation

The average liquidity scores are nearly identical across all decision categories.

Although liquidity is often considered important in financial analysis, this dataset does not provide strong evidence that liquidity alone distinguishes Invest opportunities from Avoid opportunities.

The signal may still contribute value when combined with other features.

Signal Test 2: Volatility Index
Hypothesis

Higher volatility is associated with Avoid recommendations.

Method

Volatility distributions and class averages were compared across investment decisions.

Results
Decision	Average Volatility Index
Avoid	42.57
Invest	42.80
Monitor	42.39

Verdict
FALSE
Interpretation

The volatility averages are very similar across all recommendation categories.

The analysis does not support the assumption that higher volatility consistently results in Avoid recommendations.

Volatility may interact with other variables, but it does not appear to be a strong standalone signal.

Signal Test 3: Social Sentiment
Hypothesis

Positive social sentiment is associated with Invest recommendations.

Method

Average sentiment values were compared across recommendation categories.

Results
Decision	Average Social Sentiment
Avoid	0.00058
Invest	0.01360
Monitor	0.00232

Verdict
CONFIRMED
Interpretation

Invest recommendations show the highest average sentiment values.

This suggests that positive sentiment may be associated with favorable investment decisions within this dataset.

However, the relationship should be interpreted as a statistical association rather than proof of causation.

Signal Test 4: Market Trend
Hypothesis

Uptrend markets are more likely to receive Invest recommendations.

Method

Market trend categories were compared against investment decision counts.

Results
Market Trend	Avoid	Invest	Monitor
Downtrend	32,800	952	6,511
Sideways	32,406	930	6,397
Uptrend	32,678	1,007	6,319
Verdict
MIXED
Interpretation

Uptrend markets contain slightly more Invest recommendations than other market conditions.

However, the differences are relatively small and do not provide strong evidence of a standalone relationship.

Market trend may be more useful when analyzed alongside other market indicators.

Summary of Findings
Signal	Verdict
Liquidity Score	FALSE
Volatility Index	FALSE
Social Sentiment	CONFIRMED
Market Trend	MIXED
Practical Takeaways

The analysis produced mixed evidence regarding common investment assumptions.

Key findings include:

Social Sentiment was the strongest signal observed in the dataset.
Liquidity Score did not show meaningful separation between recommendation categories.
Volatility Index did not demonstrate a strong standalone relationship with investment decisions.
Market Trend showed weak evidence but may contribute value when combined with other features.

These results suggest that investment recommendations are likely influenced by combinations of factors rather than any single variable.

Limitations

Several limitations should be considered:

Correlation does not imply causation.
Historical market conditions may differ from future market behavior.
Individual signals were evaluated independently.
Some relationships may only become visible when multiple variables are analyzed together.
Results should not be interpreted as financial advice.
Conclusion

This signal audit demonstrates the importance of testing assumptions before model development.

While some commonly cited indicators showed limited standalone value, Social Sentiment displayed a measurable association with investment recommendations.

The findings support continued investigation using multivariate machine learning models while maintaining careful interpretation of results.
