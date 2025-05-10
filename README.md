# Florida Labor Market Analysis Using Big Data

## Overview

This project analyzes Florida’s labor market trends from 2015 to 2024 by leveraging big data tools, predictive modeling, clustering, and a recommendation system. Using the Occupational Employment and Wage Statistics (OEWS) dataset and Apache Spark, we transformed raw wage and employment data into actionable insights for policymakers, workforce planners, employers, and career counselors.

## Objectives

- Analyze wage and employment patterns across 25 Metropolitan Statistical Areas (MSAs) in Florida.
- Identify regional wage disparities and top-paying occupations.
- Predict average wages based on occupation, location, and employment demand.
- Cluster occupations into labor market segments to guide workforce strategy.
- Develop a recommendation system to suggest similar occupations based on wage potential.

## Data

- **Source:** U.S. Bureau of Labor Statistics, Occupational Employment and Wage Statistics (OEWS).
- **Years Covered:** 2015–2024.
- **Variables:**
  - `Occupation_Code`
  - `Occupation_Title`
  - `City`
  - `Employment`
  - `Mean_Hourly_Wage`
  - `Entry_Hourly_Wage`
  - `Experienced_Hourly_Wage`

## Tools & Technologies

- Apache Spark (PySpark)
- MLlib (Machine Learning Library)
- SQL (Spark SQL)
- Pandas, Matplotlib, Seaborn, Plotly
- TF-IDF Vectorization
- Jupyter Notebooks / Databricks

## Methodology

1. **Descriptive Analysis:**
   - Visualized wage trends by year, occupation, and city.
   - Analyzed wage disparities using histograms, boxplots, heatmaps.
   - Identified top-paying occupations and cities.
   - Mapped wage patterns geographically using choropleth and bubble maps.
   - Analyzed wage differences across major occupational groups (2-digit SOC codes).

2. **Predictive Modeling:**
   - Linear Regression model (R² = 0.56).
   - Random Forest Regression model (R² = 0.851, RMSE = 6.18).
   - Key feature: Occupation_Code as strongest predictor.

3. **Classification:**
   - Wage Band classification using Random Forest Classifier.
   - Applied Spark-based oversampling to handle class imbalance.

4. **Clustering:**
   - K-Means clustering to segment occupations into 3 economic clusters:
     - Cluster 0: Low-wage, low-growth.
     - Cluster 1: High-wage, high-growth.
     - Cluster 2: Mid-wage, moderate-growth.

5. **Recommendation System:**
   - Built using TF-IDF and cosine similarity to suggest similar occupations based on title keywords.

## Key Findings

- Management (SOC 11) and Healthcare Practitioners (SOC 29) are the highest-paid occupational groups.
- Food Preparation (SOC 35), Cleaning (SOC 37), and Personal Care (SOC 39) occupations have the lowest wages.
- Miami and Tampa consistently lead in regional average wages; some cities show wage disparities over $180/hr.
- Occupation is the primary driver of wage differences; city and employment have smaller predictive impact.

## Real-World Applications

- Policymakers can identify wage inequality hotspots and design interventions.
- Employers can benchmark salaries across regions and occupations.
- Workforce agencies can prioritize training and upskilling in low-wage clusters.
- Career counselors and job seekers can explore recommended alternative occupations.

## What's New

- Integrated descriptive, predictive, clustering, and recommendation models in a unified Apache Spark pipeline.
- Automated data cleaning, feature engineering, class balancing at scale.
- Combined occupation-level and geographic wage analysis to bridge macroeconomic and individual insights.
- Provided interpretable, actionable outputs instead of static reporting.

## Future Work

- Integrate real-time labor market data.
- Expand analysis to additional states or national level.
- Build an interactive dashboard for public and stakeholder use.
- Include cost-of-living and industry factors for deeper modeling.

