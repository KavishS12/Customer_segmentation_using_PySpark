# Customer Segmentation in Banking Using PySpark and K-means Clustering

## Project Overview
This project leverages PySpark and K-means clustering to perform customer segmentation on a large bank transaction dataset. By identifying distinct customer groups based on account balances, transaction amounts, gender, and location, we can inform targeted marketing and customized financial services strategies.

## Methodology
1. **Data Preprocessing**
   - Loaded `bank_transactions.csv` using PySpark with schema inference.
   - Cleaned data by handling null values and removing duplicates.
2. **Feature Engineering**
   - Categorical features (`CustGender` and `CustLocation`) indexed with `StringIndexer`.
   - Combined numerical features into a single vector using `VectorAssembler` and scaled with `StandardScaler`.
3. **Clustering**
   - Applied K-means with `k=5` to the scaled features, based on data distribution and domain insights.
4. **Visualization and Analysis**
   - Generated scatter plots to visualize clusters by account balance, transaction amount, and gender.
   - Computed cluster statistics to profile each segment.

## Results
The analysis identified five customer segments:
- **Cluster 1 (Mass Market Segment):** Large, male-dominated group with moderate balances and low transactions.
- **Cluster 3 (Affluent Segment):** Smaller, mixed-gender group with high balances and transactions, suitable for premium services.
- **Cluster 4 (High Net Worth Segment):** Exclusive group with very high balances, requiring personalized services.
- **Cluster 2 (Ultra High Net Worth Segment):** Predominantly male with extreme balances, ideal for investment banking services.
- **Cluster 0 (Female-Dominated Mass Market Segment):** Large, primarily female group with low balances, ideal for financial education products.
