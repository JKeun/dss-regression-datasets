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

#### 1. root-mean-square deviation (RMSD) or root-mean-square error (RMSE)
![](https://wikimedia.org/api/rest_v1/media/math/render/svg/6d689379d70cd119e3a9ed3c8ae306cafa5d516d)

[sklearn.metrics.mean_squared_error](http://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_squared_error.html)
```
sklearn.metrics.mean_squared_error(y_true, y_pred, sample_weight=None, multioutput=’uniform_average’)
```

#### 2. Root Mean Squared Logarithmic Error (RMSLE)
$$\epsilon = \sqrt{\frac{1}{n} \sum_{i=1}^n (\log(p_i + 1) - \log(a_i+1))^2 }$$

```
def rmsle(predicted,real):
    sum=0.0
    for x in range(len(predicted)):
        p = np.log(predicted[x]+1)
        r = np.log(real[x]+1)
        sum = sum + (p - r)**2
    return (sum/len(predicted))**0.5
```
