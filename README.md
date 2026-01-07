# mlb-feature-importance-analysis
MLB feature importance analysis
MLB Next‑Season WAR Prediction Model
A machine‑learning system that predicts a hitter’s next‑season WAR using multi‑year MLB performance data.

Overview
This project builds a predictive model that estimates a hitter’s next‑season WAR based on their current‑season performance. Using qualified MLB hitters from 2015–2024, the system constructs a player‑level dataset with a shifted WAR target (“Next_WAR”), engineers key offensive features, and trains a Random Forest model to forecast future value.
The goal is to understand which offensive metrics best predict year‑ahead performance and to evaluate the model’s accuracy using standard regression metrics and feature importance analysis.

Key Components
1. Multi‑Year Data Pipeline
- Pulled qualified hitters (min PA) from 2015–2024 using pybaseball
- Grouped players by FanGraphs ID (IDfg)
- Shifted WAR forward one season to create a Next_WAR target
- Removed incomplete seasons to ensure clean training data
2. Feature Engineering
Selected performance indicators include:
- Age
- Games (G)
- Plate Appearances (PA)
- AVG, OBP, SLG, OPS
- wOBA
- wRC+
- ISO
- BABIP
These features capture contact quality, plate discipline, and overall offensive production.

Modeling Approach
- Train/test split (80/20)
- Random Forest Regressor with 100 trees
- Evaluation metrics:
- MSE
- RMSE
- R²
This model structure captures non‑linear relationships and avoids the over‑extrapolation common in linear models.

Feature Importance Analysis
The project includes a visualization ranking all features by their contribution to predicting next‑season WAR. This helps identify which offensive skills are most predictive of future value.
