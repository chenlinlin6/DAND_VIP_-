## 导航

知识点

### Numpy

**NumPy** 是 *Numerical Python* 的简称，它是 Python 中的科学计算基本软件包。NumPy 为 Python 提供了大量数学库，使我们能够高效地进行数字计算。

2. Numpy简介

了解Numpy是python的一个非常高效的科学计算库。

下载anaconda，查看Numpy的版本。

3. 为何要使用Numpy

- 节约内存
- 多维数组结构数据可以用来完成如机器学习和数据分析的任务
- 大量的内置数学函数

4. 创建和保存Numpy ndarray

> ndarray就是n维数组的意思。
>
> 导入numpy的方式：`import numpy as np`
>
> 创建Numpy的两种方法：
>
> 1.传入Python内置列表
>
> ```python
> arr=np.array([1, 2, 3, 4])
> ```
>
> 保存和加载`numpy array`
>
> 保存和加载`numpy array`使用`save`和`load`方法
>
> 请在ipython中练习
>
> ```python
> #保存数组
> np.save('my_arr', arr)
> #加载已经保存的数组
> ​```上述代码将 x ndarray 保存到叫做 my_arr.npy 的文件中。你可以使用 load() 函数将保存的 ndarray 加载到变量中。```
> arr_load=np.load('my_arr.npy')
> ```



5. 使用内置函数创建ndarray

> numpy有许多内置的函数可以用来生成特定的ndarray，这部分函数需要传入一个重要参数`shape`，也就是生成的数组的形状，你可以理解为你要生成多少行(n)，多少列(m)的一个数组？`shape`用`(n, m)`表示
>
> 这部分方法有：
>
> - `np.zeros()`生成都是0的数组
> - `np.ones()`生成都是1的数组
> - `np.full()`填充数组
> - `np.eye(N)`创建单位矩阵
> - `np.diag()`创建对角矩阵
> - `np.arange()`和`np.linspace()`创建连续数字的数组，`reshape(shape)`对创建的数组进行改变形状
> - `np.random.randint(start, stop, size = shape)`生成随机的整数数组
> - `np.random.normal(mean, standard deviation, size=shape)` 会创建一个高斯分布的 ndarray

6. 练习：创建ndarray

在这小节当中将上述学到的知识点练习一下，看一下返回的结果。

7. 访问和删除ndarray中的元素及向其中插入元素🌟🌟🌟

> 在这小节当中，掌握以下几个部分：
>
> **索引**
>
> 对一维的numpy ndarray索引可以用`arr[n]`的方式，对二维的numpy array索引可以用`arr[n][m]`的方式，三维及以上以此类推。
>
> **追加**
>
> `np.append(ndarray, elements, axis)` 函数向 ndarray 中附加值
>
> 请在ipython中练习 
>
> ```python
> # We create a rank 1 ndarray 
> x = np.array([1, 2, 3, 4, 5])
> # We append the integer 7 and 8 to x
> x = np.append(x, [7,8])
> ```
>
> `np.insert(ndarray, index, elements, axis)` 函数向 ndarray 中插入值，类似于`append`，只不过`append`是在尾部追加，而`insert`在我们指定完`index`的位置以后可以在中间插入。
>
> `np.vstack()`和`np.hstack()`对numpy array进行垂直方向和水平方向的堆叠

8. ndarray切片

>  三种类型的切片
>
> ```python
> ndarray[start:end]
> ndarray[start:]
> ndarray[:end]
> ```

9. 布尔型索引、集合运算和排序🌟🌟

>  上一节我们了解了怎么样去索引特定位置的numpy ndarray。但有时候我们想根据条件去筛选特定的数据，比如大于10并且小于20的数据。这个时候我们就需要加入逻辑判断，逻辑判断的条件返回的是True或者是False，是对数值的判断是否满足筛选条件。
>
> 请在ipython中练习
>
> ```python
> a=15
> print((a>10)&(a<20))
> ```
>
> 返回的结果是什么？以上就是一个对a的逻辑判断，`&`是连接两个条件的符号。其逻辑判断与python基础当中的逻辑判断条件是一样的，我们可以把它加入到对numpy ndarray的索引当中。
>
> 请在ipython中练习
>
> ```python
> # We create a 5 x 5 ndarray that contains integers from 0 to 24
> X = np.arange(25).reshape(5, 5)
> # We use Boolean indexing to assign the elements that are between 10 and 17 the value of -1
> X[(X > 10) & (X < 17)] = -1
> ```

10. 练习：操纵ndarray

> 该部分对前面的条件筛选进行训练。

11. 算术运算和广播

> 广播是什么意思？
>
> 初学numpy array的同学可能不太明白`广播`这个词是如何理解。
>
> 其实我们可以想象一个场景，在学校学生做广播体操的时候，学生是不是拍成一个大的方方正正的矩阵？随着广播的命令，每一排的学生或者是每一列的学生依次进行广播的命令进行相同的操作。numpy array的每个元素就类似于广播体操里面的学生，而我们将一个函数比如`np.add(X, Y)`应用到`X`和`Y`上，就相当于下达一个命令，`X`和`Y`里面的元素就会乖乖按照指令，站到对应的位置进行相加。当然，我们很多时候都会指定`axis=0`还是`axis=1`，来说明是对行进行操作还是对列进行操作。所以，广播是对所有元素进行相同操作的一个意思。
>
> 请在ipython中练习
>
> ```python
> # We create two rank 2 ndarrays
> X = np.array([1,2,3,4]).reshape(2,2)
> Y = np.array([5.5,6.5,7.5,8.5]).reshape(2,2)
> 
> # We print X
> print()
> print('X = \n', X)
> 
> # We print Y
> print()
> print('Y = \n', Y)
> print()
> 
> # We perform basic element-wise operations using arithmetic symbols and functions
> print('X + Y = \n', X + Y)
> print()
> #尝试一下传入axis=0和axis=1的差别是什么
> print('add(X,Y) = \n', np.add(X,Y))
> print()
> print('X - Y = \n', X - Y)
> print()
> print('subtract(X,Y) = \n', np.subtract(X,Y))
> print()
> print('X * Y = \n', X * Y)
> print()
> print('multiply(X,Y) = \n', np.multiply(X,Y))
> print()
> print('X / Y = \n', X / Y)
> print()
> print('divide(X,Y) = \n', np.divide(X,Y))
> ```
>
> 对`单个元素进行运算`这部分对照该节知识点进行训练。



12. 练习：通过广播创建ndarray

> 这个练习将上面的广播进行训练，注意axis参数。

13. 为迷你项目做准备

> 推荐安装anaconda，参考"(选修)安装anaconda"部分。

14. 迷你项目：均值标准化和数据分离

> 为什么要进行均值标准化？
>
> 所有数据采用相似范围的值，才能够使得机器学习算法正常工作，你可以想象，如果我们想用同一个模型来分析巨人和正常人类的身高，如果我们不标准化的话，巨人与巨人的差别是不是在人类看来是很大的？但是标准化以后，有点类似于将巨人按照它们的比例缩小了，这样就可以跟人类身高的分布进行一个类比，看是不是巨人社会的身高分布与人类是一样的，同时缩放后的巨人身高也不会对模型造成很大的影响。
