# Turning Supply Chain Chaos into Decisions: A Data-Driven Approach

Student: Imran Qureshi
Faculty Advisor: Dr. Yi-Chin Lin
Frank G. Zarb School of Business, Hofstra University, Hempstead, NY 11549 

---

# Background and Problem

Global supply chains operate in an environment defined by constant and growing uncertainty. Disruptions caused by geopolitical conflict, severe weather, and economic instability make delivery timelines increasingly unpredictable and difficult to manage. As a result, delays are no longer isolated operational issues; they directly impact customer satisfaction, contractual obligations, and overall business performance for companies and governments alike.

Because of this, relying on reactive decision-making is no longer sufficient. Companies and governments must adopt predictive, data-driven approaches that allow them to anticipate disruptions before they occur and respond more effectively. This project focuses on identifying the key drivers of supply chain delays and transforming complex data into actionable insights that support better operational decisions and insights before the ships leave the port. 

---

# Objectives

* Identify the key variables that contribute to supply chain delivery delays.
* Analyze how external risk factors (geopolitical, weather, and economic) influence delivery outcomes and corrective actions.
* Develop predictive models using decision trees and k-nearest neighbors (kNN) to classify delivery status and delay severity.
* Evaluate how these models can support proactive, data-driven decision-making in supply chain operations.



---

# Methods

## Data Preparation

* Cleaned numeric + formatted date variables
* Encoded categorical variables (route type, product category, transport mode) into factors
* Filtered dataset when needed (e.g., focusing only on delayed shipments)

## Feature Engineering

* Created cost per kilogram metric
* Binned Cost per Kg, Geopolitical Risk, Weather Index, and Inflation Rate
* Applied log transformation to skewed variables and standardized variables (z-score normalization) for modeling consistency

## Modeling Approach

* Built two models:

  * Decision Trees (`rpart`) → for interpretability
  * k-Nearest Neighbors (kNN) → for nonlinear pattern detection
* Tuned parameters:

  * kNN → number of neighbors (k)
  * Decision Tree → cp, max depth, min split

## Validation & Evaluation

* Used cross-validation to prevent overfitting
* Evaluated models using Accuracy, Kappa (accounts for imbalance), Sensitivity, Specificity



---

# Discussion Implications

* Companies already optimize for cost and efficiency, but they increasingly redesign logistics strategies by diversifying routes and reducing reliance on known bottlenecks such as the Suez Canal.
* Disruption response is often reactive, but leading supply chain teams improve response time by implementing predefined playbooks that guide actions such as expedited shipping or rerouting in addition to data-driven insights.
* Predictive models are becoming integrated into operations, allowing firms to identify high-risk shipments in advance and adjust transportation modes or inventory allocation before delays escalate.
* Decision-making in supply chains is frequently inconsistent across teams, but interpretable models like decision trees enable organizations to standardize responses using clear and repeatable rules.



---

# Technologies Used

## Languages & Platforms

* Excel
* R
* Power BI

## R Libraries

```r id="tvyht"
library(rpart)
library(rpart.plot)
library(caret)
library(class)
library(dplyr)
library(ggplot2)
```

---

# Visualizations Included

* Best Decision Tree — Delivery Status
* Best Decision Tree — Delay Bin
* Best Decision Tree — Corrective Action
* Delay Frequency Time Series
* Route Type Delay Severity Distribution
* Geopolitical Risk Severity Analysis
* Monthly Shipment Status Pie Charts

---

# Conclusions

* Geopolitical risk and weather severity were not as strong of predictors concerning whether a delay would occur, challenging common assumptions about their direct impact on delivery status.
* Route type emerged as the most significant factor influencing the severity of delays, with the Suez Canal in particular acting as major bottlenecks for extended disruptions.
* The type of disruption event, particularly geopolitical conflict, as well as key industries such as semiconductors and pharmaceuticals were key predictors in determining the appropriate mitigation strategy once a delay occurred.
* Decision tree models provided clear, interpretable rules that distinguished between predicting delay occurrence, delay duration, and corrective actions with an 80-90% accuracy rate, matching or beating kNN results.



---

## Data Source and License
This project uses the *Global Supply Chain Disruption and Resilience* dataset by Bertnardo Mario Uskono, obtained from Kaggle: https://www.kaggle.com/datasets/bertnardomariouskono/global-supply-chain-disruption-and-resilience
Copyright © Bertnardo Mario Uskono
Licensed under the Apache License, Version 2.0.
You may obtain a copy of the License at: http://www.apache.org/licenses/LICENSE-2.0

---

# Contact

LinkedIn: https://www.linkedin.com/in/imran-qureshi25/
Phone Number: 8607224490
Email: [iqureshi1@pride.hofstra.edu](mailto:iqureshi1@pride.hofstra.edu)



---

# Reference

1. Uskono, B. M. (n.d.). *Global supply chain disruption and resilience* [Data set]. Kaggle.
   [https://www.kaggle.com/datasets/bertnardomariouskono/global-supply-chain-disruption-and-resilience](https://www.kaggle.com/datasets/bertnardomariouskono/global-supply-chain-disruption-and-resilience). Licensed under the Apache License, Version 2.0.
