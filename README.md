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
import numpy as np

x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])

plt.scatter(x,y)
plt.show()

xmean = np.mean(x)
ymean = np.mean(y)

num=0
den=0

for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2

m = num/den
b = ymean - m*xmean

print(m,b)
y_pred = m*x+b
print(y_pred)

```
## Output
<img width="771" height="598" alt="Screenshot 2025-10-18 093108" src="https://github.com/user-attachments/assets/42f9385b-a8a2-43a2-9781-de52d5172aaa" />


<img width="679" height="508" alt="Screenshot 2025-10-18 093122" src="https://github.com/user-attachments/assets/d49ee466-c1b4-4600-85bd-5e26580bb457" />


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
