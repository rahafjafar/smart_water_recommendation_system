# Smart Water Recommendation System

## Overview
The Smart Water Recommendation System is an ML-assisted, rule-based engine designed to generate personalized water-saving recommendations based on predicted consumption and household conditions.

It combines machine learning forecasting outputs with sensor and environmental information to evaluate potential water consumption risks and provide actionable guidance.

## Methodology

### 1. Input Data
The recommendation engine uses several inputs:
- Forecasted water consumption.
- Current water tank level.
- Tank capacity and household tank information.
- Estimated hours until the next refill.
- Temperature.
- Weekend indicator.

### 2. Risk Assessment
The system calculates:
- **Risk Score (0–100):** Represents the potential water consumption and tank-related risk.
- **Water-Saving Score:** Provides a complementary indication of water-use efficiency.

The scores are used to determine the appropriate recommendation category and its priority.

### 3. Recommendation Engine
A rule-based decision layer applies seven prioritized recommendation tiers, ranging from critical tank risk to efficient usage.

Each recommendation includes:
- Risk level.
- Recommendation category.
- Priority.
- Main explanatory message.
- Suggested action.

Examples of generated recommendations include:
- Critical tank risk warnings.
- High consumption warnings.
- Usage monitoring suggestions.
- Preventive water-saving tips.
- Efficient usage feedback.

### 4. Advisor Function
The system provides a reusable function called:

`smart_water_advisor()`

This function encapsulates the recommendation pipeline and allows front-end applications, including Streamlit, to request recommendations through a single function call.

## Evaluation

The recommendation engine is evaluated using consistency-based metrics rather than regression metrics because it is rule-based.

Evaluation includes:
- **Recommendation Coverage:** Measures the percentage of records receiving a valid recommendation.
- **High/Critical Risk Consistency:** Checks whether records classified as High or Critical correspond to low projected tank levels.

The system achieves **100% recommendation coverage**.

## Saved Artifacts
- `smart_water_recommendations_3h.csv`
- `smart_water_recommendation_summary_3h.csv`

## Technologies
Python, Pandas, NumPy, Scikit-learn, Matplotlib.

## Purpose
The system transforms forecasting results and household conditions into understandable recommendations that encourage efficient water consumption and help users take preventive action before critical tank conditions occur.
