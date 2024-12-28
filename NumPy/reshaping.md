# Reshaping Arrays in NumPy

This file demonstrates how to reshape arrays, flatten them, and concatenate them.

---

## Reshaping (reshape)

1. **Basic reshape**

       import numpy as np

       arr = np.array([1, 2, 3, 4, 5, 6])
       reshaped = arr.reshape((2, 3))
       print(reshaped)
       # [[1, 2, 3],
       #  [4, 5, 6]]

2. **Using -1 to infer the dimension**

       arr = np.array([1, 2, 3, 4, 5, 6, 7, 8])
       reshaped = arr.reshape((2, -1))
       print(reshaped)
       # [[1, 2, 3, 4],
       #  [5, 6, 7, 8]]

---

## Flatten and ravel

1. **flatten**

       mat = np.array([
           [1, 2, 3],
           [4, 5, 6]
       ])
       flat = mat.flatten()
       print(flat)  # [1, 2, 3, 4, 5, 6]

2. **ravel**

       flat_ravel = mat.ravel()
       print(flat_ravel)  # [1, 2, 3, 4, 5, 6]
       # ravel() tries to return a view (instead of a copy) if possible.

---

## Concatenation and Stacking

1. **Concatenate**

       a1 = np.array([1, 2, 3])
       a2 = np.array([4, 5, 6])
       cat = np.concatenate((a1, a2))
       print(cat)  # [1, 2, 3, 4, 5, 6]

2. **vstack and hstack**

       arr1 = np.array([
           [1, 2],
           [3, 4]
       ])
       arr2 = np.array([
           [5, 6],
           [7, 8]
       ])

       v_stacked = np.vstack((arr1, arr2))
       # [[1, 2],
       #  [3, 4],
       #  [5, 6],
       #  [7, 8]]

       h_stacked = np.hstack((arr1, arr2))
       # [[1, 2, 5, 6],
       #  [3, 4, 7, 8]]

---

## Practice Exercises

1. Create a 1x12 array and reshape it into a 3x4 matrix. Then flatten it using both `flatten()` and `ravel()`.  
2. Create two 2D arrays of the same size and concatenate them both vertically and horizontally.

By the end of this section, you should be comfortable with reshaping arrays and merging them in different ways.
