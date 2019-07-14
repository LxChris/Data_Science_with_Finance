# Data Science with Finace
---
Original Contributor:
- Jhansi Nair
- Kanika Nama
- Lixi Zhou
- Ramit Jaal
- Yin Li
- Yixuan Wang

---
## Optimize the structure of the class project
---
**Reorganizer: Lixi Zhou**

**Note:**

Because pyplot is not supported in GitHub yet. Please use the link below to review the Jupyter Notebook.

**Part 1**

https://nbviewer.jupyter.org/github/LxChris/Data_Science_with_Finance/blob/master/Part1_Basic_Analysis.ipynb

**Part 2**

https://nbviewer.jupyter.org/github/LxChris/Data_Science_with_Finance/blob/master/Part2_SVR_OLS_With_Trading.ipynb

**Part 5**

https://nbviewer.jupyter.org/github/LxChris/Data_Science_with_Finance/blob/master/Part5_Pair_Trading.ipynb

---

**Ideal structure of project**
- [x] Part1_Basic_Analysis
- [x] Part2_SVR_LinearRegression
- [ ] Part3_GARCH_FAMAFRECH
- [ ] Part4_RandomForest
- [x] Part5_PairTrading
- [ ] Part6_PredictModel_TradingAlgorithm
- [ ] Write a report
---
## Update History
- 05/01/2019: Start this project. Planning. 
- 05/02/2019: Add Part1_Basic_Analysis. ETA: 05/03/2019。
  - Requirements:
    - [x] 1. Underscore is not allowed in a variable name, and it is only allowed in dataFrame.
    - [x] 2. Detailed the comment, arguments and return.
    - [x] 3. Plot share price data and then normalized it. Calcuklate the change rate for each data. Check whether breaking news would have a huge impact o share price. 
    - [x] 4. Explorer `Januaray Effect`. Use the histogram to summarize the change rate.
- 05/03/2019: Add `fig` folder to store figure used in jupyter notebook. Comments for each function have been added. Basic_Analysis ETA: 05/04/2019.
- 05/04/2019: `Basic_Analysis` Done。Next targets：GARCH model and the Fama-French model.
  - Requirements：
    - [ ] 1. GARCH  **Postponed**.
    - [ ] 2. Kalman Filter  **Postponed**.
- 05/09/2019: Make **OLS and SVR part as a higher priority**, start`Part2_SVR_Linear Regression`, by applying new indexing methods, the performance of code was improved a lot. The time cost of a function reduced from the 40s to 10s. Refactor time window function, make it more powerful. To-Do:
    - [x] Finish SVR and Linear Regression Part。
    - [x] Finish comments。
    - [x] Build trading algorithm with model built。
    - [x] `makePrediction()` Refactor the input of model.
    - [x] `makePrediction()` Determined that the function would return a model, so it can be used for further consideration.
    - [x] `makePrediction()` Detailed the help for the function.
    - [x] Optimize the model 
- 05/10/2019: Finish the refactor of makePrediction function. Help text still needs to be done. Features selecting, t-test and RMSE calculating are done.
- 05/23/2019: Improved efficiency of for loop. Build a trading strategy. Finished the trading algorithm part and plot a nice graph. Next Period requirement:
    - [x] Sharpe ratio analysis
    - [x] Sortino ratio analysis
- 05/28/2019: Fixed a critical bug that may result in the model failed. **As a result of it: the model did not play very well.** Create a function to calculate the hit rate for the model prediction. For now, this hit rate only reaches **52%**. It is a very bad model.
- 07/06/2019: Update `Pair_Trading`, select the most matched stock and built the trading algorithm. Beta version is done. Known issues to be fixed:
  - [x] The model is based on historical data not use input data as a stream to feed the model. Need to refactor as `OLS_SVR_model` use historical data to train a model and take action based on next day's open price.
  - [x] Comments clear.
- 07/08/2019: Update `Pair_Trading`, fixed known issues. Correct the predicting model. Use real cash to plot the return graph.
- 07/13/2019: Finish `Pair_Trading` part, update streaming data model, optimize `action` model for making actions to avoid unncessary signal. The performance of the model is not very well. Only **20%** profit for three years. If a user only holde Amazon share without selling, he can earn **200%** profit. Next step:
  - [ ] Change timewindow to optimize the model.
  - [ ] Change the threshold to optimize the model.
- 07/14/2019: Add risk analysis for `Part5`.
  - [ ] Add risk analysis for `Part2`.

