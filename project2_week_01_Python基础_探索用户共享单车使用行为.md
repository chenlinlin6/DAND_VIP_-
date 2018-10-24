

学习地图：

- 为什么要学习Python
- python编程入门

学习方法

- 如果你是学习新手
  - 不妨跟着视频学习，并且多动手
- 如果你已经有了一定的编程基础
  - 可以看一下文字的教程，并且动手做一下编程题，有问题再去查找解决方案

### 第2节 数据类型和运算符

按照课时2.1-2.30了解基本的概念即可。运算符参照一般的数学表达式，多种数据类型可以通过举例子的方式来了解。

### 第3节 控制流

控制流可以理解成在给予一定的判断条件，当满足某个判断条件的时候就输出某个值。关注几个概念：‘迭代’，‘遍历’，‘循环’。

17.zip和enumerate
zip的用法可以想象是衣服的拉链，列表就是上面一个一个元素组成的，然后拉链拉过的地方就会进行元素的合并。

enumerate相当于是将元素的位置信息和元素本身枚举出来。

### 第4节 函数

5.变量作用域

变量只有一定范围内才可以被访问到，比如定义在函数内的变量，只能被这个函数访问到；定义在全局内的变量，它可以被函数访问到。

11.lambda表达式

lambda表达式由两部分所组成，冒号前面的参数部分，冒号后面的表达式部分，也就是返回的结果。

14.迭代器和生成器

迭代器就是每次只生成一个元素的对象，而生成器就是产生迭代器的函数。

### 第5节 脚本编写

关于配置环境

- 配置基本环境
  - anaconda+jupyter notebook
- 学习jupyter notebook、spyder、sublime text等文本编辑器的用法
  - 快捷键

8.文本字符串格式化

```python
name = input("Enter your name: ")
print("Hello there, {}!".format(name.title()))
```

在这里input接受输入的文本，赋值到name这个变量当中，然后通过`.format`的方法将name这个变量传入到文本当中的`{}`，像是填空题一样，称为python的文本字符串格式化。还有其他的实现方式。

比如

```python
name = input("Enter your name: ")
print("Hello there, %s!"%(name.title()))
```

python3版本还有

```python
name = input("Enter your name: ")
print(f"Hello there, f{name.title()}!")
```







### 

## 