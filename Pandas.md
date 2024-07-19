# Important Functions in Pandas

1. **astype()**:
The `astype()` method in pandas is used to change the data type of a DataFrame column. For
example, converting a column from `int` to `float`.
   
2. **pd.concat([df1, df2])**:
The `pd.concat()` function is used to concatenate two or more DataFrames along a particular axis
(rows or columns).
   
3. **Making a new DataFrame**:
To create a new DataFrame column, you can simply assign a list or series to `df['name']`. This
will create or replace a column named `'name'` in the DataFrame.
   
4. **Create DataFrame from list**:
`def createDataframe(student_data: List[List[int]]) -> pd.DataFrame:
df = pd.DataFrame(student_data, columns=['student_id','age'])`
This function creates a DataFrame from a list of lists, with columns 'student_id' and 'age'.
   
5. **df.drop_duplicates(subset="column")**:
The `drop_duplicates()` method removes duplicate rows from the DataFrame based on the 'email'
column, keeping only the first occurrence.

6. **df.dropna()**:
The `dropna()` method removes rows from the DataFrame where the 'name' column has `NaN` (Not a Number) values.

7. **df['column'].fillna(0)**:
The `fillna()` method replaces `NaN` values in the 'quantity' column with `0`.

8. **df.shape()**:
The `shape` attribute returns a tuple representing the dimensions of the DataFrame (number of rows, number of columns).

9. **pd.melt**:
`df_melt = pd.melt(report, id_vars=['product'], value_vars=['quarter_1', 'quarter_2', 'quarter_3', 'quarter_4'],
    var_name='quarter', value_name='sales')`
The `pd.melt()` function unpivots a DataFrame from wide format to long format, making it easier to analyze.
  
10. **Method Chaining**:
`result_df = df[df['weight'] > 100].sort_values(by='weight', ascending=False)[['name']]`
Method chaining allows combining multiple pandas operations in a single, readable line of code.

11. **df.pivot()**:
`df_pivot = weather.pivot(index='month', columns='city', values='temperature')`
The `pivot()` method reshapes the DataFrame by setting the 'month' as the index, 'city' as columns, and 'temperature' as values.

12. **df.rename()**:
`new_column_names = {
    'id' : 'student_id',
    'first' : 'first_name',
    'last' : 'last_name',
    'age' : 'age_in_years'
}
students = students.rename(columns = new_column_names)`

The `rename()` method changes the column names of the DataFrame based on a dictionary of new names.

13. **df.loc** and **df.iloc**:
`df.loc` is used for label-based indexing to select rows and columns by labels, while `df.iloc` is used for position-based indexing to select rows and columns by their integer positions.

14. **.groupby()**:
The `groupby()` function is used to split the DataFrame into groups based on some criteria, and then apply a function to each group independently. For example, `actor_director.groupby(['actor_id', 'director_id']).size().reset_index(name='count')` groups by actor_id and director_id and counts the size of each group.

15. **.rename()**:
The `rename()` method allows you to change the labels of the rows or columns in a DataFrame. It takes a dictionary where the keys are the current names and the values are the new names.

16. **.sort_values(by='column_name', ascending=True)**:
The `sort_values()` method sorts a DataFrame by the values of one or more columns. Setting `ascending=True` sorts the data in ascending order.

17. **big_countries_df = world[(world['area'] >= 3000000) | (world['population'] >= 25000000)]**:
The `|` operator is used to perform an element-wise logical OR operation between two conditions. This filters the DataFrame to include rows where either condition is True.

18. **[['column_name']] (why two brackets)**:
Using double brackets `[['column_name']]` returns a DataFrame with a single column, whereas single brackets `['column_name']` return a Series.

19. **for loop in Python**:
A `for` loop in Python is used to iterate over a sequence (like a list, tuple, dictionary, set, or string) and execute a block of code for each element.

20. **.reset_index()**:
The `reset_index()` method resets the index of a DataFrame, converting the index into a column and creating a default integer index.

