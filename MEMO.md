## Set up

```
$ jupyter notebook
```

## Memo

- Juypter Notebookで補完ってできないの...？
- JupyterLabというのがあるらしい
- VSCodeでもできるっぽい？

## Steps

- データを集める
- 前処理
- 分析
- 評価
- 考察

- とりあえずdataFrameに打ち込む
- データをちゃんと読む
- グラフとかにして関係をみてみる

## Snippets

<details>
<summary>import libs</summary>

```py
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
%matplotlib inline
import seaborn as sns
```
</details>

## Methods / Property

### sklearn

<details>
<summary>data.DESCR</summary>

```py
from sklearn.datasets import load_boston
boston = load_boston()
print(boston.DESCR)
```
</details>

<details>
<summary>linerRegression.fit</summary>

```py
lr = LinearRegression()

x_column_list = ['RM']
y_column_list = ['PRICE']

data_boston_x = data_boston[x_column_list]
data_boston_y = data_boston[y_column_list]

lr.fit(data_boston_x, data_boston_y)
```
</details>

<details>
<summary>linerRegression.coef_</summary>

```py
print(lr.coef_)
```
</details>

<details>
<summary>linerRegression.intercept_</summary>

```py
print(lr.intercept_)
```
</details>

### pandas

<details>
<summary>pd.DataFrame</summary>

```py
data_boston = pd.DataFrame(boston.data, columns=boston.feature_names)
data_boston['PRICE'] = boston.target
```
</details>

<details>
<summary>dataFrame.head</summary>

```py
data_boston.head()
data_boston.tail()
```
</details>

### seaborn

<details>
<summary>sns.jointplot</summary>

```py
sns.jointplot('RM', 'PRICE', data=data_boston)
```
</details>

<details>
<summary>sns.pairplot</summary>

```py
sns.pairplot(data_boston, vars=['PRICE', 'RM', 'DIS'])
```
</details>
