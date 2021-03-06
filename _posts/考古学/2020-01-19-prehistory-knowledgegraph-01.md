---
layout: post
title: "历史文献与知识图谱 1"
date: 2020-01-19 16:49:00
category: archaeology
tags: 在线系统 prehistory 定量 人工智能 知识图谱
---

## 历史文献与知识图谱 1

> 知识图谱（Knowledge Graph），在图书情报界称为知识域可视化或知识领域映射地图，是显示知识发展进程与结构关系的一系列各种不同的图形，用可视化技术描述知识资源及其载体，挖掘、分析、构建、绘制和显示知识及它们之间的相互联系。

  
&emsp;&emsp;历史文献研究也是文本研究，基于自然语言处理的文本分析技术理所当然有用武地。作为尝试，作者在进行自然语言学习的过程中，尝试以《二十四史》为文本材料，进行知识图谱自动构建，并以自动构建的结果加以人工分析和校正。

&emsp;&emsp;系统首先通过神经网络模型（该模型的构建另文介绍），对翻译成现代白话文的《二十四史》文本进行检索，逐句进行分析，从单句中抽取简单的实体及关系，形成知识图谱三元组。自动抽取出的知识图谱三元组会存放在数据库中，等待进一步的人工审核。

&emsp;&emsp;需要改进的地方：
* 知识图谱的三元组抽取是个硬核算法，需要提升的空间很多，比如跨句联系上下文进行关系抽取、需要更高效更准确的进行命名实体识别、需要更丰富的自定义词典。。。；
* 知识图谱的UI呈现；
* 知识图谱和搜索引擎的配合工作；

&emsp;&emsp;目前配合着这个系统，我准备在2020年开始逐本通读《二十四史》，以校验知识图谱为目标，作为坚持阅读的动力。。。


<img style="align: center;" src="https://caimmy.github.io/img/202001/kn_sel1.jpg">


<img style="align: center;" src="https://caimmy.github.io/img/202001/kn_sel2.jpg">

<img style="align: center;" src="https://caimmy.github.io/img/202001/kn_sel3.jpg">