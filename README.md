# ECE-2112-PA-2

### Made by John Felix C. Francisco | 2ECE-C

##### This repository contains the solution to the Programming Assignment 2 for the course “Advance Computer Programming and Algorithms,” this S.Y. 2026-2027. It tackles three python problems involving Module 2, which is about Numpy. 

##### The objective of this experiment is for students to:
##### 1. create and reshape NumPy arrays using appropriate NumPy functions;
##### 2. perform vectorized numerical operations on an ndarray;
##### 3. compute array statistics and use Boolean conditions to select elements; and
##### 4. save computed NumPy arrays as .npy files.

# A. Reproducible Normalization Problem
##### Create a reproducible random 5x5 integer ndarray named “X” using these two statements;
```
np.random.seed(2112)
X = np.random.randint(10, 101, size=(5, 5))
```
##### Afterwards, normalize the array and display it along with its mean, standard deviation and the original array X. 

### The following functions were used:
##### `.mean()` - a function that gets the mean of all the elements in the array.
##### Example. 
```
A = np.array([1,2,3,4])
A.mean() —> “4.65”
```
##### `.std()` - a function that gets the standard deviation of the array.
##### Example. 
```
A = np.array([1,2,3,4])
A.std() —> “1.118033988749895” 
```
##### `round(number, decimal places)` - a function that returns a floating point number that rounds the specified number to the desired number of decimals.
##### Example. 
```
X = 1.2345
round(X, 2) —--> “1.23”
round(X) —--> “1” #returns an integer
```
##### Before all else, NumPy was imported as np for the program to work. Through these functions, the normalized array, which we’ll call X_normalized, was obtained along with its mean, and standard deviation, forming the program,
```python
import numpy as np

np.random.seed(2112)
X = np.random.randint(10, 101, size=(5, 5))

X_normalized = (X - X.mean())/X.std()

print(X)
print(X_normalized)
print(round(X_normalized.mean()))
print(round(X_normalized.std()))
```

# B. Cubes Divisible by 4 Problem
##### Create a 10 x 10 array of the cubes of the first 100 positive integers and name it “C.” Use a boolean condition to every cubed element that is divisible by 4, which is to be stored in the array named “div_by_4.”

### The following functions and methods were used:
##### `np.linspace(a,b,c)` - a function that creates an array of evenly spaced values from a to b with c as the number of elements. 
##### Example. 
`np.linspace(1,10,10) —> array([ 1.,  2.,  3.,  4.,  5.,  6.,  7.,  8.,  9., 10.])`

##### `np.int64()` - a data type class that converts the array’s elements into 64-bit integers.
##### Example. 
```
A = np.int64(np.array([1.1,2.2,3.3,4.4]))
A —> array([1,2,3,4])
```
##### `.resize(row, column)` - a method that changes the shape of the array without changing the data. 
##### Example. 
```
A  = np.array([1,2,3,4])
A.resize(2,2) —> array([1,2],
                      [3,4])
```
##### Array indexing was used to get the values divisible by 4. It uses the modulus operator to get the remainder of each element. Then, it was compared to the value of 0 as values divisible to 4 should have a remainder of 0. Before all else, Numpy was imported as np for the program to work. All of these functions and methods were combined to create the program,
``` python
import numpy as np

C = np.int64(np.linspace(1, 100, 100))**3
C.resize(10, 10)

div_by_4 = C[(C%4) == 0]
div_by_4

print(C)
print(div_by_4)
```
# C. Above-mean Squares Problem
##### Create a 6 x 6 array that contains the squares of the first 36 positive integers and name it “S.” Get the mean of the array and store it in “S_mean.” Through boolean filtering, select the values greater than the mean, and store it in “above_mean.”
### The following functions and methods were used:
##### `np.linspace(a,b,c)` - a function that creates an array of evenly spaced values from a to b with c as the number of elements. 
##### Example. 
`np.linspace(1,10,10) —> array([ 1.,  2.,  3.,  4.,  5.,  6.,  7.,  8.,  9., 10.])`

##### `np.int64()` - a data type class that converts the array’s elements into 64-bit integers.
##### Example. 
```
A = np.int64(np.array([1.1,2.2,3.3,4.4]))
A —> array([1,2,3,4])
```
##### `.resize(row, column)` - a method that changes the shape of the array without changing the data. 
##### Example. 
```
A  = np.array([1,2,3,4])
A.resize(2,2) —> array([1,2],
                      [3,4])
```
##### `.mean()` - a function that gets the mean of all the elements in the array.
##### Example. 
```
A = np.array([1,2,3,4])
A.mean() —> “4.65”
```

##### Array Indexing was used to select the values greater than the array’s mean. Before all else, NumPy was imported as np for the program to function. Combining these functions and methods, the following program was created, 
```python
import numpy as np

S = np.int64(np.linspace(1,36,36)**2)
S.resize(6,6)
S_mean = S.mean()
above_mean = S[S>S.mean()]

print(S)
print(S_mean)
print(above_mean)
```
##### Thank you for reading!

##### If you want to try the main program for the Programming Assignment 2, kindly refer to the link: https://github.com/JFFrancisco0/Problem-Assignment-2---Francisco.git, and download the ipnyb file. Afterwards, open it in Jupyter Notebook and run all the cells. 

##### READme File History:
##### August 31, 2026 - Initial READme content upload
