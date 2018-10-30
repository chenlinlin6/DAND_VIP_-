
## 导读
在此项目中，你将利用 Python 探索与以下三大美国城市的自行车共享系统相关的数据：芝加哥、纽约和华盛顿特区。你将编写代码导入数据，并通过计算描述性统计数据回答有趣的问题。你还将写一个脚本，该脚本会接受原始输入并在终端中创建交互式体验，以展现这些统计信息。

通过该项目，你将掌握：  
- 基本的python语法  
- python数据分析工具包numpy、pandas的使用
- 数据可视化
- 完整的数据分析流程

**现在踏上成为数据分析师的日月征途吧！**✨٩(˃̶͈̀௰˂̶͈́)و

🔧工欲善其事，必先利其器，在正式开始打怪之前，不妨准备好以下的工具。

### 你需要什么软件？

- 安装anaconda（非必需，但十分推荐，有条件的都安装一个不会有错）
  - 参考课程的第7课[配置anaconda](https://classroom.udacity.com/nanodegrees/nd002-cn-basic-vip/parts/e566ad37-6119-4448-a6bc-7ade73ef3992/modules/2424424b-f71a-4c80-a34c-9a1f47e35cd5/lessons/c6a12f2e-63f2-4007-a2c3-dd3e5f06f3cb/concepts/4cdc5a26-1e54-4a69-8eb4-f15e37aaab7b)，anaconda一个安装包就一条龙服务，双击一下安装，喝杯茶回来，发现Python，Numpy，Pandas等各种工具包，ipython，spyder等各种交互式编辑器都整好了。
  - ![image-20181026223903206](/Users/chenlinlin/Documents/macbook air/写的文章/DAND_VIP_数据分析入门班每周导学/pic/配置anaconda.png)
- 文本编辑器，sublime text或者atom，推荐使用sublime
- 终端应用（Mac 和 Linux 上的终端和 Windows 上的 Cygwin）

## 项目概述

项目概述请认真参考课程里的[介绍](https://classroom.udacity.com/nanodegrees/nd002-cn-basic-vip/parts/0ad43cea-8e74-4486-911c-d1fae2f03c97/modules/134150b9-81b0-40d1-9c2c-bb288bb49d55/lessons/e5bef1dd-5031-45c3-aaf7-8536f6f3cf8a/concepts/d233dd24-607b-4bb1-a17d-dfa94768104b)。



![](\pic\共享单车图片.jpg)

## 学习地图

### ／项目总体规划／

项目名称：探索共享单车用户行为规律 

项目时间：4周 

- 🚕 **第1周：Python基础内容 - Python基础（数据类型和运算符、控制流、函数、脚本编写）**
- 第2周：Python数据处理内容 - Python数据分析（学习Numpy、Pandas库基本操作） 
- 第3周：完成项目并实现第一次提交
- 第4周：通过项目 - 修改项目，项目的反思总结，整理成可呈现面试的项目报告

### 本周要完成的任务

- 完成Python基础部分的知识点学习
- 完成项目2的python练习
  - [ ] lesson 2 数据类型和运算符
  - [ ] lesson 3 控制流
  - [ ] lesson 4 函数
  - [ ] lesson 5 脚本编写
- 下载bike_share。zip文件，查看要完成的任务，列到清单

## 学习方法

- 如果你是学习新手
  - 不妨跟着视频学习，并且多动手
  - 遇到代码思路不清晰的时候，尝试用分解的方法去分解实现的步骤，并且与自己对话，用普通话跟自己解释如何实现（费曼学习法）
  - 可以在安装完anaconda以后，用mac osx的终端或者是windows的Cygwin的ipython界面来进行一些代码的测试。例如我不知道`zip()`的用法，那么我可以在终端敲入`list(zip([a, b], [1, 2]))`来看一下反馈的结果。
- 如果你已经有了一定的编程基础
  - 可以看一下文字的教程，并且动手做一下编程题，有问题再去查找解决方案或者是看视频

### 第2节 数据类型和运算符

按照课时2.1-2.30了解基本的概念即可。运算符参照一般的数学表达式，多种数据类型可以通过举例子的方式来了解。

### 第3节 控制流

控制流可以理解成在给予一定的判断条件，当满足某个判断条件的时候就输出某个值。关注几个概念：‘迭代’，‘遍历’，‘循环’。

**条件语句**1～3部分

注意认真完成练习题

- if，elif，else试着用三个造个句子
- 如果代码有层级的时候要注意缩进问题（比如底下如果输入是满足x的，接下来就要判断是否满足y，有个先后顺序在里面，y是被包在里面的，所以y要相对于x条件缩进）

```python

#if x:
#    if y:
#        code-statement
#elif z:
#    other-code-statement
#else:
#    another-code-statement


person = 'George'

if person != 'George':
    if person == 'Sammy':
    	print('Welcome Sammy!')
elif person =='George':
    print('Welcome George!')
else:
    print("Welcome, what's your name?")
```

**条件布尔表达式**4～6部分

认真学习知识点，完成练习题。

- 了解判断语句返回的是布尔值`True`和`False`。

- 了解python的比较符号返回的是布尔值

  - <h2> Table of Comparison Operators </h2><p>  In the table below, a=3 and b=4.</p>

    <table class="table table-bordered">
    <tr>
    <th style="width:10%">Operator</th><th style="width:45%">Description</th><th>Example</th>
    </tr>
    <tr>
    <td>==</td>
    <td>If the values of two operands are equal, then the condition becomes true.</td>
    <td> (a == b) is not true.</td>
    </tr>
    <tr>
    <td>!=</td>
    <td>If values of two operands are not equal, then condition becomes true.</td>
    <td>(a != b) is true</td>
    </tr>
    <tr>
    <td>&gt;</td>
    <td>If the value of left operand is greater than the value of right operand, then condition becomes true.</td>
    <td> (a &gt; b) is not true.</td>
    </tr>
    <tr>
    <td>&lt;</td>
    <td>If the value of left operand is less than the value of right operand, then condition becomes true.</td>
    <td> (a &lt; b) is true.</td>
    </tr>
    <tr>
    <td>&gt;=</td>
    <td>If the value of left operand is greater than or equal to the value of right operand, then condition becomes true.</td>
    <td> (a &gt;= b) is not true. </td>
    </tr>
    <tr>
    <td>&lt;=</td>
    <td>If the value of left operand is less than or equal to the value of right operand, then condition becomes true.</td>
    <td> (a &lt;= b) is true. </td>
    </tr>
    </table>


17.zip和enumerate
zip的用法可以想象是衣服的拉链，列表就是上面一个一个元素组成的，然后拉链拉过的地方就会进行元素的合并。

请在ipython中练习

```python
letters = ['a', 'b', 'c']
nums = [1, 2, 3]
nl=list(zip(letters, nums))
print(nl)
letters, nums = nl
print(letters, nums)
for letter, num in zip(letters, nums):
    print("{}: {}".format(letter, num))
```

这里就像是，`letters`和`nums`是两个拉链，通过zip方法，拉链上面的元素就关联了起来，变成了`[('a', 1), ('b', 2), ('c', 3)]`这样的一整条拉链。

🌟🌟17的练习先确定目标，最后要返回的是一个列表，这个列表里面都是文本字符串，每个字符串都是包含四个列表里面的对应元素。

接下来是分解步骤：

1. 先用zip将四个列表里面的元素对应包含在元组里。
2. 用python的文本格式化format方法去生成对应格式的文本
3. 将文本append到一个空列表当中

很多关于编程实现的思路都是：

> - 先确定自己的目标，由抽象到具体
> - 分解实现的步骤，从具体到宏观去实现

不妨多多尝试一下。

enumerate相当于是将元素的位置信息和元素本身枚举出来。

**列表推导式部分**19～21

列表推导式分成三个部分，循环部分，条件判断部分，以及最后的数据处理部分

```python
squares = [x**2 for x in range(9) if x % 2 == 0]
```

### 第4节 函数

学习内容包括：

- 函数定义
- 变量作用域
- 文档
- Lambda 表达式
- 迭代器和生成器

**定义函数**2～4

这部分要知道定义函数之后我们可以反复使用函数（就像你把洗衣机建好了以后再也不用管里面的内部组成是什么，只管把脏衣服扔进去就可以了），函数的组成，默认参数是什么

5.变量作用域

变量只有一定范围内才可以被访问到，比如定义在函数内的变量，只能被这个函数访问到；定义在全局内的变量，它可以被函数访问到。你可以理解为，中国每个省份就像是一个文件里面的各个写好的函数，每个省份都会有相同的东西，比如人民政府，万达广场……这些就类似于一个省份里面的变量。但是每个省份这些变量只限于“本省”也就是本函数范围内使用，就像是河南的万达集团无法跨域去管理广东的万达集团，哪怕它们在写好的函数里面的名字是一样的，有个使用的范围，所以叫“域”。

```python
# This works fine
def some_function():
    word = "hello"

def another_function():
    word = "goodbye"
    
    
print(some_function())
print(another_function())
```

这里两个函数里面的`word`是一样的吗？不妨打印下

11.lambda表达式

`lambda`表达式由两部分所组成，冒号前面的参数部分，冒号后面的表达式部分，也就是返回的结果。

`map`、`filter`和`lambda`的联用可以对可遍历的类型比如列表，元组等进行单个元素的操作，然后返回对应的列表或者是元组等等。

要认真完成课程对应的[习题](https://classroom.udacity.com/nanodegrees/nd002-cn-basic-vip/parts/0ad43cea-8e74-4486-911c-d1fae2f03c97/modules/2ceb59e6-2fa6-4177-a8b8-b6130f45ac3f/lessons/d91fa76c-cfb4-40b5-8aec-40d5b25a1e58/concepts/9330654f-fbd0-4c90-bb30-cc0cb3b0a078)，体验一下。



14.迭代器和生成器

迭代器就是每次只生成一个元素的对象，而生成器就是产生迭代器的函数。

### 第5节 脚本编写

关于配置环境

- 配置基本环境

  - anaconda+jupyter notebook
- 学习jupyter notebook、spyder、sublime text等文本编辑器的用法

  - 快捷键

  ![image-20181027235947301](/Users/chenlinlin/Documents/macbook air/写的文章/DAND_VIP_数据分析入门班每周导学/pic/添加python到环境变量.png)

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



9.练习：在脚本中接受原始输入
在这个练习当中，分步骤写代码，首先用input的方法生成三个列表，接着是遍历相同的位置索引（比如用`range(len(xxx))`）这样的方式去获得相同位置的元素，然后插入到文本。

**错误和异常部分**11～16

了解跟处理错误相关的四个语句：

- `try`
- `except`
- `else`
- `finally`

**读写文件**的两种方式：

- `with open(filename) as f`:
- `f=open(filename)`

**导入本地脚本、标准库、模块**

了解我们可以写好本地脚本，并通过导入，重新使用里面的函数。

了解`if `__name__ == '__main__':`
​    main()`只有在脚本作为主程序运行的时候才会调用。

**第三方库**

尝试用`pip install package_name`安装第三方库



### 

## 