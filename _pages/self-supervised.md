---
layout: single
title: Self-Supervised Learning Predictor of BVDS
permalink: /portfolio/self-supervised/
header:
  overlay_image: /images/scg.jpg # Add the path to your splash image
  overlay_filter: 0.5 # Optional: Adjust the filter opacity for better title visibility
  overlay_full: true  # Makes the header full-width
  actions:
    - label: "Visit Inan Lab Website"
      url: "https://irl.gatech.edu/"
---

I'm currently a Master's student with Dr. Omer Inan's research lab, and am working on publishing my recent works using self-supervised learning methods to predict blood volume decompensation status (BVDS) in pigs. The project refers frequently to an existing paper: “Unifying the Estimation of Blood Volume Decompensation Status in a Porcine Model of Relative and Absolute Hypovolemia Via Wearable Sensing,” and the open-source code (excluding data) is on [GitHub](https://github.com/samueliu/bvds/).

Several pigs were put into various stages of BVDS, and the timeseries data from various wearable sensors were labeled and segmented, allowing for use in deep-learning models.

<div style="text-align: center;">
  <img src="/images/inanpaper.png" alt="literature" style="max-width: 75%; height: auto; border-radius: 10px;">
  <p><em>Process of feature extraction from timeseries data of different BVDS stages - Taken from previous literature</em></p>
</div>

For the initial part of the project, leave-one-out cross-validation was used on 6 pigs; 6 pig models were created, with each trained on other 5 pigs and tested on the original pig. Windows were taken for 12 features at multiple BVDS stages for each pig.

<div style="text-align: center;">
  <img src="/images/dataset.png" alt="dataset" style="max-width: 75%; height: auto; border-radius: 10px;">
  <p><em>Data cleaning process for 6 pigs used for training and cross-validation</em></p>
</div>

LSTM were the model of choice due to its temporal nature. Using the timeseries windows, forecast and backcast predictions of each feature were made by running through the autoregressor.

<div style="text-align: center;">
  <img src="/images/model1.png" alt="lstm upstream" style="max-width: 75%; height: auto; border-radius: 10px;">
  <p><em>Diagram showing LSTM autoregressor portion of model</em></p>
</div>

After training on itself (hence the self-supervised), the best performing LSTM for each pig was cut, and redirected towards a downstream regressor for BVDS. The resulting model used the information learned from the autoregressor into detecting a new feature entirely. 

<div style="text-align: center;">
  <img src="/images/model2.png" alt="lstm downstream" style="max-width: 75%; height: auto; border-radius: 10px;">
  <p><em>Diagram showing saved LSTM model redirected towards BVDS regressor</em></p>
</div>

This model was able to beat the ones found in literature using the same dataset (and a CNN model) by approximately 7%. More analysis is currently being done with different parameter tunings, datasets, and approaches (such as autoencoders, other downstream regressor ML methods, etc.). 

<div style="display: flex; justify-content: space-around; flex-wrap: wrap; text-align: center;">
  <div style="flex: 1; margin: 10px;">
    <img src="/images/results0.png" alt="drawing1" style="max-width: 100%; height: auto; border-radius: 10px;">
    <p><em>Results from 6 pigs used in literature with a CNN model</em></p>
  </div>
  <div style="flex: 1; margin: 10px;">
    <img src="/images/results1.png" alt="" style="max-width: 100%; height: auto; border-radius: 10px;">
    <p><em>Current best-performing results from LSTM as of July 2024</em></p>
  </div>
</div>



