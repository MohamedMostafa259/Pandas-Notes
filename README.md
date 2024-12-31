# Pandas Learning Notes

Welcome to my Pandas Learning Notes repository! 🌟

My learning notes of the Pandas package, covering a wide range of Pandas concepts and techniques such as data manipulation, cleaning, joining, visualization, and many other topics with Pandas.

## Contents

Feel free to explore the notebooks, which cover a wide range of Pandas topics, including:

00. Indexing and Slicing

    This notebook explores fundamental concepts of indexing and slicing in Pandas, including setting index columns during DataFrame creation, copying DataFrames for safe modifications, and accessing data using various methods (`[]`, `.loc[]`, `.iloc[]`, `.at[]`, `.iat[]`, `.get()`). It highlights the advantages of label-based (`loc`) and position-based (`iloc`) access over standard square bracket access for more flexible and intuitive data selection. The notebook also introduces handling MultiIndex DataFrames using `loc`, `iloc`, and `xs` methods, with practical examples to demonstrate efficient data manipulation.

01. Filtering and Iterating Over DataFrames

    This notebook explores key techniques for filtering and iterating over Pandas DataFrames. It demonstrates filtering using conditional expressions, logical operators, and the `isin()` method for categorical variables. It also covers iterating over DataFrame rows using `.iterrows()`.

02. Adding and Dropping Columns in DataFrames

    This notebook explains techniques for adding new columns to a Pandas DataFrame using three approaches: traditional for-loops, list comprehensions, and efficient vectorized operations like `.apply()` and `.map()`. It also demonstrates how to drop columns using the `.drop()` method and manage specific values within columns effectively, ensuring streamlined DataFrame manipulation.

03. Handling Duplicates in DataFrames

    This notebook demonstrates how to identify, handle, and remove duplicate rows in a Pandas DataFrame. It covers methods like `.duplicated()` to locate duplicates and `.drop_duplicates()` to remove them based on specified criteria. Additionally, it explores techniques for aggregating duplicated rows using `groupby()` and `agg()` to compute summary statistics.

04. Counting   

    This notebook focuses on counting unique values and their proportions in a Pandas DataFrame using the `.value_counts()` method. It compares the performance of counting methods applied to DataFrames and Series, highlighting efficiency improvements. By utilizing the `%timeit` magic command, it demonstrates that working directly with Series is typically faster, offering practical insights for optimizing data manipulation tasks.

05. Some Methods and Attributes

    - Inspecting DataFrames using `.head()`, `.info()`, and `.describe()`.  
    - Accessing data with `.values`, `.columns`, and `.index`.  
    - Viewing numerical and non-numerical columns using `select_dtypes()`.  
    - Counting unique values and calculating percentage changes with `.unique()`, `.nunique()`, and `.pct_change()`.  

06. Sorting   

    This notebook demonstrates how to sort data in a DataFrame using Pandas. It covers sorting by values with single or multiple columns, applying ascending or descending order, and sorting the index for better organization and analysis of the data.

07. DateTime Handling in Python and Pandas

    A comprehensive guide demonstrating datetime manipulation in Python and Pandas, covering datetime objects, timezone handling, and time series analysis. Features practical examples of:

    -   Basic datetime operations and conversions
    -   Timezone management and DST handling using dateutil
    -   Time series analysis with Pandas (resampling, grouping by time)
    -   Real-world applications like sales analysis and ride duration calculations
    -   Best practices for cross-timezone data processing

08. Summary Statistics / GroupBy / Pivot Tables  

    This notebook explores different methods for calculating summary statistics using Pandas. It covers single, multiple, and cumulative summary statistics, as well as grouped and pivot table statistics. It demonstrates how to compute mean, median, standard deviation, and quartiles, along with how to apply functions like `groupby`, `agg`, and `pivot_table` for more advanced summarization. Additionally, the notebook shows how to compare the performance of `groupby` versus `pivot_table` for large datasets.

09. Manipulating DataFrame Indices 

    This notebook demonstrates various methods of handling indices in a Pandas DataFrame, including setting, resetting, dropping, and working with multi-level indices. It also covers sorting by index values and slicing by both row and column labels. Additionally, it shows how to slice data based on specific time ranges and levels of a hierarchical index.

10. Visualizing DataFrames

    This notebook demonstrates various techniques to visualize avocado sales data using Matplotlib. It includes examples of histograms, bar plots, line plots, scatter plots, and layering plots. The visualizations help in understanding the distribution of variables, trends over time, and relationships between numerical variables in the dataset.

11. Handling Missing Values 

    This notebook demonstrates how to handle missing values (NaN) in a dataset using the Gapminder dataset. It covers detecting, counting, and visualizing missing values, as well as techniques for dealing with missing data, such as removing or replacing missing values. The notebook also includes an explanation of different types of missingness (MCAR, MAR, MNAR) and an example of imputing missing values based on a group (e.g., median GDP per capita by continent).

12.  DataFrame Creation / Renaming Columns / Exporting a DataFrame to a CSV file

    This notebook covers the basics of creating pandas DataFrames from a list of dictionaries or a dictionary of lists. It also demonstrates how to add new columns, save the DataFrame to a CSV file, and rename columns using both the `columns` attribute and the `rename()` method.

