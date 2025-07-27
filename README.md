Name: Shyam Nath
Course Title:Advanced Big Data and Data Mining (MSCS-634-M40)
Lab 6: Association Rule Mining with Apriori and FP-Growth 

 Purpose  
The purpose of this lab is to explore association rule mining techniques using the Apriori and FP-Growth algorithms. By analyzing real-world transactional data (the Online Retail dataset), we aim to uncover frequent itemsets and meaningful association rules that reveal hidden patterns in customer purchasing behavior.

Key Insights  
- The most frequently purchased items were generic products like `WHITE HANGING HEART`, `REGENCY CAKESTAND`, and `JUMBO BAG RED RETROSPOT`.
- Frequent itemsets revealed consistent groupings of small homeware and gift items commonly bought together.
- Association rules with high confidence and lift suggested strong relationships between specific product pairs.
- For example, customers who purchased `JUMBO BAG RED RETROSPOT` often also purchased other similarly themed tote bags or household decor items.
- The scatter plots of confidence vs. lift helped visualize which rules offered the most valuable associations.

Algorithms Compared  
- Apriori: Easy to understand and configure but slower on large datasets due to candidate generation.
- FP-Growth: More efficient in terms of runtime and memory usage, especially with higher support thresholds.

Challenges & Decisions  
- The original dataset contained cancelled transactions and missing values, which had to be cleaned.
- Performance issues with Apriori on larger subsets prompted the use of support threshold tuning.
- Warnings were encountered regarding data types:
  - The use of `.applymap()` raised deprecation warnings; this was replaced with a vectorized boolean transformation.
  - `mlxtend` also warned about passing integer values instead of boolean values; this was corrected by using a boolean mask (`basket > 0`).
- OpenPyXL had to be installed to read the Excel file format.

Files in this Repository  
- `Association_Mining_Lab_6.ipynb`: The complete Jupyter notebook with code, visualizations, and outputs.
- `Online Retail.xlsx`: The dataset used (ensure it’s in the same directory or excluded in `.gitignore` for large file size).
- `README.md`: This file describing the project, methodology, and outcomes.


Feel free to clone or fork the repository and run the notebook in JupyterLab or Google Colab.

