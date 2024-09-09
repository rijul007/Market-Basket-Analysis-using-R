# Market Basket Analysis

## Objective
The objective of this project is to perform Market Basket Analysis using Association Rules to understand customer purchasing behavior and identify product associations.

## Dataset Used
The analysis uses a dataset containing transaction information, with each record representing a product purchased in a transaction. The dataset is stored in a CSV file named "MarketBasketAnalysis.csv" and contains two columns: "Transaction" and "Product".

## Analysis Technique
The project employs Association Rule Mining, specifically using the Apriori algorithm, to discover relationships between products in the transaction dataset. The analysis involves several key steps and tools:

1. **Data Preparation**: 
   - Utilized the **`arules`** package to read and process the transaction data.
   - Converted the CSV file into a special "transactions" class using **`read.transactions()`** function.

2. **Exploratory Data Analysis (EDA)**:
   - Performed basic EDA using **`summary()`** and **`itemFrequencyPlot()`** functions.
   - Analyzed item frequency and transaction patterns.

3. **Association Rule Mining**:
   - Applied the **Apriori algorithm** using the **`apriori()`** function from the **`arules`** package.
   - Set parameters for minimum support, confidence, and rule length.

4. **Rule Evaluation and Filtering**:
   - Analyzed rules based on support, confidence, and lift metrics.
   - Used **`inspect()`** and **`sort()`** functions to examine and rank rules.

5. **Redundancy Removal**:
   - Identified and removed redundant rules using **`is.subset()`** function.

6. **Visualization**:
   - Utilized the **`arulesViz`** package for visualizing association rules.
   - Created various plots including scatter plots, grouped matrix plots, and graph-based visualizations.

7. **Focused Analysis**:
   - Conducted a specific analysis on the most frequent item (Magazine) to understand its associations with other products.

## Results
The analysis yielded several insights into product associations:

1. Identified 49 association rules with a minimum support of 0.01 and confidence of 0.1.
2. After removing redundancy, the most significant rules were analyzed based on lift, support, and confidence.
3. Visualizations provided intuitive representations of rule strength and relationships between products.
4. Specific analysis on Magazine (the most frequent item) revealed its associations with other products.

Based on the analysis, the following product combinations are recommended for potential marketing strategies or store layouts:
- Photo Processing and Magazine
- Greeting Cards and Candy Bar
- Toothbrush and Perfume

The project demonstrates the power of **R** and its specialized packages (**`arules`** and **`arulesViz`**) in conducting sophisticated market basket analysis, providing valuable insights for retail strategy and decision-making.

For a detailed view of the analysis and visualizations, you can access the [RPub Document here](https://rpubs.com/Rijul-Grover/1218045).