# Instagram-Engagement-Analytics-NLP
End-to-end data analytics project using NLP, Topic Modeling (LDA), and Regression Analysis in R to uncover the drivers of Instagram engagement for a travel lifestyle brand.

# 📱 Influencer Engagement Analytics & Optimization

## 📊 Project Overview
This project applies advanced data analytics to deconstruct what truly drives user engagement (likes and comments) on Instagram. By analyzing 250 posts across 5 major travel influencers, this study develops a data-driven content strategy for **ROAM**, a solid perfume brand targeting digital nomads and travelers.

The analysis challenges conventional social media wisdom, proving that authenticity and visual quality significantly outperform traditional "algorithm-hacking" tactics like hashtag stuffing.

## 🛠️ Methodological Workflow
The end-to-end pipeline was built in **R**, leveraging text and image data:

1. **Natural Language Processing (NLP)**: 
   * Tokenization and text cleaning using `tidytext`.
   * **Sentiment Analysis** applying multiple lexicons (AFINN, Bing, NRC) to quantify the emotional tone of captions.
2. **Topic Modeling**:
   * Implemented **Latent Dirichlet Allocation (LDA)** to cluster captions into 5 distinct latent themes (e.g., "Digital Nomad Lifestyle", "Van Life", "Outdoor Hiking").
3. **Computer Vision / Image Feature Extraction**:
   * Analyzed pre-extracted visual features including Brightness, Saturation, and Object Detection (e.g., presence of a person in the frame).
4. **Statistical Modeling**:
   * Built multivariable **Linear Regression models** (on log-transformed engagement metrics) to quantify the exact impact of visual and textual features on Likes and Comments. Tested for non-linear and interaction effects.

## 🚀 Key Data Science Insights
* **Visuals Do the Heavy Lifting**: Image Brightness ($\beta = +1.17$) and Saturation ($\beta = +0.79$) strongly drive likes. 
Human presence in the frame increases likes by **2.76x**. [cite: 4159, 4160]
  **Hashtags Kill Conversation**: Counterintuitively, every additional hashtag significantly *reduces* comment engagement ($\beta = -0.163$), acting as a signal of low authenticity. [cite: 4226, 4322]
  **The "Digital Nomad" Premium**: LDA Topic Modeling revealed that posts clustered around the "Digital Nomad / Laptop Lifestyle" topic drove significantly more likes ($\beta = +5.58$) compared to pure "Outdoor Adventure" content, identifying a clear content gap. [cite: 4247, 4260]
**Authenticity > Positivity**: Overtly positive sentiment (AFINN) and question marks in captions actively hurt engagement, suggesting audiences reward raw storytelling over curated ad copy. [cite: 4312, 4335]

## 💡 Strategic Recommendations
Based on the regression outputs, the influencer playbook was optimized to:
1. Prioritize bright, high-saturation outdoor imagery with the influencer always in-frame.
2. Eliminate engagement-bait (questions) and restrict hashtags to a maximum of two.
3. Pivot content themes towards the aspirational "work-travel" lifestyle to maximize reach.

## 💻 Tech Stack
* **Language**: R
* **Key Libraries**: `tidyverse`, `tidytext`, `topicmodels` (LDA), `SnowballC` (Stemming), `ggplot2`, `janitor`
