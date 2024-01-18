# pandas_cleaning-data
 
In this assignment, we started off with a brief review of pandas basics but mainly focused on cleaning data and practising finding answers to questions that are not explicitly framed in coding language. 

## What I've learned

### Cleaning data
1. `.replace` to replace the entire cell, whereas `str.replace` can replace parts of the cell
2.  To remove things in a column use `.replace` with `""` (empty string)
3. `.dtypes` to check the datatypes and `.astype()` to convert datatypes
4. `.isnull()` and `notnull()` to find missing data then classify them with `.value_counts`
5. Add `na_values = []` up top when reading the csv file, so pandas know what to look out for when you involve `na_values`.
6. `.value_counts` is default to dropping `NaN` values when counting `value_counts(dropna=False)` to get the numbers of `NaN`.
7. `fillna()` 

### Query
1. `.str.contains` to match part of the column. When using this code, be mindful of the `NaN` values. Add `na=False` to avoid errors. 
2. `.describe` to get the distribution.  
3. `!=` to find something that is not what you typed.
4. `value_counts(normalize=True)` get the percentage of the values in each column.
5. Usage of [`lambda`](https://www.geeksforgeeks.org/applying-lambda-functions-to-pandas-dataframe/)

### Join data
1. `merged = prisons_df.merge(states_df, left_on='state', right_on='name')` to join other data. `.merge` is an *inner join* so <ins>rows without a match get discarded</ins>. To do a *left join*, add `how=left` in the parameters to preserve the left column.