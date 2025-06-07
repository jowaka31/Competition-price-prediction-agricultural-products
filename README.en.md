![img](./README_ASSETS/데이터-AI를_활용한_물가_예측_경진대회.png)

# Price Forecasting Competition Using Data & AI

## Organized by

- Digital Platform Government Committee
- Ministry of Agriculture, Food and Rural Affairs

## Hosted by

- Korea Agro-Fisheries & Food Trade Corporation (aT)
- National Information Society Agency (NIA)

## Sponsored by

- The Korean Society of Artificial Intelligence (KSAI)

## Period

- October 1, 2024 – November 14, 2024

## Participation & Award

- **Type**: Individual (Solo)
- **Award**: Excellence Prize (President of KSAI Award)
- **Prize**: KRW 5,000,000

---

## Competition Overview

### Preliminary Round 1

- **Objective**: Predict prices of 10 key agricultural products closely related to daily life  
  _(Cabbage, Radish, Onion, Apple, Pear, Dried Red Pepper, Peeled Garlic, Potato, Green Onion, Lettuce)_

- **Approach**:

  1. **Tree-based prediction without scaling**:
     - Scaling was skipped to **maximize the strength of tree-based models**.
  2. **Two model designs**:
     - **Single-output model**:
       - Predicts each product’s price independently at a specific time.
       - Strong for detailed prediction per item.
     - **Multi-output model**:
       - Predicts prices of multiple products simultaneously.
       - Reflects correlations among products, improving **overall prediction stability**.
  3. **Time series data modeling**:
     - Tree-based models were trained on time-series price data.
     - Combined both single and multi-output models to ensure **robust forecasting** across time.
     - Captured both individual volatility and inter-item correlations.

- **Result**:
  - **Advanced to Round 2**:
    - Simplicity and efficiency of the model design were highly evaluated.

---

### Preliminary Round 2

- **Objective**: Predict prices of the same 10 agricultural products

- **Approach**:

  - Continued use of **tree models without scaling**.
  - Same time-series strategy as Round 1, now enhanced with:
    - **Price slope prediction models** using external variables (e.g., weather, supply/demand data, retail/wholesale prices, import/export factors).

- **Key Analyses and Improvements**:

  1. **Volatility Analysis**:

     - Identified **significant price fluctuations** in agricultural products.
     - Addressed limitations of average-based models by explicitly designing for volatility.

  2. **Multi-dimensional Prediction**:

     - Generated three outputs per prediction: **Upper Bound**, **Average**, and **Lower Bound**:
       - **Upper Bound**: reflects risk of price surges.
       - **Average**: reflects general trend.
       - **Lower Bound**: reflects risk of price drops.

  3. **Feature Engineering with Predicted Values**:

     - Used the three predicted values as **features for the next time point’s prediction**.
     - Calculated the **momentum (rate of change)** of predictions to incorporate time trend signals.

  4. **Momentum-Weighted Averaging Model**:

     - Applied **dynamic weights** to upper, average, and lower predictions based on recent momentum.
     - Used **weighted averages** to generate stable forecasts that align with actual trends.

  5. **Enhanced Interpretability**:
     - Final prediction as a combination of upper/mid/lower bounds enables:
       - Easier interpretation of predictions.
       - Informed decision-making for various scenarios.

- **Result**:
  - Advanced to Final Round with improved accuracy via volatility-aware modeling and momentum weighting.

---

### Final Round

- **Objective**:
  - Submit a report detailing the logic and outcomes of the model.
  - Present results at the 2024 Government Fair.

---

## Key Achievements

- Excellence Award Winner (President of the Korean Society of AI)
- KRW 5,000,000 in prize money
- Recognized for the model's **practicality and originality**, with a presentation opportunity at the Government Fair.
