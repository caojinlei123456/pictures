# NER

[toc]



## 背景

NER是NLP中的一项基础性关键任务，是信息提取的一个子任务，旨在将文本中的命名实体定位并分类为预先定义的类别。**NER可以看作词法分析中未登录词识别的一种，是未登录词中数量最多、识别难度最大、对分词效果影响最大问题。**同时NER也是信息抽取、信息检索、知识图谱、机器翻译、问答系统等诸多NLP任务必不可少的组成部分。

NER所涉及的实体一般包括3大类（实体类，时间类，数字类）和7小类（人名、地名、组织机构名、时间、日期、货币。百分比）





### 应用

![img](https://image.jiqizhixin.com/uploads/editor/2081f585-7937-4d76-82de-6f71feca93bb/1535688372832.png)

早期会用HMM,CRF等方法进行训练，现在基本都是采取DL-CRF模型做序列标注，最新的可能是bert类+CRF

其中最近点的应用时BiLSTM+CRF/IDCNN+CRF



## 参考链接

- [达观数据](https://www.jiqizhixin.com/articles/2018-08-31-2)
- [知乎](https://zhuanlan.zhihu.com/p/56085975)

