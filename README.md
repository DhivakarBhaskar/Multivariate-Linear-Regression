# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Load dataset with input features and target variable.
<br>

### Step2
Preprocess data (clean, normalize, split).
<br>

### Step3
Initialize model parameters
<br>

### Step4
Train the model using an optimization method.
<br>

### Step5
Predict output and evaluate model performance.
<br>

## Program:
```
CREATED BY: Dhivakar B
REGISTER NO: 212225040075
import matplotlib.pyplot as plt
import numpy as np
from sklearn import datasets, linear_model, metrics
from sklearn.model_selection import train_test_split

housing = datasets.fetch_california_housing()
X = housing.data
y = housing.target

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.4, random_state=1
)

reg = linear_model.LinearRegression()
reg.fit(X_train, y_train)

print('Coefficients: ', reg.coef_)
print('Variance score: {}'.format(reg.score(X_test, y_test)))

plt.style.use('fivethirtyeight')
plt.scatter(reg.predict(X_train),
            reg.predict(X_train) - y_train,
            color="green", s=10, label='Train data')

plt.scatter(reg.predict(X_test),
            reg.predict(X_test) - y_test,
            color="blue", s=10, label='Test data')

plt.hlines(y=0, xmin=0, xmax=5, linewidth=2)
plt.legend(loc='upper right')
plt.title('Residual Errors')
plt.show()









```
## Output:
<img width="1365" height="381" alt="image" src="https://github.com/user-attachments/assets/f01dd8a9-8a1b-4ee5-b3c5-f8cbfb19bcfb" />


### Insert your output

<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
