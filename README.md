# Colina-2ECEA-PA2(Experiment2 Numerical Python)

## Objectives
1. To identify the codes and functions incorporated in the Numpy library 
2. To be able to apply and use the different codes and functions in creating a Python program using a 
Numpy library 

## Problem 1: Normalization
Normalization is one of the most basic preprocessing techniques in 
data analytics. This involves centering and scaling process. Centering means subtracting the data from the 
mean and scaling means dividing with its standard deviation.It can be expressed as:

<img width="200" height="200" alt="image" src="https://github.com/user-attachments/assets/fb8cbe96-3d00-410b-83ec-3a3f428d9f65" />

So we are tasked to:
1. Create a random 5 x 5 ndarray and store it to variable X
2. Obtain its mean and standard deviation using .mean() & .std()
3. Normalize the array using the formula above.
4. Save the normalized array as X_normalized.npy

Steps:

1.import numpy as np it is for numerical operations

```python
# Import the NumPy library for numerical operations
import numpy as np
```

2.create a random 5 x 5 by using np.random.rand it is a function from the NumPy library used to generate an array of random values

```python
# Generate a 5x5 array of random floats between 0 and 1
X = np.random.rand(5, 5)

#Prints the original array and inside it is the value of X from earlier
print("Original Array X:\n", X)
```

3.use the .mean() and .std() before the period put x to compute the mean and standard deviation of the array

```python
#Gets the mean of X with the use of function .mean()
mean_X = X.mean()

#Gets the std of X with the use of function .std()
std_X = X.std()

#Displays the mean of X
print("Mean of X:", mean_X)

#Displays the std of X
print("Standard Deviation of X:", std_X)
```

4.To normalize the array we must declare  a variable then put the equation,then call the variable

```python
#Formula for Normalization
X_normalized = (X - mean_X) / std_X

#Displays the Normalized array inside it is the normalized X
print("Normalized Array X_normalized:\n", X_normalized)
```

5.Save the normalized array into a .npy file

```python
#Saves the normalized X
np.save('X_normalized.npy', X_normalized)

#Displays if the Normalized X has been saved
print("X_normalized.npy has been saved.")
```

## Problem 2: Elements divisible by 3

Construct a 10×10 ndarray containing the squares of the first 100 positive integers:

<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/cd0b07ef-03b0-47ec-84c2-22132caa8588" />

So we are tasked to:

1.Generate numbers from 1 to 100

2.Square them to form the array.

3.Reshape into a 10×10 matrix

4.Use Boolean indexing to obtain all the elements that are divisible by 3

5.Save the result as div_by_3.npy.

Steps:

1.We use np.arange(1, 101)**2 to create an array of integers starting at 1 and ending at 100 and squaring it, then A.reshape(10,10) so it has 10 rows and columns.

```python
# Create a 1D array of squares of the first 100 positive integers
A = np.arange(1, 101) ** 2

#Reshapes the 1D array to a 10x10 2D array for better readability
A = A.reshape(10, 10)

# Print the 10x10 array of squared values
print("Array A (Squares of the first 100 positive integers):\n", A)
```

2.We apply the condition A % 3 == 0 which returns a Boolean mask, and use it to extract values divisible by 3.

```python
# Extract elements from A that are divisible by 3 using boolean indexing(the %3 == 0,checks if it is divisible by 3 with no remainder)
div_by_3 = A[A % 3 == 0]

# Print the filtered elements that are divisible by 3
print("Elements of A divisible by 3:\n", div_by_3)
```

3.Finally, we save the filtered elements into a .npy file using np.save.

```python
# Save the filtered array to a .npy file for later use or sharing
np.save('div_by_3.npy', div_by_3)

# Confirm that the file has been successfully saved
print("div_by_3.npy has been saved.")
```
