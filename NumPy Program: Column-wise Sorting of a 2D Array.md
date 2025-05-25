# NumPy Program: Column-wise Sorting of a 2D Array

## 🎯 Aim
To write a **NumPy** program that sorts the elements in each column of a given 2D array in ascending order.

## 🧠 Algorithm

1. **Import NumPy**: Start by importing the NumPy library.
2. **Get Input**: Accept a 2D NumPy array from the user.
3. **Sort Column-wise**: Use the `np.sort()` function with `axis=0` to sort each column in ascending order.
4. **Store Result**: Store the sorted result in a new array.
5. **Display Output**: Print the original array and the column-wise sorted array.

##
🧾 Program
~~~
mport numpy as np

rows = int(input())
cols = int(input())

elements = []

for i in range(rows):
    row = list(map(int, input(f"Row {i+1}: ").split()))
    if len(row) != cols:
        print(f"Error: Please enter exactly {cols} elements.")
        exit()
    elements.append(row)

array = np.array(elements)

sorted_array = np.sort(array, axis=0)

print("\nOriginal Array:")
print(array)

print("\nColumn-wise Sorted Array:")
print(sorted_array)

~~~
## Output
![image](https://github.com/user-attachments/assets/44b83fd8-053f-4c30-b486-f7447c11ff35)

## Result
The python program is created and executed successfully.
