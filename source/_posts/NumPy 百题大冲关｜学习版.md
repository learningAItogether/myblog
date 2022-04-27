---
title: Blog模板 | NumPy 百题大冲关｜学习版
data: 
tage: Github
---

---

#### 介绍

NumPy 是 Python 语言的一个第三方库，其支持大量高维度数组与矩阵运算。此外，NumPy 也针对数组运算提供大量的数学函数。机器学习涉及到大量对数组的变换和运算，NumPy 就成了必不可少的工具之一。NumPy 百题大冲关分为基础篇和进阶篇，每部分各有 50 道练习题。基础部分的练习题在于熟悉 NumPy 常用方法的使用，而进阶部分则侧重于 NumPy 方法的组合应用。

---

<div class="alert alert-info"><p>本次实验为 Notebook 实验，前后单元格之间有关联性，你需要按顺序执行单元格，跳跃或重复执行部分单元格可能会造成赋值混乱。</p></div>

### 基础部分

练习 NumPy 之前，首先需要导入 NumPy 模块，并约定简称为 `np`。

<i class="fa fa-arrow-circle-down" aria-hidden="true"> 教学代码</i>：

**1. 导入 NumPy：**


```python
import numpy as np
```

<i class="fa fa-arrow-circle-down" aria-hidden="true"> 动手练习</i>｜如果你对课程所使用的蓝桥云课 Notebook 在线环境并不熟悉，可以先学习
[<i class="fa fa-external-link-square" aria-hidden="true"> 使用指南课程</i>](https://www.lanqiao.cn/courses/1322)。

### 创建数组

Min-Max 标准化公式：

$$Y = \frac{Z-\min(Z)}{\max(Z)-\min(Z)}$$


```python
# 根据公式定义函数
def l2_normalize(v, axis=-1, order=2):
    l2 = np.linalg.norm(v, ord=order, axis=axis, keepdims=True)
    l2[l2 == 0] = 1
    return v/l2

# 生成随机数据
Z = np.random.randint(10, size=(5, 5))
print(Z)

l2_normalize(Z)
```

    [[4 0 9 4 1]
     [7 5 9 8 0]
     [7 6 6 7 7]
     [6 8 3 4 2]
     [4 5 1 2 8]]
    




    array([[0.37463432, 0.        , 0.84292723, 0.37463432, 0.09365858],
           [0.47301616, 0.33786869, 0.60816364, 0.5405899 , 0.        ],
           [0.47301616, 0.40544243, 0.40544243, 0.47301616, 0.47301616],
           [0.52827054, 0.70436073, 0.26413527, 0.35218036, 0.17609018],
           [0.38138504, 0.47673129, 0.09534626, 0.19069252, 0.76277007]])




```python
Z = np.array([
    [1, 2, 1, 9, 10, 3, 2, 6, 7],  # 特征 A
    [2, 1, 8, 3, 7, 5, 10, 7, 2],  # 特征 B
    [2, 1, 1, 8, 9, 4, 3, 5, 7]])  # 特征 C

np.corrcoef(Z)
```




    array([[ 1.        , -0.05640533,  0.97094584],
           [-0.05640533,  1.        , -0.01315587],
           [ 0.97094584, -0.01315587,  1.        ]])



<div style="font-size:14px; line-height:17px;" class="hljs">
         [A]     [B]     [C]
array([[ 1.  , -0.06,  0.97]   [A]
       [-0.06,  1.  , -0.01],  [B]
       [ 0.97, -0.01,  1.  ]]) [C]
</div>

<hr><div style="color: #999; font-size: 12px;"><i class="fa fa-copyright" aria-hidden="true"> 本课程内容版权归蓝桥云课所有，禁止转载、下载及非法传播。实验中少量题目编译自：<a href="https://github.com/rougier/numpy-100">100 numpy exercises</a></i></div>


```python

```
