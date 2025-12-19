# THB-EU
# Establishes df as the CSV data
df = pd.read_csv("Python_project.csv")
#Prints df
print(df)
            Country  Year  Value
0   The Netherlands  2020   5.65
1   The Netherlands  2021   4.53
2   The Netherlands  2022   4.63
3   The Netherlands  2023   4.87
4           Romania  2020   3.08
5           Romania  2021   2.63
6           Romania  2022   2.63
7           Romania  2023   2.37
8          Portugal  2020   1.02
9          Portugal  2021   1.94
10         Portugal  2022   2.38
11         Portugal  2023   3.90
12           Cyprus  2020   2.82
13           Cyprus  2021   2.34
14           Cyprus  2022   1.77
15           Cyprus  2023   3.58
# Asked to import packages necessary for the regression analysis
import statsmodels.api as sm
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np
# Data defined as data in CSV
data = pd.read_csv('Python_project.csv')
# x defined as the years
x = data['Year'].tolist()
# y defined as the values (number of THB victims per hundred thousand people)
y = data['Value'].tolist()
# Constant defined for the regression
x = sm.add_constant(x)
# Result defined as the OLS regression
result = sm.OLS(y,x).fit()
# Result printed leading to the OLS regression table
print(result.summary())
                            OLS Regression Results                            
==============================================================================
Dep. Variable:                      y   R-squared:                       0.021
Model:                            OLS   Adj. R-squared:                 -0.049
Method:                 Least Squares   F-statistic:                    0.3012
Date:                Fri, 19 Dec 2025   Prob (F-statistic):              0.592
Time:                        12:13:57   Log-Likelihood:                -25.930
No. Observations:                  16   AIC:                             55.86
Df Residuals:                      14   BIC:                             57.40
Df Model:                           1                                         
Covariance Type:            nonrobust                                         
==============================================================================
                 coef    std err          t      P>|t|      [0.025      0.975]
------------------------------------------------------------------------------
const       -321.3170    591.200     -0.543      0.595   -1589.315     946.681
x1             0.1605      0.292      0.549      0.592      -0.467       0.788
==============================================================================
Omnibus:                        1.441   Durbin-Watson:                   0.468
Prob(Omnibus):                  0.487   Jarque-Bera (JB):                1.062
Skew:                           0.591   Prob(JB):                        0.588
Kurtosis:                       2.559   Cond. No.                     3.66e+06
==============================================================================

Notes:
[1] Standard Errors assume that the covariance matrix of the errors is correctly specified.
[2] The condition number is large, 3.66e+06. This might indicate that there are
strong multicollinearity or other numerical problems.
# Packages imported for visualization
import matplotlib.pyplot as plt
import seaborn as sns
import pandas as pd
import numpy as np
# df established as CSV
df = pd.read_csv("Python_project.csv")
# Plot of the df estbalished as scatter, with years as x and values as y
df.plot(kind="scatter",x="Year",y="Value")
# df plot printed and resulting chart
print(df.plot)
 <pandas.plotting._core.PlotAccessor object at 0x78a42e5e2690>
<img width="555" height="432" alt="image" src="https://github.com/user-attachments/assets/3857261a-d7a9-4821-bb2d-88d6b08cb4d1" />

