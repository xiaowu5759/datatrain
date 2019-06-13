# ndarray 数组的创建和变化

### ndarray对象的属性

![sp190612_130206](F:/PycharmProjects/datatrain/note/datatrain/images/sp190612_130206.png)

### ndarray 数组的元素类型

![sp190612_130515](F:/PycharmProjects/datatrain/note/datatrain/images/sp190612_130515.png)

![sp190612_130528](F:/PycharmProjects/datatrain/note/datatrain/images/sp190612_130528.png)

![sp190612_130539](F:/PycharmProjects/datatrain/note/datatrain/images/sp190612_130539.png)

ndarray 为什么要支持这么多中元素类型？

对比：Python语法仅支持整数、浮点数和复数3种类型

1. 科学计算设计数据较多，对存储和性能都有较高要求
2. 对元素类型精细定义，有助于Numpy合理使用存储空间并优化
3. 对元素类型精细化定义，有助于程序员对程序规模有合理评估

#### 非同质的ndarray对象

非同质ndarry对象无法有效发挥numpy优势



### ndarray 数组的创建

- 从python中的列表、元组等类型创建

当`np.array()`不指定dtype时，numpy会根据数据情况关联一个dtype类型

- 使用numpy中函数创建，如：arange,ones,zeros等

![sp190612_132157](.\images\sp190612_132157.png)

![sp190612_132633](.\images\sp190612_132633.png)

![sp190612_132745](.\images\sp190612_132745.png)

`linspace,endpoint=false`，最后一个元素是否在数组中

默认将元素类型，设置为浮点数，因为这是在科学计算中

- 从字节流（raw bytes）中创建ndarray数组
- 从文件中读取特定格式，创建ndarray数组



### ndarray数组的变换

对于创建后的ndarray数组之后，可以对其进行维度变换和元素类型变化

#### 维度变换

![sp190612_133253](.\images\sp190612_133253.png)

`.reshape`生成了一个新数组

#### 元素类型

- ndarray数组的类型变换使用`.astype`

`.astype()`方法一定会创建新的数组（原始数据的拷贝）

- ndarray数组向列表的转换

`ls = a.tolist()`



### ndarray数组的操作

操作包括索引和切片

索引：获取数组中特定位置元素的过程

**使用负数，从右到左的倒序查找**

切片：获取数组元素子集的过程

**3个冒号分割，起始编号（从0开始）：终止编号（不含）：步长**



- 一维数组的索引和切片：与python的列表类似
- 多维数组的索引：从0开始的
- 多维数组的切片：选取每个维度进行操作



### ndarray数组的运算

#### 数组与标量之间的运算

数组与标量之间的运算作用于数组的每个元素

`a.mean()`计算a的元素平均值的商

#### numpy的一元函数

![sp190612_135402](.\images\sp190612_135402.png)

![sp190612_135555](.\images\sp190612_135555.png)



#### numpy的二元函数

![sp190612_135802](.\images\sp190612_135802.png)