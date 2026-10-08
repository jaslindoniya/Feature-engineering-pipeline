# Feature-engineering-pipeline
# Robust ML Preprocessing Pipeline

This project is about building a clean, leak-free machine learning pipeline. Many beginners do scaling and encoding before splitting the data, which causes data leakage. This project fixes that.

### What this project does?

1.  **Loads a tabular dataset** - Customer Churn dataset with numerical and categorical columns.
2.  **Prevents Data Leakage** - First we do train/test split, then only we apply transformations.
3.  **Uses ColumnTransformer** - For numbers we use StandardScaler, for categories we use One-Hot Encoding.
4.  **Finds important features** - We used Correlation heatmap and Mutual Information score to find which feature causes churn the most.

### Key Findings from my Analysis

*   `support_tickets` has 0.90 correlation with churn. If a customer raises more tickets, they will likely churn.
*   `tenure_months` has -0.83 correlation. New customers are churning more.
*   Top feature from MI Score: `plan_type_Basic` and `contract_type_Monthly`. So basic plan users with monthly contract are leaving.

### Tech Stack

*   Python, Pandas, NumPy
*   Scikit-Learn (Pipeline, ColumnTransformer, StandardScaler, OneHotEncoder)
*   Matplotlib & Seaborn for visualization

### How to run

1.  Open the `.ipynb` file in Google Colab
2.  Run all cells
3.  You will see the pipeline, heatmap and feature ranking output
