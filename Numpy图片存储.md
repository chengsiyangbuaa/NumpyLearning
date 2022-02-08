# Numpy图片存储

## Numpy、数组和python数组的关系

### Numpy

Numpy是对数组的一个封装。通过封装，让数组具备了很多强大的功能。

支持大量的维度数组与矩阵运算，此外也针对数组运算提供大量的数学函数库。

### 数组

数组本质上是一个数据结构。

数组是一个容器，里面可以存放大量的（**相同**）元素。

优点是：支持**随机访问**，即访问数组内任何一个元素，所消耗的计算量（时间）都是相同的。

缺点是：**插入或删除**会消耗大量时间。

### python数组

可以存放不同类型元素的容器。

## a、b指向同一块内存区域

```python
b = np.array([[0,1,2,3],[4,5,6,7]],dtype=np.int16) #换成不同类型
a = b.reshape((4,-1))# a,b在内存中共享一块内存
```

![image-20220208143546225](http://tallestdaisy.oss-cn-beijing.aliyuncs.com/img/image-20220208143546225.png)

## a、b的维度有区别

**a；4*2**

**b：2*4**

![image-20220208144950414](http://tallestdaisy.oss-cn-beijing.aliyuncs.com/img/image-20220208144950414.png)

## 访问a[1]\[1]

![image-20220208145558367](http://tallestdaisy.oss-cn-beijing.aliyuncs.com/img/image-20220208145558367.png)

想要访问**a[1]\[1]**

![image-20220208145710758](http://tallestdaisy.oss-cn-beijing.aliyuncs.com/img/image-20220208145710758.png)

想要访问a[1]\[1]，我们就需要知道这个数据的地址，通过访问这个内存地址，才能取出这个数

![image-20220208150026909](http://tallestdaisy.oss-cn-beijing.aliyuncs.com/img/image-20220208150026909.png)

![image-20220208150145221](http://tallestdaisy.oss-cn-beijing.aliyuncs.com/img/image-20220208150145221.png)

## 思考题：访问b[1]\[2]的过程

## 思考题：为神魔，数组能够支持随机访问？

## 思考题：数组可不可以存放不同类型的元素？为神魔？

## 思考题：Numpy的数组ndarray，是否存储在连续的内存块中？