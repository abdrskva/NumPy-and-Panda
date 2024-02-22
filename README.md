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



import pandas as pd

# Dictionary with batch groups and the number of students
batch_groups_data = {
    'MatMIE': 30,
    'MatDAIS': 25,
    'COMIE': 40,
    'COMEC': 35
}

# Creating a Series using the dictionary
students_series = pd.Series(batch_groups_data)

# Displaying the created Series
print(students_series)




import pandas as pd
import numpy as np

# Sample Python dictionary data
exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}

# List of index labels
labels = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']

# Creating a DataFrame from the dictionary with specified index labels
df = pd.DataFrame(exam_data, index=labels)

# Displaying the created DataFrame
print(df)



import pandas as pd
import numpy as np

# Sample Python dictionary data and list labels
exam_data = {
    'name': ['Anastasia', 'Dima', 'Katherine', 'James', 'Emily', 'Michael', 'Matthew', 'Laura', 'Kevin', 'Jonas'],
    'score': [12.5, 9, 16.5, np.nan, 9, 20, 14.5, np.nan, 8, 19],
    'attempts': [1, 3, 2, 3, 2, 3, 1, 1, 2, 1],
    'qualify': ['yes', 'no', 'yes', 'no', 'no', 'yes', 'yes', 'no', 'no', 'yes']
}

labels = ['Sophia', 'Liam', 'Olivia', 'Noah', 'Ava', 'Isabella', 'Jackson', 'Emma', 'Aiden', 'Mia']

# Creating a DataFrame from the provided data
df = pd.DataFrame(exam_data, index=labels)

# Selecting rows where the number of attempts is greater than 2
selected_rows = df[df['attempts'] > 2]

# Displaying the DataFrame and selected rows
print("Original DataFrame:")
print(df)
print("\nSelected rows where attempts > 2:")
print(selected_rows)
