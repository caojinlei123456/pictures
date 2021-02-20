# pytorch 使用记录

## 1.preprocessing（预处理）

1. 创建一个Dataset对象，必须实现__len__()、**getitem**()这两个方法。
2. 创建一个DataLoader对象，它是对Dataset对象进行迭代。
3. 循环遍历这个Dataloader对象，将img，label加载到模型进行训练

```python
torch.utils.data
from .dataset import Dataset, TensorDataset, ConcatDataset, Subset, random_split
from .dataloader import DataLoader

dataset = MyDataset()           # 第一步：构造Dataset对象
dataloader = DataLoader(dataset)# 第二步：通过DataLoader来构造迭代对象
 
num_epoches = 100
for epoch in range(num_epoches):# 第三步：逐步迭代数据
    for img, label in dataloader:
        # 训练代码
```

## 2.moduls(模型)

## 3.utils（工具包）

### 3.1 Loss

### 3.2 optim

### 3.3 Logger

### 3.4 torchsummary

## 4. train（训练）

## 5. test（测试）

## 问题记录

### 1.1 requires_grad

```
requires_grad ： tensor判断是否需要保留梯度信息，默认不保留，在反向传播中会进行相应计算。
```

### 1.2 Con1d和ConvTranspose1d的计算公式(参考笔记)

### 1.3 优化器（Adam,SGD）

#### **Adam**

**优点**

1. 收敛速度快，尤其擅长处理稀疏数据。
2. 如果不确定，直接上Adam

**缺点**

1. 可能不收敛
2. 可能无法获取全局最小值

#### SGD

较为容易的收敛到全局最优点，但收敛速度较慢

> 因此现在会有前期Adam+后期SGD的操作

