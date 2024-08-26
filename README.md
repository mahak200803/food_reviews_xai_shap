## Study Overview

This study explores the effectiveness of Long Short-Term Memory (LSTM) and Bidirectional LSTM (Bi-LSTM) models for sentiment analysis of customer reviews related to food delivery services. The primary goal is to evaluate which model provides more accurate sentiment classification—positive, negative, or neutral—using the F1 score metric.

### Objectives

1. **Model Accuracy**: Compare LSTM and Bi-LSTM models to determine which one achieves higher accuracy in classifying customer review sentiments in the food delivery industry.
   
2. **Model Transparency**: Apply SHAP (SHapley Additive exPlanations) to the selected model to gain insights into its decision-making process. SHAP will help explain how the model assigns sentiment labels to reviews and highlight the importance of various features (such as word sentiment and delivery speed) in its predictions.

3. **Feature Importance**: Assess the significance of different attributes within the reviews to understand which factors most influence sentiment classification.

### Goals

- **Enhanced Accuracy**: Identify the deep learning model that provides the best performance in sentiment analysis for customer reviews in the food delivery sector.

- **Model Transparency**: Use SHAP to shed light on how the chosen model processes review data and assigns sentiment labels, making its decision-making process more understandable.

- **Feature Importance**: Evaluate the relative importance of various features in the reviews to gain insights into the aspects that most affect customer sentiment.

### Contribution

This research advances the field of sentiment analysis by demonstrating the effectiveness of deep learning models for analyzing customer reviews in the food delivery domain. By integrating SHAP for interpretability, the study enhances model transparency, builds trust in its predictions, and offers actionable insights for food delivery service providers to improve customer satisfaction.

## What is SHAP?

In the field of machine learning, models can generate sophisticated predictions through complex computations and relationships. However, a major trade-off with these advanced models is their interpretability. These "black-box models" excel at making predictions but often lack transparency in their decision-making processes. This opacity makes it challenging to understand why specific predictions are made, raising concerns about potential biases and errors. To address this issue, techniques like SHAP (SHapley Additive exPlanations) have been developed. SHAP provides insights into the inner workings of these models by attributing feature contributions and explaining how each piece of data influences the final prediction. This increased transparency fosters trust in the model's decisions, helps identify the factors driving predictions, and ensures responsible application of machine learning.

## SHAP for Interpretability

Originating from game theory, SHAP values help us decode the complexities of a model by assigning feature attribution scores to each input feature for a given prediction. Think of each feature as a player in a team competition, where the model's prediction represents the outcome. SHAP calculates each player's contribution to the overall result by considering all possible combinations of features. This approach reveals not only the individual impact of each feature but also how features interact with one another, providing a comprehensive view of their collective influence. SHAP values thus represent the average impact of each feature on predictions across various scenarios, and they also allow us to explore potential correlations between features. Being model-agnostic, SHAP can be applied to a wide range of models, from simple linear regressions to complex deep neural networks, making it a versatile tool for interpreting different machine learning applications.

## SHAP Applications

SHAP values offer valuable insights into the global significance of features within a model. By averaging SHAP values across all predictions, we can assess the overall contribution of each feature to the model's output. SHAP summary plots visualize these values, showing which features are most influential. These plots are akin to bar charts, where each bar represents the average impact of a feature, with positive values indicating a push towards a particular prediction and negative values indicating a pull away from it. This high-level analysis helps identify the most important features driving the model’s decisions.

SHAP also enables a deeper understanding of individual predictions. Techniques like SHAP force plots and waterfall plots are crucial for this purpose. Force plots visually represent how each feature shifts the base prediction (the average prediction) towards the final outcome, with features arranged sequentially to show their cumulative effect. Waterfall plots illustrate the combined effect of features, detailing how they collectively influence the prediction away from the base. By examining these visualizations, we can pinpoint the specific features that significantly impact a given prediction, offering detailed insights into the model’s reasoning process.
