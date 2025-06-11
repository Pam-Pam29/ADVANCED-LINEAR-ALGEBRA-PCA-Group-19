# Alumath-Matrix Library
A simple matrix multiplication library was created as part of an Advanced Linear Algebra project.

# Features
1. Matrix Multiplication: Performs standard matrix multiplication with proper validation.Contains creative error messages and ASCII art animations
2. Robust Validation: Comprehensive input checking with helpful feedback
3. Lightweight: No external dependencies required

# Installation
From PyPI (Recommended)
```
pip install alumath-peergroup19
```

From Source
```
git clone https://github.com/Pam-Pam29/ADVANCED-LINEAR-ALGEBRA-PCA-Group-19.git
cd ADVANCED-LINEAR-ALGEBRA-PCA-Group-19
pip install.
```

## Quick Start
```
from alumath-peergroup19 import matrix_multiply

# Define your matrices
matrix_a = [
    [1, 2, 3],
    [4, 5, 6]
]

matrix_b = [
    [7, 8],
    [9, 10],
    [11, 12]
]
Multiply them!
result = matrix_multiply(matrix_a, matrix_b)
print(result)
 Output: [[58, 64], [139, 154]]
```

## Basic Matrix Multiplication
```
from alumath-peergroup19 import matrix_multiply
```
**2x2 matrices**
```
a = [[1, 2], [3, 4]]

b = [[5, 6], [7, 8]]

result = matrix_multiply(a, b)

Returns: [[19, 22], [43, 50]]
```

### Different-Sized Matrices
**3x2 and 2x4 matrices**
```

a = [[1, 2], [3, 4], [5, 6]]

b = [[1, 2, 3, 4], [5, 6, 7, 8]]

result = matrix_multiply(a, b)

 Returns: [[11, 14, 17, 20], [23, 30, 37, 44], [35, 46, 57, 68]]
 ```

# What Makes This Library Special
When everything goes right, you'll see:
✅ Matrix multiplication successful!

When things go wrong, you get helpful (and entertaining) error messages created with ASCII art!

# Technical Details
## Requirements
Python 3.6 or higher

No external dependencies

## Matrix Multiplication Rules

Matrix A (m×n) can be multiplied by Matrix B (n×p) to produce Matrix C (m×p)

The number of columns in A must equal the number of rows in B

Result matrix dimensions: rows of A × columns of B

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Version History

1.0.5 - Current stable release.
Includes comprehensive error handling and ASCII art animations.

Supports Python 3.6+.

# Author
ALU Advanced Linear Algebra PCA Group 19
## Python Library

Our custom matrix multiplication library `alumath-peergroup19` developed by the team.

### Repository
- **Main Library Repo**: [ICYEZAGATORE/alumath-peergroup19-](https://github.com/ICYEZAGATORE/alumath-peergroup19-)
- **PyPI Package**: `alumath-matrixlib`


# Acknowledgments
Created as part of the Advanced Linear Algebra coursework.

Thanks to the ALU community for support and feedback.


