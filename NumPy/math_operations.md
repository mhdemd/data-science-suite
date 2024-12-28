# Mathematical Operations in NumPy

In this section, we explore common arithmetic and statistical operations in NumPy.

---

## Basic Arithmetic

1. **Element-wise addition, subtraction, multiplication, and division**

       import numpy as np

       arr1 = np.array([1, 2, 3])
       arr2 = np.array([4, 5, 6])

       sum_arr = arr1 + arr2        # [5,  7,  9]
       diff_arr = arr2 - arr1       # [3,  3,  3]
       mul_arr = arr1 * arr2        # [4, 10, 18]
       div_arr = arr2 / arr1        # [4.0, 2.5, 2.0]

2. **Sum along an axis**

       mat = np.array([
           [1, 2],
           [3, 4],
           [5, 6]
       ])
       sum_all = mat.sum()          # 21
       sum_rows = mat.sum(axis=1)   # [3, 7, 11]
       sum_cols = mat.sum(axis=0)   # [9, 12]

3. **Dot product (matrix multiplication)**

       A = np.array([[1, 2],
                     [3, 4]])
       B = np.array([[5, 6],
                     [7, 8]])
       product = A.dot(B)
       # [[19, 22],
       #  [43, 50]]

---

## Statistical Functions

1. **Mean, standard deviation, variance**

       arr = np.array([1, 2, 3, 4, 5])
       print(arr.mean())   # 3.0
       print(arr.std())    # ~1.4142
       print(arr.var())    # 2.0

2. **Minimum, maximum, and median**

       print(arr.min())        # 1
       print(arr.max())        # 5
       print(np.median(arr))   # 3.0

3. **argmin and argmax**

       print(arr.argmin())  # 0 (index of min value)
       print(arr.argmax())  # 4 (index of max value)

---

## Other Mathematical Functions

1. **Exponent, log, and power**

       x = np.array([1, 2, 3])
       exp_x = np.exp(x)         # [e^1, e^2, e^3]
       log_x = np.log(x)         # [ln(1), ln(2), ln(3)]
       power_x = np.power(x, 2)  # [1, 4, 9]

2. **Trigonometric functions**

       angles = np.array([0, np.pi/2, np.pi])
       sin_vals = np.sin(angles)  # [0, 1, 0]
       cos_vals = np.cos(angles)  # [1, 0, -1]

---

## Practice Exercises

1. Create a 3x3 matrix and compute the sum of each row and column.  
2. Perform matrix multiplication between a 2x3 and a 3x2 matrix.  
3. Create a random array and compute its mean and variance.

By completing these exercises, you will strengthen your understanding of NumPy's arithmetic and statistical capabilities.
