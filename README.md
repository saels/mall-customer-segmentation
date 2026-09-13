# 🛍️ Mall Customer Segmentation with K-Means

## 💼 Business use case

Retail teams can make better marketing decisions when they understand that customers differ not only in purchasing power, but also in their observed spending behavior. This project uses customer segmentation to identify groups with similar age, income, and spending patterns that could support more focused campaigns, loyalty strategies, and re-engagement efforts.

Rather than treating the full customer base as a single audience, the analysis turns three simple customer attributes into six interpretable segments.

## 🎯 Principal objective

The objective is to use **K-Means clustering** to group 200 customers based on **Age**, **AnnualIncome**, and **SpendingScore**.

The workflow covers exploratory analysis, feature standardization, cluster selection with the elbow method, K-Means fitting, and segment profiling across several demographic and behavioral views.

The focus is not only on producing clusters, but on understanding whether the resulting groups can be translated into useful business actions.

## 🔍 Summary of takeaways

The six-cluster solution reveals several distinct customer profiles.

- Younger customers tend to show stronger spending behavior across both lower and higher income levels.
- Older customers at the income extremes tend to have lower spending scores.
- High income does not automatically translate into high spending, creating a potentially valuable re-engagement opportunity among older, affluent customers with low spending scores.
- Younger, high-income, high-spending customers stand out as a natural premium or loyalty segment.
- Younger customers with lower income but high spending may be better suited to value-oriented rewards and promotions.
- The broad customer pattern remains visible across both genders in this sample, suggesting that gender is more useful as a secondary profiling dimension than as the primary segmentation driver.

From a technical perspective, the clustering is performed on standardized features, which is important for a distance-based algorithm such as K-Means. The current six-cluster choice is based on the elbow method; a production version should also test silhouette quality, cluster stability, and performance over time.

## 🧭 Business perspective

The value of this analysis is in moving from broad demographic assumptions to customer groups that combine **capacity to spend** with **observed spending behavior**.

The segmentation can support different treatments for premium customers, reactivation candidates, highly engaged lower-income customers, and stable mid-value groups. Before deploying these segments in campaigns, the next step would be to connect them with real outcomes such as conversion, retention, visit frequency, or revenue.

## 🧪 Where I would take it next

The current dataset is intentionally compact. Adding customer tenure, transaction recency and frequency, category preferences, promotion response, digital engagement, and churn signals would make the clusters more behaviorally meaningful and easier to validate against business results.

## 💻 Explore the notebook

The [notebook](https://github.com/saels/mall-customer-segmentation/blob/d3dcfb78adafd236707a7690cce07f032f97bb35/Mall_customer_segmentation.ipynb) contains the full workflow, including the exploratory analysis, scaling logic, elbow-method evaluation, K-Means implementation, and customer-level visualizations. Check it if you want to see how the six segments were built, the visual outputs for the analysis, and where I would strengthen the modeling for a production setting.
