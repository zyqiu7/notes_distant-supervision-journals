# Distantly Supervised NER with Partial Annotation Learning and Reinforcement Learning
命名实体识别 NER/远程监督/局部标注问题/强化学习

## 摘要
- 远程监督：如果文本中的字符串包含在预定义的实体字典中，则该字符串可能是一个实体
- 远程监督当下的主要问题：不完全标注（incomplete annotation），噪声标注（noisy annotation）
- 本文解决思路：局部标注学习（Partial Annotation Learning）——不完全标注问题；  
基于强化学习的实例选择（Instance Selector）——噪声标注问题

## 引言
- **过往文献综述中 深度学习NER常用步骤（Standardlized Steps）**:
  1. BiLSTM——Encoding
  2. CRF——Jointly Label Decoding
  3. 附加步骤：BiLSTM和CNN——字/词级别表示（word-level representation）  
  
- 之前的NER集中关注一些预定义的标注实体类型，但现在不同领域都出现了大量无人工标注的新实体类型，人工标注将花费大量精力
- Mintz（2009）最早提出远程监督？  
-  ** 本文方法**
  目的： 无人工标注新命名实体类型，如——商品（PDT）等
  1. 

