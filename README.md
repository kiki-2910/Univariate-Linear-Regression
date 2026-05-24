# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
DEVELOPED BY: S.KEERTHANA
REGISTER NUMBER: 212225040186

import numpy as np
import matplotlib.pyplot as plt


x = np.array([1, 2, 3, 4, 5])
y = np.array([2, 4, 5, 4, 5])


x_mean = np.mean(x)
y_mean = np.mean(y)


m = np.sum((x - x_mean) * (y - y_mean)) / np.sum((x - x_mean) ** 2)
c = y_mean - m * x_mean


y_pred = m * x + c


print("Slope (m) =", m)
print("Intercept (c) =", c)
print("Equation of line: y =", m, "x +", c)


plt.scatter(x, y, color='blue', label='Data Points')
plt.plot(x, y_pred, color='red', label='Regression Line')
plt.xlabel("X")
plt.ylabel("Y")
plt.title("Univariate Linear Regression")
plt.legend()
plt.show()



```
## Output
<img width="439" height="83" alt="image" src="https://github.com/user-attachments/assets/8ca25900-30ec-44dd-81dd-47624e601544" />

<img width="980" height="585" alt="image" src="https://github.com/user-attachments/assets/1cb3fd22-b0fb-4d79-8376-2847c3dc602f" />

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
