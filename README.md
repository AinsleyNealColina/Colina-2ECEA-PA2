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

`
import numpy as np
`

2.create a random 5 x 5 by using np.random.rand it is a function from the NumPy library used to generate an array of random values

`
X = np.random.rand(5, 5)
`

`
print("Original Array X:\n", X)
`

3.use the .mean() and .std() before the period put x to compute the mean and standard deviation of the array

`
mean_X = X.mean()
std_X = X.std()
`

`
print("Mean of X:", mean_X)
print("Standard Deviation of X:", std_X)
`

4.To normalize the array we must declare  a variable then put the equation,then call the variable

`
X_normalized = (X - mean_X) / std_X
`

`
print("Normalized Array X_normalized:\n", X_normalized)
`

5.Save the normalized array into a .npy file
