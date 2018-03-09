## 线性回归
[原文链接](https://developers.google.com/machine-learning/crash-course/descending-into-ml/linear-regression)


## 训练与损失
**训练**模型表示通过有标签样本来学习（确定）所有权重和偏差的理想值。在监督式学习中，机器学习算法通过以下方式构建模型：检查多个样本并尝试找出可最大限度地减少损失的模型；这一过程称为**经验风险最小化**。
**损失**是对糟糕预测的惩罚。也就是说，损失是一个数值，表示对于单个样本而言模型预测的准确程度。如果模型的预测完全准确，则损失为零，否则损失会较大。训练模型的目标是从所有样本中找到一组平均损失“较小”的权重和偏差。

您可能想知道自己能否创建一个数学函数（损失函数），以有意义的方式汇总各个损失。

#### 平方损失：一种常见的损失函数
接下来我们要看的线性回归模型使用的是一种称为**平方损失**（又称为 **$L2$** 损失）的损失函数。单个样本的平方损失如下：
```
$
  = the square of the difference between the label and the prediction
  = (observation - prediction(x))2
  = (y - y')2
$
```

**均方误差 (MSE)** 指的是每个样本的平均平方损失。要计算 MSE，请求出各个样本的所有平方损失之和，然后除以样本数量：
$MSE = \frac{1}{N} \sum_{(x,y)\in D} (y - prediction(x))^2$

其中：
* (x,y)指的是样本，其中
    * x指的是模型进行预测时使用的特征集。
	* y 指的是样本的标签（例如，每分钟的鸣叫次数）。
* prediction(x)指的是权重和偏差与特征集 x 结合的函数。
* D指的是包含多个有标签样本（即 (x,y)）的数据集。
* N指的是 D 中的样本数量。

虽然 MSE 常用于机器学习，但它既不是唯一实用的损失函数，也不是适用于所有情形的最佳损失函数。

关键字
经验风险最小化|损失
----|----
均方误差|平方损失
训练

[原文链接](https://developers.google.com/machine-learning/crash-course/descending-into-ml/training-and-loss)