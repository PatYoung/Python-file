# Python-file

## [collect_all](https://github.com/PatYoung/Python-file/tree/master/collect_all)计算如下描述:

### 描述

有*total_number*种牌，抽到每种的概率相同，从中挑选出*select_number*种想要的牌，计算抽$n$次牌，收集齐这*select_number*想要的牌的概率$P(T=n)$

### 思路

第$n$次抽到牌需为*select_number*种中的一种，且不在前$n-1$次出现。同时前$n-1$次需抽到其他*select_number-1*种想要的牌。
这里令*total_number* $=N$，*select_number* $=m$

假设$A_{i}$表示前$n-1$次为未抽到想要的$m-1$中的第$i$种牌。那么同时前$n-1$次需抽到其他$m-1$种想要的牌的概率应为：

$1-P(所有A_{i}的交集)$，利用容斥恒等式，且知，

$$P(A_{1}A_{2}...A{k}) = (1-\frac{k}{N-1})^{n-1}$$

便可计算$P(T=n)$

## [2.5](https://github.com/PatYoung/Python-file/tree/master/2.5)描述:
有黑桃♠、红桃♥、梅花♣、方片♦四个种类的牌。随机抽一张，计算它与当前选中牌为相同花色的平均抽牌次数。
该次数应为：

$$\frac{1}{4}\times(1+2+3+4) = 2.5$$