13. Joining DataFrames

    This notebook is about merging DataFrames in Pandas. It covers different techniques including inner join, left join, right join, outer join, cross join, self join, filtering joins (semi join and anti join), concatenating DataFrames, verifying the integrity of data during merging and concatenating, using `merge_ordered()` for ordered or time-series data, forward filling missing values, using `merge_asof()` for time series data with uneven sampling or time-series training sets.

14. Selecting Data with `.query()` Method

    This notebook demonstrates how to use the `.query()` method to filter rows in a pandas DataFrame based on conditions. It shows how to apply single and multiple conditions, as well as using `.query()` with datetime attributes for more complex filters.

15. Reshaping Data with `.melt()` Method (Converting Wide Format to Long Format)

    This notebook demonstrates how to reshape data from wide format to long format using pandas' `.melt()` method. It showcases examples such as reshaping a sales dataset and government data for plotting, specifically US unemployment rates. The notebook also highlights the importance of the `.melt()` method for converting data into a machine-readable format and provides performance comparisons for different querying methods.

16. Analyzing Categorical Data

    This notebook demonstrates how to handle and analyze categorical data with pandas. It covers:
    - Updating data types using `.astype()` to convert columns to the appropriate types.
    - Analyzing categorical data by using `.str.contains()` to filter specific patterns in job titles, and then grouping similar roles into categories using `np.select()` to create a new "Job_Category" column.
    - Visualizing the distribution of job categories with `sns.countplot()`.
    - Converting non-numeric string values (like salary data with commas) into numeric format for further analysis.

17. Handling Outliers

    This notebook demonstrates how to detect and handle outliers in a dataset using pandas. It covers:
    1. Identifying outliers using the Interquartile Range (IQR) method by calculating the lower and upper bounds based on Q1 (25th percentile) and Q3 (75th percentile).
    2. Visualizing the impact of outliers by plotting histograms of the salary distribution with and without outliers.
    3. Discussing the importance of understanding and addressing outliers in data, particularly for statistical analysis and machine learning models, and highlighting the need to decide whether to remove or retain outliers based on their cause and relevance.

18. Exploratory Data Analysis (EDA) on Class Imbalance

    Key steps and concepts:

    1. **Class Imbalance**: This occurs when one class is significantly more frequent than others, which can bias results, especially in predictive modeling.
    - We used `value_counts()` to count the frequency of different destinations in the `planes` dataset and `value_counts(normalize=True)` to get relative frequencies, showing that some destinations, like Delhi, represent only a small portion of the total flights.
    
    2. **Cross-tabulation (`pd.crosstab`)**: This method allows us to examine the frequency of combinations of classes. By using `pd.crosstab()`, we analyzed the most frequent routes, discovering that the Delhi to Cochin route had the highest frequency of flights.
    
    3. **Aggregating Data**: We also demonstrated how to aggregate values using `pd.crosstab()` with the `values` and `aggfunc` arguments, calculating the median price for flights between various source and destination pairs.

    This EDA step helps understand the distribution and relationships in the data, particularly the representation of different categories and destinations, to identify potential bias or areas for further analysis.

19. Feature Engineering 

    This section explores the process of **feature engineering**, which involves generating new features from existing data to improve the detection of relationships and enhance the performance of machine learning models.

    - Converted to datetime format to extract useful features.
    - Plotted a heatmap to visualize correlations between numerical variables before and after adding new features.
    - extracted categorical feature from a numerical column: Divided the `Price` column into categories (e.g., "Economy", "Premium Economy") using custom bins based on percentiles of the price distribution.

20. Categorical Data Type 

    This code demonstrates using pandas' `category` dtype to store categorical data more efficiently. It shows how to:

    - Convert string columns to categorical data for memory savings.
    - Set, rename, and reorder categories.
    - Add or remove categories as needed.
    - Clean data (e.g., fix capitalization or misspellings).
    - Filter categorical data using string methods.

21. Uniformity Problems

    -   handled data containing different currencies (e.g., EUR and USD).
    -   handled data containing  dates in different formats (e.g., `26-11-2019` vs. `26, November, 2019`).
    -   handled data containing ambiguous dates like `"2019-03-08"` (March or August?).
    
22. Comparing String Similarities

    This notebook demonstrates how to use string similarity techniques for tasks like comparing strings, handling typos, and record linkage. It explains the concept of minimum edit distance and explores algorithms like Levenshtein using the `thefuzz` package. The notebook also shows how to collapse similar categories in a dataset, e.g., standardizing cuisine types with typos, and performs record linkage to merge datasets with fuzzy matching.

23. Encoding

    This notebook covers encoding techniques for categorical data:

    -   Label Encoding: Converts categories to integers, but can mislead models by implying ordinality.
    -   Boolean Encoding: Creates binary columns for specific categories (e.g., "van").
    -   One-hot Encoding: Converts categories into separate binary columns to avoid ordinal relationships.

24. Cross-field Validation

    This notebook checks data integrity by comparing multiple fields in a dataset. It focuses on identifying inconsistencies, such as mismatched investment amounts and ages.

## Contributing

If you find these notes helpful, please consider giving this repository a star ⭐! Your support motivates me to keep improving and expanding the content.  

Have ideas for enhancing the materials or spotting any mistakes? Pull requests are welcome! 🛠️ Let’s collaborate to make this resource even better.  

## Feedback

If you have any suggestions, questions, or feedback, feel free to open an issue or contact me directly.

Happy learning! 🚀
