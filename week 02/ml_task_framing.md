# ML Task Framing

## Project Title

Global Market AI Investment Prediction System

## Chosen Lane

Advanced Lane (Mentor-Gated): Financial Market Intelligence & Decision Support

---

## ML Task Type

### Primary Task: Multiclass Classification

The objective of the system is to classify market opportunities into one of three categories:

- Invest
- Monitor
- Avoid

Each prediction represents a recommended action based on observed market characteristics.

---

## Target Variable

### Target

AI_Investment_Decision

### Possible Classes

- Invest
- Monitor
- Avoid

This target represents the recommended investment action associated with each market observation.

---

## Input Features

Examples of available features include:

- Market Type
- Country
- Asset Sector
- Trading Volume
- Market Capitalization
- Volatility Index
- Liquidity Score
- Inflation Rate
- Interest Rate
- Currency Strength Index
- Market Trend
- Economic Impact Score
- Social Sentiment

These variables provide information about market conditions and asset behavior.

---

## Success Metrics

### Primary Metrics

- Accuracy
- Precision
- Recall
- F1 Score

These metrics evaluate how effectively the model distinguishes between investment decision categories.

### Secondary Metrics

- Confusion Matrix Analysis
- Class-Level Performance Evaluation
- Error Distribution Analysis

---

## Action Supported by the Output

The prediction supports a real investment decision.

After receiving a recommendation, a user may:

- Invest in an opportunity
- Continue monitoring market conditions
- Avoid investing

The output is intended to support, not replace, human judgment.

---

## Why This Is Not Just a Fixed Rule Problem

A simple rule-based approach might suggest:

- Invest when expected returns are high.
- Avoid when risk is high.

However, market behavior is influenced by multiple interacting factors, including:

- Economic conditions
- Volatility
- Liquidity
- Market sentiment
- Global events
- Sector-specific trends

These relationships are often complex and difficult to capture through static rules.

Machine learning can learn patterns from historical observations and adapt to interactions among multiple variables.

---

## Role of Data and Machine Learning

Machine learning provides a systematic approach for analyzing large volumes of financial data.

Instead of relying solely on manually defined rules, the system can learn patterns associated with historical investment outcomes and generate data-driven recommendations.

The model functions as a decision-support tool that assists users in evaluating potential opportunities.

---

## Expected Value

Potential benefits include:

- Faster investment analysis
- Improved consistency in recommendations
- Better utilization of market data
- Enhanced decision support

The project focuses on assisting human decision makers rather than guaranteeing investment success.

---

## Risks and Responsible Use

Users should recognize that:

- Historical patterns may not repeat.
- Financial markets are inherently uncertain.
- Model predictions can be incorrect.
- Recommendations should not be interpreted as financial advice.

Outputs should be combined with human expertise and additional analysis before making investment decisions.
