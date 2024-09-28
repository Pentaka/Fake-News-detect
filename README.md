# Fake-News-detect

This dataset is taken from [Kaggle](https://www.kaggle.com/datasets/mdepak/fakenewsnet).

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
We gained the following insights from EDA:

-Class Imbalance: The dataset is imbalanced between real and fake news. Methods such as SMOTE and RandomUnderSampler were used to balance this data, but it was observed that the dataset was not large enough and produced worse results than the raw data.

-Headline Lengths: The distribution of headline lengths varies significantly between real and fake news. This can be used as a feature in predictive models, but the performance drops significantly when extreme values ​​are removed.

-Source Credibility: Some news sources dominate the dataset, and some show a clear tendency to publish more fake or real news. Source credibility can be another important feature. These findings are critical for preparing the dataset for machine learning models and offer potential areas for feature engineering, such as improving classification performance using headline lengths and source credibility.

## Libraries:

```bash
pip install pandas re matplotlib seaborn scikit-learn


