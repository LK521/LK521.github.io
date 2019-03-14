---
layout: post
title:  "Python Feature List Comprehensions"
date:   2019-03-14 15:00
categories: python
permalink: /archivers/language
---

# Python 特性：列表生成式

python语言中内置了一种特殊的生成列表的方法叫列表生成式。

要生成列表[1，4，9，16，25]，简单的方法是：

```
list = []
for i in range(1,6):
    list.append(i*i)
```
使用for循环来进行生成列表所用的代码较多，比较麻烦，列表生成式只用一行：
```
[i*i for i in range(1,6)]
```
列表生成式的写法有3种：
1.单个for循环
```
[i*i for i in range(1,6)]
>>[1,4,9,16,25]
```
```
temp = {'1':'A','2':'B','3':'C'}
[x +'='+ y for k,v in temp.items()]
>>['1 = A','2 = B','3 = C']
```
2.for与if结合
```
[i for i in range(1,6) if i % 2 == 0]
>>[4,16]
```
3.2个for循环
```
[x + y for x in 'ABC' for y in 'XYZ']
['AX','AY','AZ','BX','BY','BZ','CX','CY','CZ']
```

两层的循环使用列表生成器逻辑十分清晰，多层的就比较复杂，不建议使用

