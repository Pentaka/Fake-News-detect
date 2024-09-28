# Fake-News-detect
 
## Exploratory Data Analysis (EDA) for Fake News Detection
In this section, we conduct a thorough Exploratory Data Analysis (EDA) of the dataset used to detect fake news. This analysis aims to provide insights into the characteristics of the data, which is crucial for feature engineering, model building, and understanding the overall distribution of the news articles. Below, we summarize key findings from the visualizations generated.

## 1. Distribution of Real and Fake News
The first plot shows the distribution of real and fake news articles in the dataset. This is represented as a bar plot, with:

<img src="https://github.com/Pentaka/Fake-News-detect/blob/main/EDA1.png">

-Real news (denoted by 1)
-Fake news (denoted by 0)
This plot gives a quick overview of whether there is a class imbalance in the dataset, which is important for model performance.

Observation: Any significant imbalance could necessitate handling techniques like oversampling/undersampling or adjusting evaluation metrics.


## 2. Distribution of Title Lengths
Here, we visualize the distribution of the number of characters in news article titles using a histogram with a kernel density estimate (KDE). This reveals how the length of titles varies across the dataset.

<img src="https://github.com/Pentaka/Fake-News-detect/blob/main/EDA2.png">

Observation: The majority of titles are within a moderate character range. There are some titles exceeding 150 characters, which may be outliers.


## 3. Most Frequent News Sources
This bar plot illustrates the top 10 most frequent news sources in the dataset. Understanding which sources contribute the most articles is crucial since some sources may be more prone to publishing fake news.

<img src="https://github.com/Pentaka/Fake-News-detect/blob/main/EDA3.png">

Observation: Some sources appear disproportionately often. These sources could potentially bias the dataset if they focus on either real or fake news.


## 4. Title Lengths: Real vs Fake News
A boxplot is used to compare the title lengths between real and fake news articles. This helps identify whether title length could be a useful feature for distinguishing between real and fake news.

<img src="https://github.com/Pentaka/Fake-News-detect/blob/main/EDA4.png">

Observation: There is a noticeable difference in the distribution of title lengths between real and fake news, suggesting that this could serve as a predictive feature.


## 5. Distribution of Real and Fake News by Most Frequent Sources
This count plot visualizes the breakdown of real and fake news articles among the top 5 most frequent news sources. This can help identify patterns regarding which sources tend to publish more fake or real news.

<img src="https://github.com/Pentaka/Fake-News-detect/blob/main/EDA5.png">

Observation: Certain sources lean more heavily toward publishing fake news, while others focus primarily on real news. These patterns could provide insight into the reliability of these sources.


## Summary
From the EDA, we gained the following insights:

-Class Imbalance: If the dataset is imbalanced between real and fake news, we will need to address this to avoid biased model predictions.
-Title Lengths: The distribution of title lengths varies significantly between real and fake news. This can be used as a feature in predictive models.
-Source Credibility: Certain news sources dominate the dataset, and some exhibit a clear tendency to publish more fake or real news. Source reliability could be another key feature.
-These findings are critical for preparing the dataset for machine learning models, and they offer potential areas for feature engineering, such as leveraging title lengths and source credibility to improve classification performance.
