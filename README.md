# Multiple-Linear-Regression
A Multiple Linear Regression in Pandas for Python

#testcode:
#You should download the file NBA_train.csv in the main page of my repository!

import panads as pd
import statsmodels.api as sm

NBA = pd.read_CSV("NBA_train.csv")
Y = NBA[ 'w' ]
X = NBA[['PTS', 'oppPTS']]
X = sm.add_constant(X)
model11 = sm.OLS(Y, X).fit()
model11.summary()
