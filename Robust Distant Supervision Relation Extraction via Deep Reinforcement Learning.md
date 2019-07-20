# 基于深度强化学习的远程监督关系提取  
北邮，UCSB

## 对抗远程监督噪声相关工作
- 远程监督已成为关系提取中的标准步骤， 但远程监督标注的样本通常非常嘈杂。  
为对抗噪声，近期文献中常用方法有：
  1. 选择关于同实体对的句子集合中最正确的一句（select onebest sentence)
  [Lin,2016, Neural relation extraction with selective attention over instances]
  2. 计算关于某些特定（误报？）实体对的句子集合的软注意力权重(calculate soft attention weights over a set of sentences about a specific entity pair）  
  [Lin, 2014/2015, Relation classification via convolutional deep neural network/Distant supervision for relation extraction via piecewise convolutional neural networks]
  3. 多关系联合训练(a model to jointly learn with multiple relations)  
  [Hoffman,2011, Knowledge- based weak supervision for information extraction of overlapping relations]
  4. 多实例多关系学习(a multi-instance multi-label learning framework)  
  [Surdeanu, 2012, Multi-instance multi-label learning for relation extraction] 
  5. 结合外部知识丰富实体对表达，提高注意力权重准确度（combine the external knowledge to rich the representation of entity pair, to improve the accuracy of attention weights）  
  [Ji,2017,Distant supervision for relation extraction with sentence-level attention and entity descriptions]
  6. **本文方法**： 通过评估关系分类器在喂入这些远程监督标注的例子的性能，使用无监督的强化学习鉴别标注的反正例（FP），并将这些例子重新归为反例（TN）。
