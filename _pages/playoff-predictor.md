---
layout: single
title: NBA Playoff Prediction Algorithm
permalink: /portfolio/playoff-predictor/
header:
  overlay_image: /images/76.jpg # Add the path to your splash image
  overlay_filter: 0.5 # Optional: Adjust the filter opacity for better title visibility
  overlay_full: true  # Makes the header full-width
  actions:
    - label: "Visit GitHub"
      url: "https://github.com/AviShah10/nba-playoff-prediction"
---

_Please visit our team's [GitHub page for the project](https://github.com/AviShah10/nba-playoff-prediction/)_

In this group project for CS 4641 (Machine Learning), we created several models to predict playoff performance of NBA teams, based only on the first half of the season's data. We gathered data directly from the NBA, and set the cutoff date for data at the midpoint of each season (2000-2022). The 2020, 2021, and 2022 seasons were left as a validation dataset.

The main objective was to discover what statistics (features in the ML models) were the most influential in playoff performance, hypothetically allowing for a blueprint for teams that want to improve on the most important metrics. An SVM, Random Forest, Decision Tree, and Logistic Regression classifier were all tested to predict a playoff clinch vs playoff miss. In our models, the highest correlating stats were half-season Win-Loss % (obviously), Plus/Minus, and Field Goal Percentage.

<div style="text-align: center;">
  <img src="/images/correlators.png" alt="correlators" style="max-width: 90%; height: auto; border-radius: 10px;">
  <p><em>Table of all features and correlations with playoff clinch </em></p>
</div>

Notably, some statistics commonly cited as being influential in the NBA were much lower correlators than expected. This includes Free Throw Attempts/Makes, Field Goal Attempts, and Offensive Rebounding, possibly indicating lower importance to drawing fouls and high volume shooting rather than efficiency and defensive rebounding. The three highest correlating features were also plotted to show the clear distinction between playoff and non-playoff teams.

<div style="text-align: center;">
  <img src="/images/3feats.png" alt="3 features" style="max-width: 60%; height: auto; border-radius: 10px;">
  <p><em>Plot of FG%, WL%, and +/-, with red indicating playoff clinch</em></p>
</div>

The models had great success in predicting which teams made the playoffs in our testing datasets, as shown.

<div style="display: flex; justify-content: space-around; flex-wrap: wrap; text-align: center;">
  <div style="flex: 1; margin: 10px;">
    <img src="/images/results22.png" alt="results 2022" style="max-width: 100%; height: auto; border-radius: 10px;">
    <p><em>Example prediction for 2022 season</em></p>
  </div>
  <div style="flex: 1; margin: 10px;">
    <img src="/images/results.png" alt="" style="max-width: 100%; height: auto; border-radius: 10px;">
    <p><em>Performance of each ML model on NBA playoff prediction</em></p>
  </div>
</div>





**Skills Used:**
- Machine Learning (Scikit-learn)
- Data Engineering
- Open-Source Datasets
- Data Visualizations
