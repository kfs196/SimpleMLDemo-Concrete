# SimpleMLDemo-Concrete

一个基于Scikit-Learn和UCI混凝土抗压强度数据集的简单机器学习案例/ A Very Simple Machine Learning Case Based on Scikit-Learn and UCI Concrete Compressive Strength Dataset

### 项目简介：

* 由于通过传统方法由一定混凝土配合比去预测浇筑、养护完成后混凝土强度非常困难，目前国内外有大量学者在研究利用机器学习的混凝土强度预测的方法。本文将对UCI机器学习数据库中的相关公开数据进行预处理和初步的探索性分析，采用多元线性回归和CART方法训练模型，实现了对混凝土抗压强度这一关键指标进行预测，并对两种模型的性能进行简单评估。分析结果表明，CART模型相对于多元线性回归模型有更高的预测精度，但作为一种简单回归模型在复杂情况下仍无法满足实际需求，有待进一步优化提升。
* 其中，‘FinalReport1’文件主要进行了简单的数据预处理与探索性分析，‘FinalReport2’文件主要包括相关性分析、两种回归分析方法及模型的扩展应用。
* 本项目来源于作者研究生选修课程（数据分析入门类课程）的期末作业，目的是记录学习成果、方便今后参考，仅用于学习交流。其中的分析思路与方法尚存在许多不足之处，且存在理论上的不严谨处，有待持续学习进步。

### 补充说明：

* 整个分析过程中，用到的主要第三方模块及用途如下：

|   第三方库   | 子模块          | 主要用途                      |
| :----------: | --------------- | ----------------------------- |
|    Numpy    | ——            | 向量与矩阵运算、格式化存储    |
|    Pandas    | ——            | 表格化数据分析，基本统计描述  |
|  Matplotlib  | pyplot          | 图表绘制，结果可视化展示      |
|   Seaborn   | ——            | 特殊图表绘制：如热力图        |
|    Scipy    | stats           | 进行基本的相关分析与假设检验  |
|   IPython   | display         | 改善Jupyter环境的数据显示格式 |
| Scikit-Learn | model_selection | 进行训练集与测试集的随机划分  |
| Scikit-Learn | metrics         | 进行模型误差指标的计算        |
| Scikit-Learn | linear_model    | 进行线性回归分析(LR)          |
| Scikit-Learn | tree            | 进行回归决策树分析(CART)      |

* 本案例的数据来源于UCI Machine Learning Repository网站，采用了经典的混凝土抗压强度及坍落度数据集，具体网址如下：

|          数据集名称          | 网址                                                                 |
| :---------------------------: | -------------------------------------------------------------------- |
| Concrete Compressive Strength | http://archive.ics.uci.edu/dataset/165/concrete+compressive+strength |
|      Concrete Slump Test      | http://archive.ics.uci.edu/dataset/182/concrete+slump+test           |

* 由于Matplotlib默认不支持中文字体，因此需要进行配置，否则程序报错、图表异常。网上有许多配置教程，可自行搜索查看。在本案例中只需要修改每个Notebook文件的第一部分，即“0.导入必备的第三方库”中关于Matplotlib的配置即可，如下。一种采用指定字体画图的解决方案：[这里](https://huaweidevelopers.csdn.net/64d302cbecb00a6374e19620.html?dp_token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpZCI6MTA4MjczNywiZXhwIjoxNjk5ODgwNDg1LCJpYXQiOjE2OTkyNzU2ODUsInVzZXJuYW1lIjoid2VpeGluXzYzNDk1MTEzIn0.0XtZAwmQAaLUyhAX4tq-940kV_jh7BxNfXBNkAYh99s)。

```python
# 基本设置: Matplotlib中文字体与负号格式
config = {'font.family':'你的字体文件的系统英文名称'}
plt.rcParams.update(config)
plt.rcParams['axes.unicode_minus'] =False # 设置负号格式使其正常显示。
```

### 致谢：

* 特别感谢课程教师庄老师的悉心教导与帮助，一学期以来始终以细心、耐心、热心对待每一位同学，在此祝庄老师身体健康，工作顺利，科研硕果累累！
* 在完成本案例的同时参考了许多Github、Kaggle、CSDN等网站的教程与代码，无法一一列出，在此一并致谢！
