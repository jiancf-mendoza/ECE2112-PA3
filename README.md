# ECE2112-PA3
Jian Mendoza | 2ECEA
#  Intended Learning Outcomes
1. create and reshape NumPy arrays using appropriate NumPy functions;
2. perform vectorized numerical operations on an ndarray;
3. compute array statistics and use Boolean conditions to select elements; and
4. save computed NumPy arrays as .npy file
# A. POSITIONAL AND LABEL-BASED SLICING
- Display the shape and complete list of column names of cars. Using positional slicing, create cars 6 to 10 containing rows 6 through 10 of the dataset, where
the first data row is row 1. From cars 6 to 10, display only the columns Model, mpg, cyl, hp, and gear, in that order.
- Requirement: The row selection in part (b) must use iloc; the column selection in part (c) must
use column labels.
- ## What Happened?

```python
import pandas as pd

print("Shape of cars: ", cars.shape)
print("Column names: ", cars.columns.tolist())

cars_6_to_10 = cars.iloc[5:10]

selected_columns = cars_6_to_10[['Model', 'mpg', 'cyl', 'hp', 'gear']]
print(selected_columns)
```

# B. MODEL LOOKUP
# C. MULTI-MODEL SUBSETTING
