# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: A joans jay authers
RegisterNumber: 212221240019
# LEAST SQUARE METHOD 

import matplotlib.pyplot as plt ## library for display the graph
x = [5,6,3,2,6,7,1,2]
y = [2,3,6,5,8,3,5,8]
plt.scatter(x,y) #scatter plot function
plt.plot(x,y) # to map the dot using line 
plt.show() # to display the plot
from sys import base_prefix
import numpy as np
import matplotlib.pyplot as plt

# assign values in array

X = np.array([0,1,2,3,4,5,6,7,8,9])
Y = np.array([1,3,2,5,7,8,8,9,10,12])

# to find the mean values of X and Y

X_mean = np.mean(X)
print(X_mean)
Y_mean = np.mean(Y)
print(Y_mean)

# To Find The Summation

num = 0
denum = 0
for i in range(len(X)):
  num+=(X[i]-X_mean)*(Y[i]-Y_mean)
  denum+=(X[i]-X_mean)**2

# To find the slope for least square method

m=num/denum

  # To find the Y intercept 

b=Y_mean-m*(X_mean)
print(m,b)

#equation of the line 
Y_pred = m*X+b
print(Y_pred)

#plot graph
plt.scatter(X,Y,color='blue')
plt.plot(X,Y_pred,color='orange')
plt.show()
/*
```


## Output:
![1](https://user-images.githubusercontent.com/93427472/199087737-a9db4259-e8a9-4141-a371-d30bb69a490e.png)

![2](https://user-images.githubusercontent.com/93427472/199087762-f3e6a1db-5754-4720-ad36-0913aa4b6581.png)

![3](https://user-images.githubusercontent.com/93427472/199087766-ad289282-a035-4adc-b812-36ed5659a386.png)

![4](https://user-images.githubusercontent.com/93427472/199087772-e9ac0873-121e-4050-bf20-ee0eb661b41f.png)

![5](https://user-images.githubusercontent.com/93427472/199087775-c42aacf8-f3db-494b-bcfe-14966caa56ab.png)

![6](https://user-images.githubusercontent.com/93427472/199087780-d43d5fe3-1267-4d74-8d57-8ad46404080d.png)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
