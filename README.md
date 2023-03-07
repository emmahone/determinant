# Determinants

Determinants of matrices have some important properties that are useful in linear algebra. Here are some of the most important properties of determinants:

- Multiplying a row or column of a matrix by a scalar multiplies the determinant by the same scalar.

- Swapping two rows or columns of a matrix changes the sign of the determinant.

- Adding a multiple of one row or column to another row or column does not change the value of the determinant.

- If two rows or columns of a matrix are identical, the determinant is 0.

- If one row or column of a matrix is a linear combination of the other rows or columns, the determinant is 0.

- If a matrix has a row or column of all zeros, the determinant is 0.

- If a matrix is triangular, meaning all the elements below (or above) the main diagonal are zero, the determinant is the product of the diagonal elements.

- If two matrices have the same size and their corresponding entries are equal, then their determinants are equal.

- The determinant of a product of matrices is equal to the product of their determinants.

- The determinant of the transpose of a matrix is equal to the determinant of the original matrix.

These properties can be used to simplify calculations involving determinants, and they also help in proving other mathematical theorems related to matrices and linear algebra.

# Calculate determinant of a matrix
The determinant of a matrix is a scalar value that can be calculated from the elements of the matrix. The determinant is often used in linear algebra to solve systems of linear equations, find eigenvalues and eigenvectors, and invert matrices. Here's how to calculate the determinant of a matrix:

1. For a 2x2 matrix A = [[a,b], [c,d]], the determinant is defined as det(A) = ad - bc.

2. For a larger square matrix A of size n x n, the determinant can be calculated using the Laplace expansion or cofactor expansion method. Here are the steps:

- Choose a row or column of the matrix A.
- For each element in that row or column, create a submatrix by removing the row and column that contain that element. The submatrix will have size (n-1) x (n-1).
- Calculate the determinant of the submatrix.
- Multiply the determinant of the submatrix by the element in the original matrix that you removed, and add up all these products.

Here's the formula:

```
det(A) = a[1,1]C[1,1] - a[1,2]C[1,2] + a[1,3]C[1,3] - ... + (-1)^(n+1) a[1,n]C[1,n]
```

where C[i,j] is the cofactor of A[i,j], which is (-1)^(i+j) times the determinant of the submatrix obtained by removing row i and column j from A.

3. Once you've calculated the cofactors for all the elements in the first row or column, you can sum up all the products to get the determinant of A.
Note that calculating the determinant can be computationally expensive, especially for large matrices, and there are more efficient methods for solving systems of linear equations and finding eigenvalues and eigenvectors. Nonetheless, calculating the determinant can be a useful tool in linear algebra.

# Script
Here's how the script works:

The user inputs the size of the matrix.
The script creates a matrix A of size nxn filled with random integers between 0 and 9.
The determinant of A is calculated using NumPy's linalg.det() function.
The determinant value is printed to the console.
Note that this script assumes that NumPy is already installed on your machine. If you don't have NumPy installed, you can install it using the command pip install numpy.

```
import numpy as np

# define matrix size
n = int(input("Enter size of matrix: "))

# create matrix with random integers
A = np.random.randint(0, 10, (n, n))
print("Matrix A:\n", A)

# calculate determinant using NumPy's det() function
det = np.linalg.det(A)

# print determinant value
print("Determinant of A:\n", det)
```
