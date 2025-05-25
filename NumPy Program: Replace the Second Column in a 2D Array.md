# NumPy Program: Replace the Second Column in a 2D Array

## 🎯 Aim
To write a **NumPy** program that deletes the second column from a given 2D array and inserts a new column at the same position.

## 🧠 Algorithm
1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Get a 2D NumPy array and a new column (as another array) from the user.
3. **Delete Column**: Use `np.delete()` to remove the second column (index 1) from the original array.
4. **Insert Column**: Use `np.insert()` to insert the new column at the second column's original position.
5. **Display Result**: Print the updated array with the replaced column.

## 🧾 Program
~~~
import numpy as np
rows = int(input("Enter the number of rows: "))
cols = int(input("Enter the number of columns: "))

print(f"Enter the elements of the {rows}x{cols} array row-wise (space-separated):")
data = []
for i in range(rows):
    row = list(map(int, input(f"Row {i+1}: ").split()))
    if len(row) != cols:
        print(f"Error: Please enter exactly {cols} elements.")
        exit()
    data.append(row)

array = np.array(data)
print(f"\nEnter {rows} elements for the new column to insert at column index 1:")
new_column = list(map(int, input("New column values: ").split()))
if len(new_column) != rows:
    print("Error: The new column must have the same number of rows.")
    exit()

new_column_array = np.array(new_column).reshape(rows, 1)
array_without_second_col = np.delete(array, 1, axis=1)
updated_array = np.insert(array_without_second_col, 1, new_column_array, axis=1)
print("\nOriginal Array:")
print(array)

print("\nUpdated Array after replacing second column:")
print(updated_array)

~~~

## Output
![image](https://github.com/user-attachments/assets/3ccd82d6-45d3-4471-ae08-b8395d849520)

## Result
The python program is created and executed successfully.
