# Capstone Project: Analyzing the 2025 Electric Vehicle Charging Experience with IBM Granite

## Project Overview
This project aims to analyze the state of the Electric Vehicle (EV) charging infrastructure as we head into 2025. Using a public dataset of user reviews for EV charging stations across the United States, we leverage the IBM Granite AI model to perform sentiment classification, thematic summarization, and trend analysis. The goal is to uncover key drivers of user satisfaction and frustration, identify common hardware and software issues, and provide actionable recommendations for network operators and policymakers to improve the EV charging experience.

## Raw Dataset Link
The analysis uses the "Electric Vehicle Charging Station Usage" dataset, which contains real user comments and ratings for various charging networks. We treat this recent and extensive dataset as a proxy for the 2025 user experience.

-   **Dataset Source (Kaggle):** [Electric Vehicle Charging Station Usage](https://www.kaggle.com/datasets/koustavghosh17/electric-vehicle-charging-station-usage)
-   **Direct Raw File URL:** [https://raw.githubusercontent.com/koustavghosh170/EV-Charging-Station-Usage-Analysis/main/Electric%20Vehicle%20Charging%20Station%20Usage.csv](https://raw.githubusercontent.com/koustavghosh170/EV-Charging-Station-Usage-Analysis/main/Electric%20Vehicle%20Charging%20Station%20Usage.csv)

## Insight & Findings
1.  **Sentiment is Highly Polarized:** A significant portion of user feedback is negative (ratings of 1 or 2 stars), primarily driven by non-functional or "broken" chargers. This highlights a critical reliability issue in the current infrastructure.
2.  **Key Frustration Point - Broken Chargers:** The most dominant theme across negative reviews is equipment failure. Users frequently arrive at stations only to find them out of service, causing significant delays and frustration.
3.  **Positive Experience Drivers:** When stations work, users praise **charging speed** and **ease of use** (e.g., seamless app integration, simple payment). These are the key features that define a positive experience.
4.  **Network-Specific Issues:** AI analysis reveals that certain charging networks are more frequently associated with specific problems (e.g., payment system failures, slow charging speeds), suggesting inconsistent quality across providers.

## AI Support Explanation
This project utilizes the **IBM Granite (`ibm-granite/granite-3.0-8b-instruct`)** model through the Replicate API to perform advanced NLP tasks:

1.  **Sentiment Classification:** The AI model analyzes user comments to classify them as "Positive," "Negative," or "Neutral." It also extracts the core reason for the sentiment (e.g., "Broken Charger," "Fast Speed," "Payment Issue").
2.  **Thematic Summarization:** For detailed user comments, the AI generates a concise summary that captures the essential points of the user's experience, making it easier to understand complex feedback at a glance.
3.  **Trend Analysis & Root Cause Identification:** By analyzing a collection of reviews, the AI identifies recurring positive and negative themes. It is prompted to act as a data analyst to pinpoint root causes (e.g., "Hardware Reliability Issues") and suggest actionable improvements.
