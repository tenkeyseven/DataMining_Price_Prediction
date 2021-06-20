# DataMining_Price_Prediction
本仓库为「🚀 掘地求生」组2021数据挖掘课程大作业项目地址
## 前期报告
### 问题描述

#### 1、问题背景及分析

房价是人民群众及其关注的热点以及重点问题，房价的走势关系着人民的生活以及社会的发展。因此，本小组从此出发点切入，利用数据挖掘相关技术和思想，对历年来北京市二手房房价进行搜集、分析和处理，利用相关算法对整理后的数据进行仔细分析和研究。最后，形成对北京市二手房数据的分析、可视化展示、以及利用相关算法（例如，将房价预测价格问题作为回归任务）对未来房价进行预测。

#### 2、问题描述

2.1 数据准备

本项目中的数据将从 [链家北京市二手房](https://bj.lianjia.com/ershoufang/) 网站中获取。数据基本包括以下几个属性：标题、地区名称、地址、成交价格、单价、年份、楼层、是否精装等。

2.2 准备采用的方法或模型

对数据分析任务来说：采用数据清洗、集中趋势分析、相关性分析等，最后可视化呈现。

对房价预测任务来说：前期采用线性回归方法对数据进行分析，结合效果再进行后续方法考虑。

2.3 预期的挖掘结果

获得较好的相关数据分析的可视化结果和房价预测模型。

### 项目评估

对房价预测模型：将采用以下评估标准

+ 平均绝对误差(MAE）
  MAE用来衡量预测值与真实值之间的平均绝对误差，MAE越小表示模型越好，其定义如下：

![[公式]](https://www.zhihu.com/equation?tex=%5Clarge%7BMAE%3D%5Cfrac%7B1%7D%7Bn%7D+%5Csum_%7Bi%3D1%7D%5En+%7Cy_i+-+%5Chat%7By%7D_i%7C%7D%2C%5C%3B%5C%3B%5Cin%5B0%2C%2B%5Cinfty%29%5C%3B%5C%3B%5C%3B%281%29+%5C%5C)

- 均方误差（MSE）
  MSE也许是回归中最普通的评价指标，MSE越小表示模型越好，其定义如下：

  ![[公式]](https://www.zhihu.com/equation?tex=%5Clarge%7BMSE%3D%5Cfrac%7B1%7D%7Bn%7D+%5Csum_%7Bi%3D1%7D%5En+%28y_i+-+%5Chat%7By%7D_i%29%5E2%2C%5C%3B%5C%3B%5Cin%5B0%2C%2B%5Cinfty%29%7D%5C%3B%5C%3B%5C%3B%282%29+%5C%5C)

+ 均方根误差（RMSE）
  RMSE是在MSE的基础之上开根号而来，RMSE越小表示模型越好，其定义如下：

![[公式]](https://www.zhihu.com/equation?tex=%5Clarge%7BRMSE%3D%5Csqrt%7B%5Cfrac%7B1%7D%7Bn%7D+%5Csum_%7Bi%3D1%7D%5En+%28y_i+-+%5Chat%7By%7D_i%29%5E2%7D%2C%5C%3B%5C%3B%5Cin%5B0%2C%2B%5Cinfty%29%7D%5C%3B%5C%3B%5C%3B%283%29+%5C%5C)

## 最终报告

最后形成的代码以及说明文件为：[lianjia_price_prediction.ipynb](./lianjia_price_prediction.ipynb)

其中包括以下大致内容：

+ 数据分析与可视化部分
+ 房价预测-链家数据读取
+ 抽取相关特征
+ 对房价数据进行预测
    + 使用线性回归方法
    + 使用决策树方法

项目结构说说明：
```bash
.
├── LICENSE
├── README.md
├── data
│   ├── lianjia1.csv
│   ├── lianjia2.csv
│   ├── lianjia3.csv
│   ├── lianjia4.csv
│   ├── lianjia5.csv
│   ├── lianjia6.csv
│   └── lianjia7.csv
├── lianjia_price_prediction.ipynb
├── processed_data
│   └── lianjia1.csv
└── utils
    ├── lianjia_data_mining.ipynb
    ├── lianjia_preprocess.ipynb
    ├── preprocess.ipynb
    └── visualization.ipynb

4 directories, 15 files
```
其中，主代码文件为：[lianjia_price_prediction.ipynb](./lianjia_price_prediction.ipynb); data、processed_data 文件夹中为我们可视化以及数据处理使用的数据; utils文件夹中为我们项目过程中进行部分测试时用到的代码，与最终主代码文件[lianjia_price_prediction.ipynb](./lianjia_price_prediction.ipynb)没有直接联系。

本项目使用以下库以及对应的版本 
```bash
python == 3.8
numpy == 1.19.2 
pandas == 1.2.3
sklearn  == 0.2.4

```