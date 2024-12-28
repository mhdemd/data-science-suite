# NumPy Basics

NumPy (Numerical Python) is a powerful library for numerical and scientific computing in Python. Here, we cover the most essential features you need to get started with NumPy.

## Installation

To install NumPy, run the following command in your terminal or CMD:

    pip install numpy

> **Tip**: If you are using Jupyter Notebook and don't have permission to install packages, consider using a virtual environment (venv) or conda.

---

## Importing NumPy

The common convention for importing NumPy is:

    import numpy as np

This allows you to refer to NumPy objects using the short alias `np`.

---

## Creating NumPy Arrays

1. **Converting a Python list to a NumPy array**  

       my_list = [1, 2, 3, 4]
       arr = np.array(my_list)
       print(arr)
       # Output: [1 2 3 4]

2. **Creating arrays of zeros and ones**  

       zeros_1d = np.zeros(5)         # 1D array of length 5
       zeros_2d = np.zeros((3, 4))    # 2D array (3 rows, 4 columns)

       ones_1d = np.ones(5)
       ones_2d = np.ones((3, 4))

3. **linspace and arange**  

       arr_lin = np.linspace(0, 10, 5)   # [0. , 2.5, 5. , 7.5, 10. ]
       arr_arange = np.arange(0, 10, 2)  # [0, 2, 4, 6, 8]

---

## Basic Array Attributes

Let's suppose you have:

    my_array = np.array([
        [1, 2, 3],
        [4, 5, 6]
    ])

- Shape:  

       print(my_array.shape)
       # (2, 3)

- Number of dimensions (ndim):  

       print(my_array.ndim)
       # 2

- Total number of elements (size):  

       print(my_array.size)
       # 6

- Data type (dtype):  

       print(my_array.dtype)
       # e.g. int64 (depends on your system)

---

## Indexing and Slicing

1. **Simple indexing**  

       element = my_array[0, 1]  # Row 0, Column 1 => 2

2. **Negative indexing**  

       last_element = my_array[-1, -1]  # Last row, last column => 6

3. **Slicing**  

       sub_array = my_array[:, 1:]  
       # All rows, columns from index 1 onward => [[2, 3],
       #                                          [5, 6]]

4. **Boolean indexing**  

       arr = np.array([1, 2, 3, 4, 5])
       even = arr[arr % 2 == 0]   # [2, 4]

---

## Practice Exercises

1. Create a 3x3 array and extract elements below the main diagonal.  
2. Create both a 1D and 2D array, then practice different indexing/slicing operations.

In the next files, we will explore mathematical operations and reshaping arrays in more detail.
