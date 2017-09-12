## DSS TEAM PROJECTS ( 1 ) - REGRESSION ANALYSIS

Lets play data analysis with regression model !

---

#### [1. House Prices: Advanced Regression Techniques](https://github.com/JKeun/dss-regression-datasets/blob/master/project-house-prices-advanced-data/)
Predict sales prices and practice feature engineering, RFs, and gradient boosting

![](https://kaggle2.blob.core.windows.net/competitions/kaggle/5407/media/housesbanner.png)

#### [2. New York City Taxi Trip Duration](https://github.com/JKeun/dss-regression-datasets/blob/master/project-nyc-taxi-trip-duration-data/)
Share code and data to improve ride time predictions

![](https://github.com/JKeun/dss-regression-datasets/blob/master/project-nyc-taxi-trip-duration-data/header.png)

#### [3. Sberbank Russian Housing Market](https://github.com/JKeun/dss-regression-datasets/blob/master/project-sberbank-housing-market-data/)
Can you predict realty price fluctuations in Russia’s volatile economy?

![](https://github.com/JKeun/dss-regression-datasets/blob/master/project-sberbank-housing-market-data/header.png)

#### [4. Toyota Corolla Prices](https://github.com/JKeun/dss-regression-datasets/blob/master/project-toyotacorolla-data/)
Predict used Toyota Corolla car prices

![](https://github.com/JKeun/dss-regression-datasets/blob/master/project-toyotacorolla-data/header.jpg)

---

### KEY METRICS

#### [1. root-mean-square deviation (RMSD) or root-mean-square error (RMSE)](https://en.wikipedia.org/wiki/Root-mean-square_deviation)

<center><img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/6d689379d70cd119e3a9ed3c8ae306cafa5d5></center>

- [sklearn.metrics.mean_squared_error](http://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_squared_error.html)
```
# sklearn.metrics.mean_squared_error(y_true, y_pred, sample_weight=None, multioutput=’uniform_average’)

from sklearn.metrics import mean_squared_error
y_true = [3, -0.5, 2, 7]
y_pred = [2.5, 0.0, 2, 8]
rmse = mean_squared_error(y_true, y_pred)**(1/2)
```

#### 2. Root Mean Squared Logarithmic Error (RMSLE)

<center><img src="https://kaggle2.blob.core.windows.net/forum-message-attachments/9799/rmsle.png"></center>

```
def rmsle(predicted,real):
    sum=0.0
    for x in range(len(predicted)):
        p = np.log(predicted[x]+1)
        r = np.log(real[x]+1)
        sum = sum + (p - r)**2
    return (sum/len(predicted))**0.5
```
