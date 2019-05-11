# Data Science with Finace
---
Contributor:
- Jhansi Nair
- Kanika Nama
- Lixi Zhou
- Ramit Jaal
- Yin Li
- Yixuan Wang

---
## 课程PROJECT整理大行动
---
**Reorganizer: Lixi Zhou**

**Note:**

Because pyplot is not supported in GitHub yet. Please use the link below to review the Jupyter Notebook.

**Part 1**
https://nbviewer.jupyter.org/github/LxChris/Data_Science_with_Finance/blob/master/Part1_Basic_Analysis.ipynb

**Part 2**
https://nbviewer.jupyter.org/github/LxChris/Data_Science_with_Finance/blob/master/Part2_SVR_OLS_With_Trading.ipynb
---

**TO-DO LIST**
- [x] Basic_Analysis Notebook
- [ ] 整理data
- [ ] 重新编排ipython notebook
- [ ] 整理Report
- [ ] 遵循已有的工程经验
- [ ] 整理出Report
- [ ] Make it public, 封装data

---
## Update History
- 05/01/2019: 此项目开坑，预计2周内完成整理工作，存入原始数据，列出初步的计划。
- 05/02/2019: 添加Part1_Basic_Analysis.进行初步工作。该任务预计完成时间05/03/2019。
  - 需求:
    - [x] 1. 规范变量的命名，驼峰规则，变量名不使用下环线，仅在数据表中允许使用下划线来当列名。
    - [x] 2. 每个函数的注释，统一格式，需要介绍函数功能，输入参数和返回值。
    - [x] 3. 一开始对股票的走势用图标列出，然后使用归一化，计算每天的波动率/收益率来查找异常点，通过查新闻来看当天是否发生了什么重大事情，导致股价有比较明显的异常波动。
    - [x] 4. 美国的`Januaray Effect`类似于国内的金九银十，然后统计每天的收益率，使用柱状图来进行统计。
    - [x] 5. 大部分内容都在之前的Notebook上，需要整理。
- 05/03/2019: 添加`fig`文件夹用来存储图片，增长率对比图和增长率柱状图统计已经实现。函数已经规范化，有注释，注释也已经规范化。具体进度查询土豆泥项目组进度管理。Basic_Analysis预计05/04能够完成。
- 05/04/2019: `Basic_Analysis`部分完成。下一阶段：GARCH模型，Kalman Filter模型。
  - 需求：
    - [ ] 1. GARCH  **延期**。
    - [ ] 2. Kalman Filter  **延期**。
- 05/09/2019: 开工`Part1_SVR_Linear Regression`，通过优化在存储数据时索引的方式，大大优化了程序的效率，模型的训练预测过程由40s缩减到10s左右。重构了移动窗口预测代码，并且使其更加通用化，以后即可调用同一个API即可实现相同的操作。精简代码结果。 To-Do:
  - [x] Finish SVR and Linear Regression Part。
  - [x] Finish comments。
  - [ ] Build trading algorithm with model built。
  - [x] `makePrediction()`函数的feature和target需要修改形式，转为传入feature还不是DataFrame。`出于和常用的模型函数的参数输入输出，保留feature和target传入的是dataframe的设定，且这里是引用不是hard copy`
  - [x] `makePrediction()`决定函数返回的是模型，这样在后面可以对模型的数据进行操作。
  - [ ] `makePrediction()`函数的介绍部分需要完善。
  - [x] 模型优化
- 05/10/2019: 完成了makePrediction的重构，help部分仍需要完善。完成了特征的选择部分，t-test和RMSE的计算。