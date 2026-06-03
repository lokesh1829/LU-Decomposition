# LU Decomposition 

## AIM:
To write a program to find the LU Decomposition of a matrix.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
~~~
1. LU Decomposition (printing L and U)
Algorithm (4 steps):
Read the matrix A.
Perform LU decomposition of A to obtain P, L, and U.
Extract L (lower-triangular) and U (upper-triangular) matrices.
Display L and U.
2. Solving AX = B using LU Decomposition
Algorithm (4 steps):
Read matrices A and B and perform LU decomposition to get P, L, U.
Compute Pb by multiplying Pᵀ with B.
Solve the forward substitution Ly = Pb.
Solve the backward substitution Ux = y and print x.
~~~

## Program:
(i) To find the L and U matrix
```
/*
Program to find the L and U matrix.
Developed by: Lokesh K
RegisterNumber: 212225240080
*/
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
from scipy.linalg import lu
A=np.array(eval(input()))
P,L,U=lu(A)
print(L)
print(U)
```
(ii) To find the LU Decomposition of a matrix
```
/*
Program to find the LU Decomposition of a matrix.
Developed by: Lokesh,k
RegisterNumber: 212225240080
*/
'''Program to solve a matrix using LU decomposition.
Developed by: 
RegisterNumber: 
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"

# To print X matrix (solution to the equations)
import numpy as np
from scipy.linalg import lu_factor,lu_solve
A=np.array(eval(input()))
b=np.array(eval(input()))
lu,piv=lu_factor(A)
X=lu_solve((lu,piv),b)
print(X)
```

## Output:
![lu decomposition]()
<img width="1320" height="872" alt="image" src="https://github.com/user-attachments/assets/5a00910d-3d58-4fc0-a3e6-ebdf429af55c" />

<img width="1315" height="719" alt="image" src="https://github.com/user-attachments/assets/0c338319-abfd-494f-aa81-965edb590099" />


## Result:
Thus the program to find the LU Decomposition of a matrix is written and verified using python programming.

