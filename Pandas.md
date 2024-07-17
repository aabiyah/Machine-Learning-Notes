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
