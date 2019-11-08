# My first share project of nlp

## that's cool!

## onehot编码
onehot本质上属于词典模型，最终一句话的向量维数是词袋中词的总数，假设有几句话：

1. 我爱中国
2. 爸爸妈妈爱我
3. 爸爸妈妈爱中国
首先，将语料库中的每句话分成单词，并编号：

1：我      2：爱      3：爸爸      4：妈妈      5：中国

然后，用one-hot对每句话提取特征向量：

![onehot](https://github.com/opprash/braveRL/blob/master/datas/one_hot.png)

所以最终得到的每句话的特征向量就是：

1. 我爱中国 -> 1，1，0，0，1
2. 爸爸妈妈爱我 -> 1，1，1，1，0
3. 爸爸妈妈爱中国 -> 0，1，1，1，1

## tfidf提取特征
TF-IDF（term frequency–inverse document frequency，词频-逆向文件频率）是一种用于信息检索（information retrieval）与文本挖掘（text mining）的常用加权技术。
1. TF-IDF是一种统计方法，用以评估一字词对于一个文件集或一个语料库中的其中一份文件的重要程度。字词的重要性随着它在文件中出现的次数成正比增加，但同时会随着它在语料库中出现的频率成反比下降。
2. TF-IDF的主要思想是：如果某个单词在一篇文章中出现的频率TF高，并且在其他文章中很少出现，则认为此词或者短语具有很好的类别区分能力，适合用来分类。
* TF是词频(Term Frequency)   
词频（TF）表示词条（关键字）在文本中出现的频率。
这个数字通常会被归一化(一般是词频除以文章总词数), 以防止它偏向长的文件。
tf_ij=n_ij/(Σ_k n_(k,j) )

