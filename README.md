# Challenge_14

---

## Maching Learning Trading Bot

Background
I am assuming the role of a financial advisor at financial advisory firm which constantly competes with the other major firms to manage and automatically trade assets in a highly dynamic environment. In recent years, my firm has heavily profited by using computer algorithms that can buy and sell faster than human traders. The speed of these transactions gave my firm a competitive advantage early on. But, people still need to specifically program these systems, which limits our ability to adapt to new data. I am thus planning to improve the existing algorithmic trading systems and maintain the firm’s competitive advantage in the market. To do so, I’ll enhance the existing trading signals with machine learning algorithms that can adapt to new data.

---

### Installation

import [Pandas](https://pandas.pydata.org/) as pd  - For data analysis and manipulation.
import [numpy](https://numpy.org/) as np - adding support for large, multi-dimensional arrays and matrices
from [pathlib](https://docs.python.org/3/library/pathlib.html) import Path - gives access to a directory and to import files
import [hvplot.pandas](https://hvplot.holoviz.org/) - for plot visualizations
import [Matplotlib](https://matplotlib.org/) as plt - Creates static, animated or/and interactive visualizations.
from [sklearn](https://hvplot.holoviz.org/) import svm - to enable machine learning

---

## Comparing the effects of tuning the trading algorithm

*Baseline model*

I used the support vector machine (SVM) learning method, support vector classification (SVC) with a short moving average window of 4 and a long moving average window of 100 with the first 3 months training dataset.

![plot_1_Cumm_Return](https://user-images.githubusercontent.com/101282610/191393893-c3674748-7799-4dbc-babc-8b68fad87cc5.png)
plot_1_Cumm_Return

*Model 2*

Did this new model perform better or worse than the provided baseline model? Did this new model perform better or worse than your tuned trading algorithm?
Using the DecisionTreeClassifier the predicted values were -1 and the graph looks very similar to that of the baseline model. Precision was very similar as well.

![plot_2_cumm_return](https://user-images.githubusercontent.com/101282610/191394862-1df9e181-dc37-4e65-9444-2fab17721dad.png)
plot_2_cumm_return

*Model 3*

What impact resulted from increasing or decreasing the training window?
When training increases to 12 months, the strategy is the same as holding the asset through the testing period. But since precision was halfed as well, it means that further into the future, there might be significant change. Also, we want to minimize the amount of training data used in other to reduce the noise.

![plot_3_cumm_return](https://user-images.githubusercontent.com/101282610/191395877-75b852a5-071a-437c-91e0-ef247d31f934.png)
plot_3_cumm_return

*Model 4*

What impact resulted from increasing or decreasing either or both of the SMA windows?
With a short moving average window of 100 we will get better results but by increasing and also decreasing both of the SMA windows, the original model would give better results. Most of the predicted values were -1 so the strategy comulative returns graph looks very similar.

![plot_4_cumm_return](https://user-images.githubusercontent.com/101282610/191396247-4f0eea05-5714-4b7b-ba3c-515c6c2a3461.png)
plot_4_cumm_return

---

## License
MIT
