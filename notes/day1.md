什么是（监督式）机器学习？简单来说，它的定义如下：
* 机器学习系统通过学习如何组合输入信息来对从未见过的数据做出有用的预测。

#### 标签
在简单线性回归中，标签是我们要预测的事物，即 y 变量。标签可以是小麦未来的价格、图片中显示的动物品种、音频剪辑的含义或任何事物。

#### 特征
在简单线性回归中，**特征**是输入变量，即**x**变量。简单的机器学习项目可能会使用单个特征，而比较复杂的机器学习项目可能会使用数百万个特征，按如下方式指定：
$${x_1,x_2,...x_N}$$

在筛选垃圾邮件的示例中，特征可能包括：
* 电子邮件文本中的字词
* 发件人的地址
* 发送电子邮件的时段
* 电子邮件中包含莫名其妙的短语(例如：“一种奇怪的把戏”)

#### 样本
**样本**是指数据的特定实例：x。(我们采用粗体**x**表示它是一个矢量。)我们将样本分为以下两类：
* 有标签样本
* 无标签样本

**有标签样本**同时包含特征和标签。即：
$$labeled examples: {features, label}: (x, y)$$

我们使用有标签的样本来训练模型。在我们的垃圾邮件检测示例中，有标签样本是用户明确标记为“垃圾邮件”或“非垃圾邮件”的各个电子邮件。

**无标签样本**包含特征，但是不包含标签。即：
$$unlabeled examples: {features, ?}: (x, ?)$$

在使用了有标签样本训练了我们的模型之后，我们会使用该模型来预测无标签样本的标签。在垃圾邮件检测示例中，无标签样本是用户尚未添加标签的新电子邮件。

#### 模型
模型定义了特征与标签之间的关系。例如，垃圾邮件检测示例中的模型可能会将某些特征与“垃圾邮件”紧密联系起来。重点介绍一下模型生命周期的两个阶段：
* **训练**表示创建或**学习**模型。也就是说，您向模型展示有标签样本，让模型逐渐学习特征与标签之间的关系。
* **推断**表示将训练后的模型应用于无标签样本。也就是说，您使用训练过后的模型来做出有用的预测（`y`）。

#### 回归与分类
**回归**模型可预测连续值。例如，回归模型做出的预测可回答如下问题：
* 用户点击此广告的概率是多少

**分类**模型可预测离散值。例如，分类模型做出的预测可回答如下问题：
* 某个制定电子邮件是垃圾邮件还是非垃圾邮件
* 这是一张狗、猫还是仓鼠的图片

## 关键词
分类模型|样本
----|----
特征|推断
标签|模型
回归|训练



[原文链接](https://developers.google.com/machine-learning/crash-course/framing/ml-terminology)