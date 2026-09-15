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
- ## Implementation
```python
import pandas as pd

print("Shape of cars: ", cars.shape)
print("Column names: ", cars.columns.tolist())

cars_6_to_10 = cars.iloc[5:10]

selected_columns = cars_6_to_10[['Model', 'mpg', 'cyl', 'hp', 'gear']]
print(selected_columns)
```

# B. MODEL LOOKUP
- Display the complete row for Toyota Corolla. For Pontiac Firebird, display only Model, mpg, hp, and wt.
Store the two results in toyota and pontiac, respectively. Do not use a hard-coded row number to
locate either model.
- ## What Happened?
- ## Implementation
```python
toyota = cars[cars['Model'] == 'Toyota Corolla']
print("Toyota Corolla: ")
print(toyota)

pontiac = cars[cars['Model'] == 'Pontiac Firebird']
print("\n", "Pontiac Firebird: ")
print(pontiac)
```
# C. MULTI-MODEL SUBSETTING
- Create a DataFrame named selected cars containing only the records for three models: Datsun 710,
Lotus Europa, and Ferrari Dino. For these records, retain only Model, mpg, cyl, hp, and gear. Select the rows by their model values
rather than by row numbers. Display selected cars and its shape.
- Required check: The final DataFrame must contain exactly three rows and five columns.
- ## What Happened?
- ## Implementation
```python
target_models = ["Datsun 710", "Lotus Europa", "Ferrari Dino"]
target_columns = ["Model", "mpg", "cyl", "hp", "gear"]

selected_cars = cars[cars["Model"].isin(target_models)][target_columns]

print("Selected Cars: ")
print(selected_cars)
print("\n", "Shape of Selected_cars: ")
```

