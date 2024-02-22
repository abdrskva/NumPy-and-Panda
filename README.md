import pandas as pd
import numpy as np

# Creating a Series with integers and custom index
series_int = pd.Series([1, 2, 3, 4], index=['a', 'b', 'c', 'd'])

# Creating a Series with floating-point numbers and dates as index
series_float = pd.Series([1.1, 2.2, 3.3, 4.4], index=pd.date_range('2022-01-01', periods=4))

# Creating a Series with strings and named index
series_str = pd.Series(['apple', 'banana', 'cherry', 'date'], index=['fruit1', 'fruit2', 'fruit3', 'fruit4'])

# Creating a Series with boolean values and a categorical index
series_bool = pd.Series([True, False, True, False], index=pd.Categorical(['Category A', 'Category B', 'Category A', 'Category B']))

# Creating a Series with numpy NaN (Not a Number) for missing data
series_with_nan = pd.Series([1, 2, np.nan, 4])

# Displaying the created Series
print(series_int)
print(series_float)
print(series_str)
print(series_bool)
print(series_with_nan)






import pandas as pd

# Creating a Series with months' numbers as data and month names as index
months_data = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]
month_names = ['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December']

month_series = pd.Series(months_data, index=month_names)

# Displaying the created Series
print(month_series)
