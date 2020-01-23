## Set up

## Memo

- Juypter Notebookで補完ってできないの...？
- JupyterLabというのがあるらしい
- VSCodeでもできるっぽい？

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
