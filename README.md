# CRFExample

在自然语言处理中，一个非常常见的任务就是从一个给定的句子或者段落中抽取出特定类型的词或短语。比如判定实体名称（人名、地名、单位名等），或者是识别词性（名词、动词、形容词、副词等）。

这个问题叫做序列标注(sequance labeling),简单讲就是输入一个句子或段落，由识别模型给其中每一个词或短语打一个标签。CRF模型的一个常见应用就是做这类识别模型。

我们的CRFExample就是训练一个CRF模型，用它来识别文本中哪些词/短语属于一个名称（人名、地名、单位名等）。如果这个词是一个名称的一部分就将其标识为“N”，否则标为“I”。


比如我们要判定这句话:"Paxar Corp said it has acquired Thermo-Print."

转换成输入: input = ["Paxar", "Corp", "said", "it", "has", "acquired", "Thermo-Print"]
再用CRF模型predict得到结果: output = ["N", "N", "I", "I", "I", "I", "N"]

# 下载
git clone 或 download 本repository 

# module安装

pip install bs4

pip install nltk

pip install python-crfsuite

# 运行
python crf.py
