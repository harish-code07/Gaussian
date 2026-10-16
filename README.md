# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import numpy and sys module packages.
2. Initialize the matrix with zeroes, get inputs and store it.
3. Using conditional statements and gaussian elimination, find the solution.
4. Print the Result.

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Harish Bakavadh J
RegisterNumber: 26007865
'''
import os 
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
import sys
n= int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)

for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
        
for i in range (n):
    if a[i][i]==0.0:
        sys.exit('Divide be zero detected')
    for j in range (i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range (n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]

x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
    
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end=' ')

/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: 
RegisterNumber: 
*/
```

## Output:
![gaussian elimination]()
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/53ece7fb-4b90-4738-be4f-e27641145c8f" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f31bd01e-ff14-4031-ad4d-e85be010a1f4" />


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

