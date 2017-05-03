# Pandas

## Intro to Pandas

**Read in a CSV file**

```
import pandas
pandas.read_csv('file_name.csv')
```

_dataframe = custom data structure_

**Head method** - return first _n_ rows:

```
pd.head(n)
```

**Column attribute** - return column names:

```
pd.columns <-- dataframe of columns; convert to list with tolist() method
```

**Shape attribute** - return a tuple of integers representing the number of rows by columns:

```
pd.shape <-- (# rows, # columns)
```

_Series object_ = core data structure use by pandas to represent rows and columns. A one-dimensional labeled array capable of holding any data type. A dataframe is like a dict of series objects.

**Selecting a row**

```
pd.loc[n]
pd.loc[n:m]
pd.loc[n,m,o]
```

**Selecting a column**

```
pd[n]
pd[[n,m,o]]
```

## Pandas: Intermediate

**Transforming a column**

Using arithemetic operators:

```
new_col_1 = pd["col_name"] / n <-- divides each row in the column by n
new_col_2 = pd["col_name_1"] + pd["col_name_2"] <-- performs pair-wise addition
```

**Noramlizing columns in a dataset**

To normalize a column, each item in the column can be divided by the maximum value to create a range fo 0 to 1

```
max_calories = food_info["Energ_Kcal"].max() normalized_calories = food_info["Energ_Kcal"] / max_calories
```

**Inserting a new column**

```
 pd["new_col_name"] = new_pd_col
 ```

**Sorting by a column**

```
DataFrame.sort_values("name or list of names in axis", axis=0, ascending=True, inplace=False, kind='quicksort', na_position='last')
```

**Check for null values (NaN for pandas)**

```
pandas.isnull(obj) <-- returns an series object of boolean values
```

**Count unique elements in a series**
```
Series.value_counts()
```

**Descriptive statistics for a series**
```
Series.describe(percentiles=None, include=None, exclude=None)
```