21. **How to perform left and right join in Python using pd.merge()**:
The `pd.merge()` function combines two DataFrames based on a key. Using `how='left'` performs a left join, including all rows from the left DataFrame and matching rows from the right. Using `how='right'` performs a right join, including all rows from the right DataFrame and matching rows from the left.

22. **.agg()**:
The `agg()` method allows you to apply multiple aggregation functions to a group of columns in a DataFrame. For example, `grouped = daily_sales.groupby(['date_id', 'make_name']).agg(unique_leads=('lead_id', 'nunique'), unique_partners=('partner_id', 'nunique')).reset_index()`.

23. **person.sort_values(by=['email', 'id'], inplace=True)**:
The `sort_values()` method sorts the DataFrame by the specified columns. Setting `inplace=True` modifies the original DataFrame without creating a new one.

24. **.transform()**:
The `transform()` method applies a function to a group of values from a DataFrame and returns a DataFrame with the same shape. For example, `joined_table['max_salary'] = joined_table.groupby('departmentId')['salary'].transform('max')` adds a column with the maximum salary for each department.

25. **set()**:
The `set()` function creates a set, which is an unordered collection of unique elements. For example, `allowed_chars = set(string.ascii_lowercase + string.ascii_uppercase + string.digits + '.' + '_' + '-')` creates a set of allowed characters.

26. **pd.concat()**:
The `pd.concat()` function concatenates two or more DataFrames along a particular axis (rows or columns). It is useful for combining datasets.

27. **.iterrows()**:
The `iterrows()` method generates an iterator that yields index and row data as pairs. It is useful for iterating over DataFrame rows.

28. **.find()**:
The `find()` method is used to locate the position of a substring within a string. It returns the index of the first occurrence or -1 if not found.

29. **.issubset()**:
The `issubset()` method determines whether all elements of a set are contained within another set. It returns `True` if the calling set is a subset of another set.

30. **apply(lambda x: x.capitalize())**:
A `lambda` function is an anonymous, inline function defined with the `lambda` keyword. The `apply()` method uses the lambda function to capitalize each element in the column. For example, `apply(lambda x: x.capitalize())` capitalizes the first letter of each element in the column.

31. **pd.to_datetime**:
The `pd.to_datetime` function converts argument to datetime. It can handle different formats of date strings and convert them into datetime objects.

32. **apply(len)**:
The `apply(len)` method applies the `len` function to each element in the Series or each row/column in the DataFrame, returning the length of each element.

33. **pd.DataFrame({'getNthHighestSalary({})'.format(N): [nth_highest_salary]})**:
This line creates a new DataFrame with a single column named 'getNthHighestSalary(N)' where N is a variable, and the column contains the value of `nth_highest_salary`.

34. **patients[patients['conditions'].apply(lambda x: any(cond.startswith('DIAB1') for cond in x.split()))]**:
This line filters the DataFrame to include only rows where the 'conditions' column contains at least one condition that starts with 'DIAB1'.

35. **scores_sorted = scores.sort_values(by='score', ascending=False)**:
The `sort_values()` method sorts the DataFrame by the 'score' column in descending order. Using `method='dense'` with `rank()` assigns ranks to scores, ensuring that duplicate scores receive the same rank.

36. **pd.melt()**:
The `pd.melt()` function unpivots a DataFrame from wide format to long format, making columns into rows. It is useful for transforming data for analysis.

37. **.dropna()**:
The `dropna()` method removes missing values (NaNs) from a DataFrame. You can specify which axis and how to handle the missing values.

38. **pd.notna()**:
The `pd.notna()` function checks for non-missing values in a DataFrame or Series, returning a boolean mask indicating where values are not NaN.

39. **.unique()**:
The `unique()` method returns an array of unique values in a Series or DataFrame column, eliminating duplicate values.

40. **if len(sorted_df) < 2: return pd.DataFrame({'SecondHighestSalary': [None]})**:
This condition checks if the sorted DataFrame has fewer than two rows. If true, it returns a DataFrame with a single entry of `None` under the column 'SecondHighestSalary'.   
