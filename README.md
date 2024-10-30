# Customer-Segmentation
# PROJECT DESCRIPTION

This project involved segmenting supermarket customers based on demographics and spending behavior to identify key customer groups for targeted marketing.

# TECHNOLOGIES USED

- Python (Pandas, Matplotlib, Scikit-Learn, Seaborn)
- PowerBI
- SQL
- Excel

# METHODOLOGY

### **Step 1: Data Loading**

- **Code:** We used `pd.read_csv()` from the `pandas` library to load the customer data file into a DataFrame.
- **Explanation:** Loading data is the initial step in any data project. It allows us to bring the raw data into our environment to examine it and prepare it for analysis.

### **Step 2: Data Exploration**

- **Code:** We used `.head()`, `.info()`, and `.describe()` functions from `pandas` to inspect the dataset.
- **Explanation:** Data exploration helps in understanding the data structure, identifying data types, and getting a sense of basic statistics like mean, min, max, etc. This step is critical for gaining initial insights and spotting any issues in the data.

### **Step 3: Data Cleaning**

- **Code:** We checked for missing values with `isnull().sum()` and handled them accordingly if any were present.
- **Explanation:** Data cleaning ensures that the dataset is free from errors or inconsistencies. Handling missing or incorrect values is essential to avoid skewing the results during analysis.

### **Step 4: Feature Selection**

- **Code:** We chose relevant features such as **Customer ID**, **Age**, **Annual Income**, and **Spending Score**.
- **Explanation:** Selecting the right features is key to improving model performance. For customer segmentation, we focused on features directly impacting customer behavior, such as spending and income.

### **Step 5: Data Preprocessing (Standardization)**

- **Code:** We used `StandardScaler` from `sklearn. preprocessing` to scale features so they have a mean of 0 and a standard deviation of 1.
- **Explanation:** Standardizing data is crucial for algorithms like k-means, which are sensitive to the scale of the data. Standardization puts all features on a comparable scale, ensuring that one variable doesn’t disproportionately influence the model.

### **Step 6: K-Means Clustering**

- **Code:** We applied the `KMeans` algorithm from `sklearn.cluster`, specifying the number of clusters.
- **Explanation:** K-means is an unsupervised learning algorithm used for clustering similar data points together. We specified the number of clusters based on the Elbow Method, which involved plotting the sum of squared distances and identifying the "elbow" point where adding more clusters didn’t significantly reduce this sum.

### **Step 7: Evaluation and Insights**

- **Code:** We analyzed the clustering results by visualizing the clusters with `Matplotlib` and `Seaborn`.
- **Explanation:** Visualization helps in understanding the characteristics of each cluster. We plotted clusters in terms of annual income vs. spending score, identifying distinct customer groups such as high-spending and low-spending segments.

### **Step 8: Final Results and Interpretation**

- **Code:** We used plots to interpret each customer segment and documented insights on each group’s characteristics.
- **Explanation:** This final step involves summarizing insights. For instance, high-income and high-spending groups may represent valuable customers for targeted marketing. These insights can guide business strategies tailored to each segment.

# KEY INSIGHTS
### **Gender and Spending Behavior**:

- The **Average Spending Score by Gender** shows that **females (51.53)** have a slightly higher spending score than **males (48.51)**, suggesting that women may be slightly more engaged or have higher purchasing power in this dataset.
- **Gender Distribution** in the pie chart indicates that **56% of the customer base is female** while **44% is male**.

### **Age and Spending Trends**:

- The **Average Spending Score per Age** line chart reveals spending peaks in specific age groups, notably around ages 25-30 and 35-40. This suggests that younger and mid-age customers tend to spend more, which could guide age-targeted marketing strategies.
- **The Average Age per Gender** bar chart highlights that the average ages are above 30 for both genders but with a slightly younger average age for females.

### **Income and Spending Correlation**:

- The **Average Spending Score per Annual Income** area chart shows a spending peak around **$60k-$70k annual income**. Spending decreases significantly beyond **$100k**, indicating that high-income earners might be less price-sensitive or have different shopping preferences.

Overall, this dashboard provides valuable insights into demographic and behavioral factors that impact customer spending in this supermarket. These findings can help the business develop targeted campaigns that cater to specific age groups, income levels, and genders, enhancing engagement and maximizing revenue.
