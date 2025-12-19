# THB-EU
import statsmodels.api as sm
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np
data = pd.read_csv ('Python_project(Feuil1).csv')
x = data ['year'].tolist()
y = data ['country'].tolist()
x = sm.add_constant (x)
result = sm.OLS (y,x).fit ()
print (result.summary ())
