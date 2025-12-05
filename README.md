# Pneumonia Classification with Uncertainty Estimation

This project is a proof-of-concept demonstrating the use of deep learning for medical image classification, with a special focus on quantifying model uncertainty using Monte Carlo Dropout.

Developed by: Ahmad Ahmad
Model Version: v3.0
Final Test Accuracy: 90%

## Project Goal

The primary goal was not just to build an accurate classifier, but to build a system that **knows when it might be wrong**. In critical applications like medicine, a model that makes a mistake but flags its own uncertainty is safer and more useful than a model that is overconfident in its errors.

## Key Features

*   **Transfer Learning:** Utilizes a pre-trained VGG16 model as a base.
*   **Uncertainty Quantification:** Implements Monte Carlo Dropout to estimate the model's confidence in its predictions.
*   **Improved Training:** Addresses data imbalance using class weights and creates a robust validation set for stable training.

## Key Findings

*   The final model achieved **90% accuracy** on the unseen test set.
*   More importantly, the model successfully reduced critical "False Negative" errors by **40%** compared to the baseline version.
*   The model demonstrates varying levels of uncertainty, correctly showing high confidence on "easy" cases and (in some instances) higher uncertainty on more ambiguous images. This highlights the importance of uncertainty estimation as a tool to identify cases that require expert human review.

## How to Run

The entire development process is documented in the `notebook.ipynb` file, which can be run in an environment like Google Colab or Kaggle.

