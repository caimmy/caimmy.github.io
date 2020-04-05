---
layout: post
title: "历史文献中的“态度”"
date: 2020-04-05 10:50:00
category: archaeology
tags: 在线系统 prehistory 定量 自然语言处理 词向量 文本分析
---

## 历史文献中的“态度”

> 近期在针对二十四史进行语料库建设，在训练词向量的过程中，发现针对同一个词，不同的文献训练出的相似词带有明显的情感
倾向，比较有意思，记录如下。

一、 文本整理与词向量训练

  本文中训练词向量采用的是python的gensim包，针对二十四史分别与公共新闻文本库混合进行训练。这样可以既可以满足训练所需要的
  大文本要求，又能避免不同历史文献同名词汇的相互干扰。训练过程采用了skip-gram 算法，窗口宽度为10，100维向量空间。词向量的
  概念此处不予详细解说，可参考 [word2vec][link_word2vec] 。
  
二、 不通文献对人物的态度
  汉代的历史人物，其人物事迹、历史形象为人们广为熟知，我尝试选取《汉书》、《后汉书》、《三国志》、《史记》四本书，对比研究几个主要
  历史人物的近似词，以期能够看出不同文本在叙述同一历史人物时在书写上的倾向性。
  
  1、刘邦
  
   《汉书》
   
   ![刘邦-《汉书》](/img/202004/hanshu_liubang_wv.png)
     
   [原始链接](https://www.prehistory.cn/nlp/word2vec?posword=%E5%88%98%E9%82%A6&negword=&book=%E6%B1%89%E4%B9%A6)
   
   《后汉书》
   
   ![刘邦-《后汉书》](/img/202004/houhanshu_liubang.png)
   
   [原始链接](https://www.prehistory.cn/nlp/word2vec?posword=%E5%88%98%E9%82%A6&negword=&book=%E5%90%8E%E6%B1%89%E4%B9%A6)
   
   《三国志》
   
   ![刘邦-《三国志》](/img/202004/sanguozhi_liubang.png)
   
   [原始链接](https://www.prehistory.cn/nlp/word2vec?posword=%E5%88%98%E9%82%A6&negword=&book=%E4%B8%89%E5%9B%BD%E5%BF%97)
   
   《史记》
   
   ![刘邦-《史记》](/img/202004/shiji_liubang.png)
   
   [原始链接](https://www.prehistory.cn/nlp/word2vec?posword=%E5%88%98%E9%82%A6&negword=&book=%E5%8F%B2%E8%AE%B0)  
     
     
[link_word2vec]: https://baike.baidu.com/item/Word2vec/22660840