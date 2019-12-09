### Probability of Loan Default

Lending club is an online peer to peer lending platform. Peer to peer lending cuts out banks and institutions as the middleman between the lender and borrower. Lower interest rate, reasonable repayment terms and joint application options make Lending Club an attractive option for credit borrowers and debt consolidation seekers. Through their website individuals or initiations can apply to become borrowers or lenders. Lending Club publishes a quarterly loan report, open source, on their website.

Due to githubs file size maximum being 25MB, I was unable to add the data to this repository. It can be easily accessed through Lending Clubs website https://www.lendingclub.com/.

### Data Description Summary

Each quartlerly report contained 150 columns and ~100,000 rows of data.

Loan Status - Current, Fully Paid, In Grace Period, Late, Charged Off, Default Loan Properties - Amount, Length, Interest Rate, Month Issued, Description provided by the borrowers, etc. Borrower Data - Income, Home Ownership Status, Occupation, Employment Length, etc. Credit Risk Metrics - Metrics used to measure the risk of the loan, such as, fico score, bank card utilization, current balances on accounts, etc.

For more descriptions check out LCDataDictionary.csv

file:///Users/alicjaligas/Desktop/Screen%20Shot%202019-12-08%20at%2010.17.27%20PM.png

### Unbalanced Classes

Quarterly, less than 1% of all loans resulted in default. This caused a marjor class inbalance of the target variable. Attempting to train a model that would predict above the baseline was a major challange. I tried two techniques to deal with the class inbalance. The first was undersampling with the majority class. The second was SMOTE. SMOTE helps underbalanced classes by generating synthetic samples similar to the target class. Such as with K nearest neighbors, SMOTE uses distance to find data points closest to the target and learns form its features. It then generates data points that have properties of both the target data and the majority class.

The class inbalance also made it difficult to identify features that were strongly correlated to the target. Using Random Forest Feature Selection I was able to identify the columns that reduced the gini impurity the most. Even then the most valuable feature only reduced the gini impurity by 6%.

### Going Forward

Continuing forward I will explore better and more robust ways to deal with unbalanced classes and continue to try different modeling techniques.
