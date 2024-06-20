# Pet Store Transaction Analysis

This project aims to enhance the marketing strategies and boost sales for a pet store through detailed data analysis of transactional data. The analysis focuses on customer segmentation and personalized product recommendations using the OSEMN framework (Obtain, Scrub, Explore, Model, iNterpret).

## Objectives

1. **Product Analysis**: Determine the total number of product categories sold within each product line (cat & dog).
2. **Customer Segmentation**: Use the K-means clustering algorithm to segment customers based on their purchasing behavior.
3. **Recommendation System**: Develop a system to recommend top-selling products to customers within each segment who haven't purchased those items yet.

## Dataset Overview

The dataset includes 2,903 entries, with 10 columns capturing various aspects of transactions:
- `Date`: The date of the transaction.
- `Order_Number`: A unique identifier for each order.
- `Customer_ID`: A unique identifier for each customer.
- `Product_Name`: The name of the product purchased.
- `SKU`: The stock keeping unit for the product.
- `Price`: The price of the product.
- `Size`: The size of the product (if applicable).
- `Quantity`: The number of units purchased.
- `Product_Category`: The category of the product.
- `Product_Line`: Whether the product is for cats or dogs.

## Analysis Workflow

### OSEMN Framework

#### 1. Obtain
- **Data Acquisition**: Loading the dataset and performing an initial inspection to understand its structure and contents.

#### 2. Scrub
- **Data Cleaning**: Handling missing values, converting data types, removing duplicates, and handling outliers.
- **Data Transformation**: Creating new features such as `Total_Sales` and extracting `Month` and `Year` from the `Date` column.

#### 3. Explore
- **Descriptive Statistics**: Summarizing key statistics of the dataset.
- **Data Visualization**: Visualizing sales trends, top-selling products, and sales distribution by product line.
- **Correlation Analysis**: Analyzing correlations between numerical features.

#### 4. Model
- **K-means Clustering**: Segmenting customers based on their purchasing behavior using features like `Total_Spend`, `Total_Transactions`, and `Total_Products_Purchased`.
- **Cluster Analysis**: Interpreting the resulting customer segments to understand distinct profiles and preferences.
- **Product Recommendations**: Developing a system to recommend top-selling products to customers within each segment who haven't purchased those items yet.

#### 5. iNterpret
- **Insights and Recommendations**: Summarizing findings and providing actionable recommendations for enhancing marketing strategies and boosting sales.

## Key Findings

### Customer Segmentation
- **Cluster 0: High Spenders**: Highest total spend and frequent transactions.
- **Cluster 1: Moderate Spenders**: Balanced purchasing behavior.
- **Cluster 2: Low Spenders**: Lowest engagement and spending.

### Product Recommendations
- Personalized recommendations to increase the likelihood of additional purchases.

### Marketing Strategies
- **Customer Retention**: Implement loyalty programs.
- **Customer Engagement**: Use targeted promotional campaigns.
- **Cross-Selling and Up-Selling**: Highlight complementary products.

## Conclusion

This analysis provides actionable insights to enhance marketing strategies and sales performance. By understanding customer behavior, the pet store can tailor its approach to meet customer needs, driving satisfaction and revenue growth.

## Future Work

Further analysis could involve:
- Exploring seasonal trends in sales.
- Evaluating the effectiveness of marketing campaigns.
- Refining the recommendation system based on customer feedback.

## Final Note

While this analysis addresses the primary objectives, it can certainly go deeper. Each insight uncovered raises new questions and opportunities for further exploration. For now, this analysis remains within the defined scope, delivering clear and actionable insights for enhancing the pet store's marketing efforts and customer engagement.

## Project Structure

- `data/`: Contains the dataset used for the analysis.
- `notebooks/`: Jupyter notebooks with the detailed analysis.
- `src/`: Source code for data processing, analysis, and modeling.
- `README.md`: This document.

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/micfaj/pet-store-analysis.git
   cd pet-store-analysis
   pip install -r requirements.txt
   jupyter notebook notebooks/
