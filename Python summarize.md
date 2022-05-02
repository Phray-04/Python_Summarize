# Python开发文档

Python Program document

---



## 前言



**内容提要**

本文档致力于帮助包括但不限于计算机专业开发人员对 Python 语言的知识整理和总结，避免重复劳动。
材料中以实践和相对全面的语言知识点，探讨了 Python 语言的运用，涵盖基础语法、编写规范、模块应用等不同的版块。辅以代码/图片/链接/安装包/知识点等讲解技术一体化的集成查询文档。


> 参考文献：[ 1 ]《 Fluent Python 》		|		[ 2 ] 千锋教育Python资料

本文档适合具有一定 Python 语言程序设计基础的开发人员查阅参考。

 

**数字版权声明**

© 本文档未成书出版和出售，所有者和最终解释权归原创作者—— <u>**燕云祈**</u> 所有 

> 版权所有，未得书面许可，本文档的任何部分和全部不得以任何形式重制或用于商用。



## 入门基础篇

### 一	环境搭建

#### 1. 操作系统



**Windows**

[Python](https://www.python.org/downloads/release/python-391/)，[Pycharm](https://www.jetbrains.com/pycharm/download/download-thanks.html?platform=windows)专业版（破解详见激活教程），VMware虚拟机Ubuntu(Linux)操作系统

开发注解:软件安装包,使用教程

**Linux**

Vim、Pycharm



#### **2.工具**

XMind 思维导图、Typora 笔记查阅，GitHub Desktop 项目空间



**Python Console** -- IDLE交互式编程（用于即时代码验证和解释）

\>>> print(“hello world”)

\>>> hello world



**包管理工具**：pip安装Python第三方工具包(添加到用户环境变量PATH中)；Pip install  包名

 

###  二	Python语言概述



#### **1. 面向对象语言**

（特点--谁来做）：继承、多态、封装

**封装**：定义类的准则。根据对象的特点，抽象化属性和行为，封装到一个类中。

**继承**：设计类的技巧。父类与子类，代码重用；

**多态**：不同的子类调用相同的父类方法，产生不同的执行结果，可以增加代码的外部灵活度。以继承和重写父类方法为前提的，它是一种调用方法的技巧，不会影响到类的内部设计

#### 2.评估

**优点**：解释型语言、高层语言、可移植性、面向对象、可扩展性、丰富的库

**缺点**：非独立性、执行效率低（解释型语言通有的）

**应用**：Web开发、操作系统管理、服务器运维自动化脚本、网络爬虫、科学计算与数据分析、桌面软件、服务器软件（网络软件）、游戏开发、人工智能与机器学习、云计算



#### **3. 专业分支方向**

<u>数据方向</u>:Python基础--Python进阶--爬虫-数据分析--数据可视化

<u>运维方向</u>:Python基础--Python进阶--计算机网络--Linux系统与shell编程

<u>Web方向</u>:Python基础--Python进阶--Linux基础--Web前端知识(HTML/CSS/JavaScript)--web框架(DjanGo/Flask)

#### 4. 应用领域

+ WEB开发：
  Django、Flask、Pyramid、Tornado等框架

+ 网络爬虫：
  urllib库、requests库、Scrappy框架
+ 科学计算与数据分析：
  Numpy、SciPy、Matplotlib库（替代MATLAB）
+ 人工智能与机器学习：
  神经网络框架PyTorch、TensorFlow
+ 云计算：
  OpenStack
  自动化运维、网络编程、游戏开发pygame等



### 三	数据结构

 

#### **1. 数据类型**

整型int、浮点型float、复数complex、字符串str、布尔型bool（T/F）

 列表list[' ',' ']、元祖tuple( ,)、字典dict{' ':' '}、集合set{ ,'  ', }

**不可变类型**：字符串、数字、元组（字典的键值）

**可变类型**：列表、字典、集合（内存地址:值变址不变）

*字符串、列表、元组、字典和集合都是由多个元素组成的<u>可迭代对象</u>*



#### 2. 序列结构



常用的序列结构:字符串/列表/元组/字典/集合



*Key查找数据、get获取数据、为已存在的键赋值以修改数据*; **forzenset( )**一旦创建不能修改

**基本操作**：增删改查		**修改元素**：为指定的下标赋值	索引/切片/合并/删除del()

下标获取元素第一个索引是0;操作嵌套列表，只要把要操作元素的下标当作变量名来使用即可。



| 方法          | 要点                                    |
| ------------- | --------------------------------------- |
| append        | 增加元素                                |
| extend        | 目标列表元素加到本列表尾部              |
| insert        | 指定元素插入到列表指定位                |
| remove        | 删除(首次出现)元素                      |
| pop           | 删除并返回指定位置元素                  |
| clear         | 删除全部元素                            |
| index         | (索引)访问元素                          |
| count         | 计(元素出现)数                          |
| len           | 列表长度                                |
| reverse       | 翻转列表(逆序排列,返回迭代器对象)       |
| sort          | 排序                                    |
| copy/deepcopy | 浅拷贝(内容一样但不是同一个对象)/深拷贝 |
| zip           | 列表合成为元组                          |
| update        | 在旧字典上添加新的键值对                |



列表、元组、字典、集合（区分和使用） :

|        | 列表list            | 元组tuple           | 集合set           | 字典dict                   |
| ------ | ------------------- | ------------------- | ----------------- | -------------------------- |
| 读写   | 读写(偏移读取)      | 只读(偏移)          | 读写(键读取)      | 读写                       |
| 存储   | 值                  | 值(长度固定)        | 键(不能重复)      | 键值对                     |
| 重复   | 是                  | 是                  | 否                | 值重复键不重复             |
| 初始化 | [1,'a']             | ('a',1)             | set([1,2])或[1,2] | {'a':1,'b':2}              |
| 添加   | append              | 只读(不可变/调用)   | add               | key-value(键-值)           |
| 其他   | 任意类型,有序可嵌套 | 任意类型,有序可嵌套 | 无序              | 无序可嵌套,唯一且不可变.   |
|        | 对象引用数组        | 对象引用数组        | 每个都是键key     | 键key映射到值,核心是散列表 |





 

#### **3. 字符串**

单引号’’ 双引号””效果相同  

\转义字符：

\r将当前位置移到本行开头；\n将当前位置移到下一行开头；\t表示一个制表符

[\\一个反斜线字符](http://一个反斜线字符)；\’表示一个单引号；[\\”表示一个双引号](http://\”表示一个双引号)

 

**索引**下标从0开始（从左往右），倒序从-1开始（从右往左）

**切片**（字符串、列表、元祖）

*在Python中，字符串是不可变的！所有的字符串相关方法，都不会改变原有的字符串，都是返回一个结果，在这个新的返回值里，保留了执行后的结果！*



##### 1  字符串操作

  find,index,rfind,rindex

  获取长度:len

  查找内容:find,index,rfind,rindex

  判断:startswith,endswith,isalpha,isdigit,isalnum,isspace

  计算出现次数:count

  替换内容:replace

  切割字符串:split,rsplit,splitlines,partition,rpartition

  修改大小写:capitalize,title,upper,lower

  空格处理:ljust,rjust,center,lstrip,rstrip,strip

  字符串拼接:join

<u>执行字符串</u>eval函数：执行字符串里的Python代码

 



##### **2 成员运算符**

 in  not in  //快速的判断元素是否在指定的可迭代对象里

  format{}替换字段；

```python
# 例：print(**‘我叫{},今年{}岁’.format(‘小明’,18))**
# 我叫小明，几年18岁
# 大括号个数可以小于位置参数的个数（若多于则报错）

Print(‘a{1}b{2}c{name}’.format(‘55’,’66’,’77’,c=’88’))

a66b7788
a,b=4,5  ==>  a,b=b,a # 通过字段名/变量名交换两个变量的值：

```

 

**JSON**

dumps，将字典、列表或者元组转换成为字符串

loads，将格式正确的字符串转换成为字典、列表



##### **3 深拷贝浅拷贝**

Copy浅拷贝（引用）、深拷贝（所有层次递归）//切片属于浅拷贝



###  四	编码规范



#### 1. 普通规范

输入/输出,注释,换行

```python
# input 输入
age = input('请输入密码:')# 注意：不管用户输入的是什么，变量保存的结果都是字符串。
print(type(age))  # <class 'str'>

# print 输出
'''print(value, ..., sep=' ', end='\n', file=sys.stdout, flush=False)
sep 参数用来表示输出时，每个值之间使用哪种字符作为分隔。默认使用空格作为分隔符
end 当执行完一个print语句以后，接下来要输出的字符。默认 \n 表示换行
'''	# 三个单引号表示多行注释;一个井号表示单行注释
print('hello', 'good', 'yes', 'hi', sep='+',end="-------------")	# demo
print(type())	# 查看变量对应的值的数据类型（变量没有数据类型、数据才有数据类型）

```



  a=b=c=1 多变量赋值



#### **2. 格式化输出符号**

%% 输出%号；  %s字符串； %d 有符号十进制整数；  %f浮点数；  %c字符

%u无符号十进制整数；  %o八进制整数；  %x十六进制整数（小x或大X）；

%e科学计数法（小e或大E）；  %g %f和%e的简写；  %G %f和%E的简写;

 

#### **3. 标识符命名**

以下划线或者A-Z/a-z中字母开头，长度不受限，区分大小写，不能用关键字;

变量_函数_模块名 使用下划线链接

 

 

### 五	运算符和数制

 

#### **1. 进制转换**(2/8/10/16)

2--10:按权展开,小数点左正右负

10--2:整数除二取余,小数乘二取整

2--8:小数点向左/右起三个一组,不足三个补0

2--16:小数点向左/右起四个一组,不足四个补0

Bin：将数字转换成二进制

Oct将数字转换成八进制

Hex：将数字转换成十六进制

Chr：编码转字符

Ord：字符转编码

*默认输入输出都是十进制数*

#### 2. **字符集**

8bit=1byte（最大整数十进制255/二进制11111111）

ASCII编码（A65 a97）

Unicode统一码

Print(ord(‘a’))获得字符对应的编码chr获得编码对应的字符

编码规范：GBK（汉字占两个字节）、Big5、UTF-8（汉字占三个字节）

编码encode/解码decode

#### **3. 整数的表示方式**

bin()将数字转换成二进制;oct()转换成八进制；hex()转换成16进制

int转换成整数；int(‘1a2b’,16)带进制的转换

 

#### **4. 运算符**

**算数**: ()小括号  **指数幂运算  *乘  /除  //整除  %取余(mod)  +加  -减 

加+ 用于字符串、列表和元组，用来拼接多个可迭代对象;-用于集合里，求两个集合的差集;乘\* 用于字符串重复，用于字符串、列表和元组，将可迭代对象重复多次,<u>数字和字符不能相加</u> 

**赋值**： = 赋值运算符  +=  -=  *=  /=  //=  %=  **= (a+=b即a=a+b)

```python
a=b=c=d='hello'	# 连续赋值
e,f=1,2	# 拆包
```

<u>等号左边一定不能是常量或者表达式</u>

**比较**：== 等于  ！=不等于  <> 是否不等于  >  <  >=  <=

值为 true或flase

**逻辑** not	>	and	>	or

**位运算符**：& 按位与	  | 按位或	  ^ 按位异或 	 ~ 按位取反	  <<左移 	 >>右移

没有自增自减运算符

**运算符优先级**： **  ~ + -  * / % // + - >> << & ^| <= < > >=<> == !== %= /= //= -= += *= **= is is not in not in not>and>or

 

 

### 六	流程控制语句

 

#### **1. 分支语句**

if	|	if...else	|	if...elif...elif...else

```python
ticket = input('是否买票了?Y/N')
if ticket == 'Y':
    print('买票了，可以进站')
    safe = input('安检是否通过?Y/N')
    if safe == 'Y':	# 出现if嵌套时要使用缩进
        print('安检通过了，进候车室')
    else:
        print('进站了，但是安检未通过')
else:
    print('没有买票，滚蛋')
    pass	# 占位符，无任何意义，可保证语句完整性
```



#### **2. 循环语句**

while	|	for in



```python
for i in range(1, 11):	# range 内置类用来生成指定区间的整数序列(列表),in后面是一个可迭代对象(字符串/列表/字典/元组/集合/range
    print(i)
```

break结束整个循环	|	continue结束本次循环



```python
# demo:连续区间判断 1<a<3

'''输入年，写代码判断输入的年是否是闰年，并且打印对应的结果。
(是闰年的条件: 能被4整除但是不能被100整除或者能够被400整除的年)''' 

 year = int(input('请输入一个年份:'))

 if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):

   print(year, '是一个闰年')

```





 

### 七	函数



#### 基础函数

 

具有独立功能的代码块的模块——***\*函数\****

 **Function对应函数的数据类型，函数名只是变量！**

 \#当出现函数重名时，后来居上

##### **1. 定义**

def 函数名(等待赋值的变量名):

代码

\#函数定义（形参：在形参中默认有值的参数，称之为缺省参数；有默认值的参数一定要位于参数列表的最后面）

***\*Function对应函数的数据类型，而函数名仅仅是一个变量用于指向定义的函数，函数名可以被修改！！！\****

##### **2. 执行**

函数名()	#函数调用（要运行的数据）

\#定义完成不执行，手动调用后才会执行（实参）

##### **3. 返回值**

return		#执行return会结束函数，return后面可以是元组，列表、字典等（多个数据默认打包为元组），只要是能够存储多个数据的类型，就可以一次性返回多个数据；

对多个数据进行拆包（拆分为多个变量直接使用）

 

##### 4. 作用域

局部变量locals（内部使用）；全局变量global（所有函数使用）

 

//应避免二者名称相同；若相同，局部函数变量名=数据：即定义了一个局部变量而不是修改了全局变量

 

#### 内置高阶函数

| 函数                                                         | 描述                                                     |
| ------------------------------------------------------------ | -------------------------------------------------------- |
| [abs()](https://www.w3school.com.cn/python/ref_func_abs.asp) | 返回数的绝对值                                           |
| [all()](https://www.w3school.com.cn/python/ref_func_all.asp) | 如果可迭代对象中的所有项均为 true，则返回 True。         |
| [any()](https://www.w3school.com.cn/python/ref_func_any.asp) | 如果可迭代对象中的任何项为 true，则返回 True。           |
| [ascii()](https://www.w3school.com.cn/python/ref_func_ascii.asp) | 返回对象的可读版本。用转义字符替换 none-ascii 字符。     |
| [bin()](https://www.w3school.com.cn/python/ref_func_bin.asp) | 返回数的二进制版本。                                     |
| [bool()](https://www.w3school.com.cn/python/ref_func_bool.asp) | 返回指定对象的布尔值。                                   |
| [bytearray()](https://www.w3school.com.cn/python/ref_func_bytearray.asp) | 返回字节数组。                                           |
| [bytes()](https://www.w3school.com.cn/python/ref_func_bytes.asp) | 返回字节对象。                                           |
| [callable()](https://www.w3school.com.cn/python/ref_func_callable.asp) | 如果指定的对象是可调用的，则返回 True，否则返回 False。  |
| [chr()](https://www.w3school.com.cn/python/ref_func_chr.asp) | 返回指定 Unicode 代码中的字符。                          |
| classmethod()                                                | 把方法转换为类方法。                                     |
| [compile()](https://www.w3school.com.cn/python/ref_func_compile.asp) | 把指定的源作为对象返回，准备执行。                       |
| [complex()](https://www.w3school.com.cn/python/ref_func_complex.asp) | 返回复数。                                               |
| [delattr()](https://www.w3school.com.cn/python/ref_func_delattr.asp) | 从指定的对象中删除指定的属性（属性或方法）。             |
| [dict()](https://www.w3school.com.cn/python/ref_func_dict.asp) | 返回字典（数组）。                                       |
| [dir()](https://www.w3school.com.cn/python/ref_func_dir.asp) | 返回指定对象的属性和方法的列表。                         |
| [divmod()](https://www.w3school.com.cn/python/ref_func_divmod.asp) | 当参数1除以参数2时，返回商和余数。                       |
| [enumerate()](https://www.w3school.com.cn/python/ref_func_enumerate.asp) | 获取集合（例如元组）并将其作为枚举对象返回。             |
| [eval()](https://www.w3school.com.cn/python/ref_func_eval.asp) | 评估并执行表达式。                                       |
| [exec()](https://www.w3school.com.cn/python/ref_func_exec.asp) | 执行指定的代码（或对象）。                               |
| [filter()](https://www.w3school.com.cn/python/ref_func_filter.asp) | 使用过滤器函数排除可迭代对象中的项目。                   |
| [float()](https://www.w3school.com.cn/python/ref_func_float.asp) | 返回浮点数。                                             |
| [format()](https://www.w3school.com.cn/python/ref_func_format.asp) | 格式化指定值。                                           |
| [frozenset()](https://www.w3school.com.cn/python/ref_func_frozenset.asp) | 返回 frozenset 对象。                                    |
| [getattr()](https://www.w3school.com.cn/python/ref_func_getattr.asp) | 返回指定属性的值（属性或方法）。                         |
| [globals()](https://www.w3school.com.cn/python/ref_func_globals.asp) | 以字典返回当前全局符号表。                               |
| [hasattr()](https://www.w3school.com.cn/python/ref_func_hasattr.asp) | 如果指定的对象拥有指定的属性（属性/方法），则返回 True。 |
| hash()                                                       | 返回指定对象的哈希值。                                   |
| help()                                                       | 执行内建的帮助系统。                                     |
| [hex()](https://www.w3school.com.cn/python/ref_func_hex.asp) | 把数字转换为十六进制值。                                 |
| [id()](https://www.w3school.com.cn/python/ref_func_id.asp)   | 返回对象的 id。                                          |
| [input()](https://www.w3school.com.cn/python/ref_func_input.asp) | 允许用户输入。                                           |
| [int()](https://www.w3school.com.cn/python/ref_func_int.asp) | 返回整数。                                               |
| [isinstance()](https://www.w3school.com.cn/python/ref_func_isinstance.asp) | 如果指定的对象是指定对象的实例，则返回 True。            |
| [issubclass()](https://www.w3school.com.cn/python/ref_func_issubclass.asp) | 如果指定的类是指定对象的子类，则返回 True。              |
| [iter()](https://www.w3school.com.cn/python/ref_func_iter.asp) | 返回迭代器对象。                                         |
| [len()](https://www.w3school.com.cn/python/ref_func_len.asp) | 返回对象的长度。                                         |
| [list()](https://www.w3school.com.cn/python/ref_func_list.asp) | 返回列表。                                               |
| [locals()](https://www.w3school.com.cn/python/ref_func_locals.asp) | 返回当前本地符号表的更新字典。                           |
| [map()](https://www.w3school.com.cn/python/ref_func_map.asp) | 返回指定的迭代器，其中指定的函数应用于每个项目。         |
| [max()](https://www.w3school.com.cn/python/ref_func_max.asp) | 返回可迭代对象中的最大项目。                             |
| [memoryview()](https://www.w3school.com.cn/python/ref_func_memoryview.asp) | 返回内存视图（memory view）对象。                        |
| [min()](https://www.w3school.com.cn/python/ref_func_min.asp) | 返回可迭代对象中的最小项目。                             |
| [next()](https://www.w3school.com.cn/python/ref_func_next.asp) | 返回可迭代对象中的下一项。                               |
| [object()](https://www.w3school.com.cn/python/ref_func_object.asp) | 返回新对象。                                             |
| [oct()](https://www.w3school.com.cn/python/ref_func_oct.asp) | 把数转换为八进制。                                       |
| [open()](https://www.w3school.com.cn/python/ref_func_open.asp) | 打开文件并返回文件对象。                                 |
| [ord()](https://www.w3school.com.cn/python/ref_func_ord.asp) | 转换表示指定字符的 Unicode 的整数。                      |
| [pow()](https://www.w3school.com.cn/python/ref_func_pow.asp) | 返回 x 的 y 次幂的值。                                   |
| [print()](https://www.w3school.com.cn/python/ref_func_print.asp) | 打印标准输出设备。                                       |
| property()                                                   | 获取、设置、删除属性。                                   |
| [range()](https://www.w3school.com.cn/python/ref_func_range.asp) | 返回数字序列，从 0 开始且以 1 为增量（默认地）。         |
| repr()                                                       | 返回对象的可读版本。                                     |
| [reversed()](https://www.w3school.com.cn/python/ref_func_reversed.asp) | 返回反转的迭代器。                                       |
| [round()](https://www.w3school.com.cn/python/ref_func_round.asp) | 对数进行舍入。                                           |
| [set()](https://www.w3school.com.cn/python/ref_func_set.asp) | 返回新的集合对象。                                       |
| [setattr()](https://www.w3school.com.cn/python/ref_func_setattr.asp) | 设置对象的属性（属性/方法）。                            |
| [slice()](https://www.w3school.com.cn/python/ref_func_slice.asp) | 返回 slice 对象。                                        |
| [sorted()](https://www.w3school.com.cn/python/ref_func_sorted.asp) | 返回排序列表。                                           |
| @staticmethod()                                              | 把方法转换为静态方法。                                   |
| [str()](https://www.w3school.com.cn/python/ref_func_str.asp) | 返回字符串对象。                                         |
| [sum()](https://www.w3school.com.cn/python/ref_func_sum.asp) | 对迭代器的项目进行求和。                                 |
| [super()](https://www.w3school.com.cn/python/ref_func_super.asp) | 返回表示父类的对象。                                     |
| [tuple()](https://www.w3school.com.cn/python/ref_func_tuple.asp) | 返回元组。                                               |
| [type()](https://www.w3school.com.cn/python/ref_func_type.asp) | 返回对象的类型。                                         |
| [vars()](https://www.w3school.com.cn/python/ref_func_vars.asp) | 返回对象的 __dict__ 属性。                               |
| [zip()](https://www.w3school.com.cn/python/ref_func_zip.asp) | 从两个或多个迭代器返回一个迭代器。                       |



可变类型和不可变类型传参（函数参数的形参实参/传值传址）？

 append 在末尾添加元素

Insert（index,object） 在指定位置插入元素

extend 合并两个列表

count计数

Index查找元素所在位置

del删除元素

pop删除最后一个元素

remove根据元素的值进行删除

sort重新排序（默认由小到大）

reverse将列表逆置（reverse=True改为倒序）



**内置函数**

 



##### 1. 数学

mod求两个数相除的商和余数

divmod求两个数相除的商和余数

Max求最大数

Min求最小数

Pow幂运算

Round四舍五入保留到指定小数位

Sum求和

lstrip移除前导空格

 

##### 2. 转换

*详见进制转换...*

Eval：执行字符串里的Python代码

 

##### 3. 输入输出

输入input：让用户输入内容

  输出print：打印数据

 

##### 4. 操作

  open打开一个文件

  Help查看帮助文档

  Dir列出对象的所有（对应的类）属性和方法

  Id获取一个数据的内存地址

  Exit：以制定的退出码结束程序

  Globals：查看所有全局变量

  Locals：查看所有局部变量

 

##### 5. 可迭代对象

All：所有元素布尔值为true；结果为true，否则flase

Any：只有有一个为true，结果为true

Len：获取长度

Iter：获取到可迭代对象的迭代器

Next：for in循环本质就是调用迭代器的next方法

Sorted：用来排序的

 

 

##### **6.**  **高阶函数**

变量指向函数（函数别名调用）函数以另外一个和函数作为参数，函数作为另外一个函数的返回值

 

**Lambda创建匿名函数**（无需命名def的函数定义）

Lambda 参数列表：运算表达式

能接受任何数量的参数和任意类型表达式（含print）

但只能返回一个表达式的值

 

***\*函数作为参数的内置函数和类:\****

Sorted函数：对无序列表进行排序（属性由返回值决定）

Filter类过滤器：过滤列表里符合规定的所有元素，得到的结果是一个迭代器

Map映射：将列表里的每一项数据都执行相同的操作，得到的结果是一个迭代器（切分数值乘2）

Reduce函数：对一个序列进行压缩运算，得到一个值（functools模块）

Forzen冻结

Add添加参数

 

**嵌套定义**：一个函数内部定义了另一个函数

**嵌套调用**：一个函数内部调用了另一个函数

 

**嵌套结构会产生闭包**

闭包=函数快+引用环境

在内部函数里对外部作用域变量进行应用，此内部函数为闭包；

闭包内默认（局部变量）不能修改外部变量：

解决方案：nonlocal：修改前使用nonlocal关键字声明

 函数名是变量,可以被修改



函数名是改（封闭），但可以被扩展（开放）

面向对象的***\*开放封闭原则：\****已实现的功能代码不能被修改（封闭），但可以被扩展（开放）

 

引入日志，函数执行时间统计，执行函数前预备处理，执行函数后清理功能，权限校验，缓存；

有参数/无参数；可以有return（会更通用）

 

 

### 八	模块module和包packing

 

#### 1.导入/自定义/管理

**模块module（工具包）导入**

import 模块名1，模块名2...

From模块名 import 功能名（只引入模块中的某个功能函数）

From 模块名 import*（查找__all__属性里声明的所有内容）

Import模块名 as 别名

From 模块名import 功能名 as 别名



支持**自定义Python模块**定义完成放在path路径（sys.path查找路径），加到site-packing扩展包里；

自定义模块名不要和系统的模块名重名；最好在自定义模块添加一些<u>测试信息</u>；

 

**包管理工具pip**:查找下载Python第三方工具包,添加到用户环境变量PATH中

pip install 包名 ：安装指定第三方包	/	pip uninstall 包名 :卸载指定第三方包

pip list 列出所有包,pip freeze 列出安装的第三方包

#### **2. 内置模块**

| 模块     | 应用                               |
| -------- | ---------------------------------- |
| sys      | 对解释器使用或维护的一些变量的访问 |
| math     | 数学计算                           |
| random   | 生成随机数                         |
| datetime | 日期时间                           |
| time     | 操作时间(sleep控制程序暂停)        |
| calender | 日历                               |
| hashlib  | 字符加密(MD5/SHA1/SHA256/SHA512)   |
| hmac     | 单向加密算法(基于哈希散列算法)     |
| deepcopy | 数据深复制                         |
| os       | 操作系统,跨平台操作                |



____init____.py 控制着包的导入行为（魔法方法）

____all____变量控制着from包名import*时导入的模块

 

####  3. 魔法方法

两侧各有两个下划线

__init__创建对象（默认调用）

__del__删除对象（默认调用）

__str__ 描述对象（可读性）

__repr__修改对象默认打印内容（正确性）

__call__对象后面加括号，触发执行

类转换相关：

__int__  __float__  __str__  __bool__

算术运算符：

__add__  __sub__  __mul__  __truediv__  __mod__  __pow__

比较运算符：

__eq__  __ne__  __lt__  __gt__  __le__  __ge__

 

内置属性：

__slots__ 对属性进行控制

__doc__ 表示类的描述信息

__module__ 表示当前操作的对象在那个模块

__class__ 表示当前操作的对象的类是什么

__dict__ 以字典的形式，显示对象所有的属性和方法

__getitem_、_setitem__ 、 __delitem__将对象当做字典一样操作

 



### 九	开发思维



#### 1. 面向对象 $ 面向过程

 

***\*面向对象\****OO：将变量与函数绑定到一起，分类进行封装，每个程序只要负责分配给自己的分类，这样能够更快速的开发程序，减少了重复代码	***\*谁来做\****

在完成某一个需求前，首先确定职责 —— 要做的事情（方法）

根据 职责 确定不同的 对象，在对象内部封装不同的方法（多个）

最后完成的代码，就是顺序地调用不同对象的相应方法

OOA:面向对象分析

OOD:面向对象设计

OOP:面向对象设计

 

**面向过程**：根据业务逻辑从上到下写代码	**怎么做**

  注重步骤与过程，不注重职责分工;如果需求复杂，代码会变得很复杂;开发复杂项目，没有固定的套路，开发难度很大！

 

#### 2. 类和对象

 

**类**是对一群具有相同特征或行为的事物统称，是抽象概念

特征==>属性  行为（函数）==>方法

**对象**由类创建出来的具体存在

类的类⽅法可以⽤对象和类名来调⽤ ;类的静态属性可以⽤类名和对象来调⽤ 

***\*类属性和对象属性\****

通过类创建的对象被称为 ***\*实例对象\****，对象属性又称为实例属性；类属性可以通过类对象或者实例对象访问

尽量避免类属性和实例属性同名。如果有同名实例属性，实例对象会优先访问实例属性。

类属性只能通过类对象修改，不能通过实例对象修改

 

类属性设置为***\*私有属性\****（私有方法）：只在对象内部使用

定义：在属性名或者方法名前增加两个下划线__

在外部调用：在私有属性名或方法名前添加 _类名__私有属性名

但对好用：get和set实现公开方法获取和修改私有变量

 

```python
 # 先有类（图纸）再有对象（实体）；一类多对象（不同对象属性值可以不同）
class Name:	# 类名大驼峰命名法
  def method1(self,参数列表):	# 第一个参数必须是self
    pass

  def method2(self,参数列表):
    pass

```



####  3. 开发技巧

pycharm开发习惯记录

#### 4. 面向对象进阶

 

***\*面向对象进阶\****：

访问私有类属性用类对象（实例化），类方法第一个形参是类对象

 @classmethod

 

***\*静态方法\****：当方法中 既不需要使用实例对象(如实例对象，实例属性)，也不需要使用类对象 (如类属性、类方法、创建实例等)时，定义静态方法

装饰器 @staticmethod

静态方法既不需要传递类对象也不需要传递实例对象（形参没有self/cls）,减少了内存占用

通过实例对象和类对象访问

类中定义了同名的方法时，调用方法会执行最后定义的方法

 

***\*单例设计模式\****：确保某一个类只有一个实例，而且自行实例化并向整个系统提供这个实例，这个类称为单例类(对象创建型模式)
__new__(cls)和__init__(self)方法

 

***\*继承\****：子类（派生类）具有父类（基类）的属性和方法或者重新定义、追加属性和方法等

 

单继承：子类只继承一个父类的所有方法和属性，子类中应该根据职责，封装子类特有的属性和方法（子类拥有父类以及父类的父类中封装的所有属性和方法）

多继承：多个父类（父类中的方法避免重名）

__mro__查看方法的搜索顺序，左至右顺序

新式类：以object为基类的类，没有指定父类会默认继承自object

多层继承（多态）：子类使用对象重写父类（调用不同子类对象的相同父类方法，可以产生不同的执行结果）

 

person身份运算符判断两个对象是否***\*相等\****（比较二者内存地址）；

isinstance判断一个实例对象是否是由某一个类(或者它的子类)实例化创建出来的***\*类和对象的关系\****；

issublcass判断类与类之间的继承关系

 

 

 

### 十	文件 & 异常

 

#### **1. Python2 $ Python3**

八进制只能用0o开头；两整数相除结果是一个浮点数；！=表示不等于运算符；不支持反引号``；ASCII

print('hello')输出语法格式；input直接接受用户输入，所有数据都是字符串类型；默认支持中文；默认继承自object的类;Unicode

 

#### **2. 文件操作**

 

打开文件open(文件路径,访问模式)

绝对路径：完整描述所在绝对地址；相对路径：当前文件所在文件夹开始路径

访问模式：r	w	a	rb	wb	ab	

**r	只读**（默认模式，可以省略，指针在文件开头）；r+读写（指针在开头）；rb二进制格式打开文件只读（指针在开头）;	rb+二进制读写（指针在开头）

**w	写入**（存在则覆盖，没有则创建）；w+读写（存在则覆盖，没有则创建）；wb二进制写入（存在则覆盖，没有则创建）;	wb+二进制读写（存在则覆盖，没有则创建）

**a	追加**（指针在文件尾，没有则创建）;a+读写（指针在文件尾，没有则创建）;ab二进制追加（指针在文件尾，没有则创建）;	

ab+二进制读写（指针在文件尾，没有则创建）

 

关闭文件 f.close()	#注意程序用完必需断开资源

 

写数据write()；

读数据red(num)	#num是读取数据的长度（字节为单位，默认所有）

Readline读取一行数据；readlines按行读取，返回列表；tell()显示当前指针的位置；

Seek(offset,whence)重新设定指针的位置（偏移量，0开头1当前2末尾）

***\*CSV文件\****：逗号分隔值（字符分隔值）

以纯文本形式存储表格数据（单元格--逗号；行数据--换行）

file = open('test.csv','w')文件写入r读取

writer = csv.writer(file)

writer.writerow(['name', 'age', 'score'])一行行写入

writer.writerows([['zhangsan', '18', '98'],['lisi', '20', '99'], ['wangwu', '17', '90'], ['jerry', '19', '95']])

一次性写入多个数据

 

***\*写入内存\****：

F=StringIO类写入字符串

F=BytesIO类写入二进制

 

***\*文件备份：\****

file_names =file_name.rsplit('.', maxsplit=1)#分割文件名和后缀名

new_file_name = file_names[0] + '.bak.'+file_names[1]#阻止新的文件名字

newFile = open(new_file_name, 'wb')#创建新文件

for lineContent in old_file.readlines():

  newFile.write(lineContent)#把旧文件中的数据一行行复制到新文件当中去

 

 

**序列化和反序列化**
把内存中的数据转化成字符序列（对象序列化写入内存）--字符序列恢复到内存

 

**1、*****\*JSON转化为字符串\****

JSON序列化

JS对象简谱--JSON，基于 ECMAScript 的一个子集（本质就是字符串）

dump/dumps对象序列化

dump方法可以在将对象转换成为字符串的同时，指定一个文件对象，把转换后的字符串写入到这个文件里

dumps方法的作用是把对象转换成为字符串，它本身不具备将数据写入到文件的功能（空对象==Null）

JSON反序列化

Load/loads

loads方法需要一个字符串参数，用来将一个字符串加载成为Python对象

load方法可以传入一个文件对象，用来将一个文件对象里的数据加载成为Python对象

 

**#字符串对应关系：dict--object、list，tuple--array，str--string，int，float--number，true--true，false--false，none--null如果是一个自定义对象，默认无法装换成为json字符串，需要手动指定JSONEncoder.**

**如果是将一个json串重新转换成为对象，这个对象里的方法就无法使用了**

 

 

 

2***\*、pickle模块转化为二进制（同上）\****

 

\#不能跨平台，保存对象的所有数据

 

#### 3.	异常处理

 

Raise手动抛出异常，程序会正常启动

##### 1. try

try:

可能会出现异常的代码块

except 异常的类型:

出现异常以后的处理语句(自发引发异常提醒)

try...else(条件不满足时执行else)

try...finally(代码必须执行)	 f.close()

 

##### 2. with

```python
# with（上下文管理器）,自主断开资源

with open("output.txt", "r") as f:

    f.write("context")

```

注意程序用完必需断开资源.	enter__()和__exit__() #程序正常或异常都会调用exit断开


标准库中的四种任务队列：
queue.Queue		asyncio.Queue		mult iprocessing.Queue		collections.deque

 

 

## **A  --基础项目汇总--**



小练手:

### 1. 猜拳游戏:

```python
import random

# 随机数模块 random生成[0,2]区间
computer = random.randint(0, 2)	# random.randint(a,b) ==> 能够生成 [a,b] 的随机整数
print('电脑出的是', computer)

player = int(input('请输入  (0)剪刀  (1)石头  (2) 布：'))  # 1 == 1 判断结果是False
print('用户输入的是', player)

if (player == 0 and computer == 2) or (player == 1 and computer == 0) or (player == 2 and computer == 1):
    print('胜利')
elif player == computer:
    print('平局')
else:
    print('失败')

```

### 2. 嵌套打印三角形

```python
j = 0
while j < 9:	# 行数
    j += 1  # j = 1;j=2
    i = 0
    while i < j:	# 列数
        i += 1
        print('*', end=' ')
    print()
```

### 3. 打印9x9乘法表

```python
j = 0
while j < 9:
    j += 1  # j = 3;
    i = 0  # i=0;
    while i < j:
        i += 1  # i=2;
        print(i, '*', j, '=', (i * j), sep="", end="\t")
    print()
```

### 4. 珠峰问题

```python
# 纸厚0.08毫米，对折多少次达到珠峰高度8848.13米
height = 0.08 / 1000	# 毫米到米1000
count = 0	# 次数
while True:
    height *= 2
    count += 1
    if height >= 8848.13:
        break

print(count)
```

### 5. 冒泡排序

```python
# 让一个数字和它相邻的下一个数字进行比较运算.如果前一个数字大于后一个数字，交换两个数据的位置
nums = [6, 5, 3, 1, 8, 7, 2, 4]

# nums[0]  nums[1]
# nums[1]  nums[2]
# ... ...
# nums[n]  nums[n+1]
# ... ...
# nums[length - 2] nums[length - 1]

# 每一趟比较次数的优化
# 总比较趟数的优化
i = 0
while i < len(nums) - 1:
    i += 1
    n = 0

    while n < len(nums) - 1:
        if nums[n] > nums[n + 1]:
            nums[n], nums[n + 1] = nums[n + 1], nums[n]
        n += 1

    print(nums)

# 有一个列表names，保存了一组姓名names=['zhangsan','lisi','chris','jerry','henry']
# 再让用户输入一个姓名，如果这个姓名在列表里存在，提示用户姓名已存在；
# 如果这个姓名在列表里不存在，就将这个姓名添加到列表里。
```



### 6. 飞机大战

pygame游戏开发模块

### 7. 植物大战僵尸



## B 应用进阶篇

 

### 一 迭代器和生成器

 

***\*装饰器decorator\****功能：

在不改变原函数的基础上为函数添加新功能的方法

@classmethod类方法  ：把类的函数直接使用（不用实例化），在解释器自动调用init()来构造之前实现一些预处理逻辑，然后将预处理后的参数传入类的构造函数来创建类实例。

@staticmethod静态方法 ：把类的方法直接作为类的静态方法使用，类的静态成员属于类本身，不属于类的实例，它无法访问实例的属性（数据成员或成员函数））。定义为 staticmethod的函数被调⽤时，解释器不会⾃动为其隐式传⼊类或类实例的参数，它的实际 参数列表与调⽤时显式传⼊的参数列表保持⼀致

@property实例方法：把方法变成属性调用，通常⽤在属性的get⽅法和set⽅法，通 过设置@property可以实现实例成员变量的直接访问，⼜保留了参数的检查。另外通过设置 get⽅法⽽不定义set⽅法可以实现成员变量的只读属性。

 

***\*迭代器（iterator）\****：可以记住遍历的位置的对象

迭代（遍历）访问集合元素，从头至尾不后退；

list、tuple、str（可迭代对象）用for...in...循环遍历——迭代操作

Isinstance判断一个对象是否可迭代（iterable对象）：是否具备__iter__方法

__next__返回它所记录位置的下一个位置的数据（核心功能）

***\*即：可迭代对象通过__iter__对象提供迭代器，用于遍历对象中的每个数据，\*******\*迭代器本身是可迭代的，迭代器的__iter__方法返回自身\****

***\*结论：\****一个实现了iter方法和__next__方法的对象，就是迭代器

 

判断一个对象是否为可迭代器：print(duixiang.__iter__())或print(isinstance(iter(names), Iterator))

For...in...（for item in Iterable）循环的本质：

1、__iter__方法获取可迭代对象iterable的迭代器iterator

2、对iterator不断调用__next__方法获取下一个值赋值给item

3、当遇到Stoplteration异常后循环结束

 

应用场景：

斐波那契序列：
class FibIterator(object):

  """斐波那契数列迭代器"""

  def __init__(self, n):

​    """

​    :param n: int, 指明生成数列的前n个数

​    """

​    self.n = n

​    \# current用来保存当前生成到数列中的第几个数了

​    self.current = 0

​    \# num1用来保存前前一个数，初始值为数列中的第一个数0

​    self.num1 = 0

​    \# num2用来保存前一个数，初始值为数列中的第二个数1

​    self.num2 = 1

 

  def __next__(self):

​    """被next()函数调用来获取下一个数"""

​    if self.current < self.n:

​      num = self.num1

​      self.num1, self.num2 = self.num2, self.num1+self.num2

​      self.current += 1

​      return num

​    else:

​      raise StopIteration

 

  def __iter__(self):

​    """迭代器的__iter__返回自身即可"""

​    return self

 

 

if __name__ == '__main__':

  fib = FibIterator(10)

  for num in fib:

​    print(num, end=" ")

 

***\*生成器(特殊类型的迭代器):\****记录当前状态，并配合next函数进行迭代

 

***\*创建生成器：\****把列表生成式的[]改成()，可进行Next、for循环、list方法操作

***\*生成器定义：\****generator函数：在def中有yield关键字

 

Yield断点挂起，表达式返回值，next唤醒生成器，return返回最终的返回值

Send唤醒同时向断点处传入一个附加数据

 

@property（装饰器）属性对应某个实例方法(self)参数：内部进行一系列的逻辑计算，最终将计算结果返回

两种方式：

1、装饰器：[在类的实例方法上应用@property装饰器，三种访问方式对应了三个被@property、@方法名.setter、@方法名.deleter修饰的方法](mailto:在类的实例方法上应用@property装饰器，三种访问方式对应了三个被@property、@方法名.setter、@方法名.deleter修饰的方法)

2、类属性：

 

  第一个参数是方法名，调用 对象.属性 时自动触发执行方法

  第二个参数是方法名，调用 对象.属性 ＝ XXX 时自动触发执行方法

  第三个参数是方法名，调用 del 对象.属性 时自动触发执行方法

  第四个参数是字符串，调用 对象.属性.doc ，此参数是该属性的描述信息

###  二 多任务



**十八、**进程process（电脑的应用）和线程thread（应用的窗口）

 

线程开销小，不利于维护；进程相反

一个进程最少一个线程

 

多任务：多进程模式/多线程模式/多进程+多线程模式

 

并发：任务数多于CPU核数（通过OS调度实现）

并行：任务书数小于CPU核数（真的一起执行）

 

**线程**：

 

Import threading

 

线程访问全局变量：

在一个进程内的所有线程共享全局变量，很方便在多个线程间共享数据。

缺点：线程对全局变量随意遂改可能造成多线程之间对全局变量的混乱（即线程非安全）。

 

线程安全问题：互斥锁（即协调线程同步机制）

互斥锁：锁定/非锁定锁定状态下其他线程不可写入

 

\# 创建锁

mutex = threading.Lock()# 锁定

mutex.acquire()# 释放

mutex.release()

 

 

线程或进程通信：Queue原理：先进先出

Put()放入 get()取出

 

\# 多线程版聊天

import socketimport threading

 

s = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)

s.bind(('0.0.0.0', 8080))

 

def send_msg():

  ip = input('请输入您要聊天的ip:')

  port = int(input('请输入对方的端口号:'))

  while True:

​    msg = input('请输入聊天内容:')

​    s.sendto(msg.encode('utf-8'), (ip, port))

​    if msg == "bye":

​      ip = input('请输入您要聊天的ip:')

​      port = int(input('请输入对方的端口号:'))

 

def recv_msg():

  while True:

​    content, addr = s.recvfrom(1024)

​    print('接收到了{}主机{}端口的消息:{}'.format(addr[0], addr[1], content.decode('utf-8')),file=open('history.txt', 'a', encoding='utf-8'))

 

 

send_thread = threading.Thread(target=send_msg)

recv_thread = threading.Thread(target=recv_msg)

 

send_thread.start()

recv_thread.start(

 

**进程**：

 

程序运行时，代码+用到的资源=进程

状态：就绪态/执行态/等待态

 

进程池

from multiprocessing import Process# 引入进程

 

### 五 正则表达式 

 

re模块,用于特殊的字符序列，用于检索、替换符合某个格式的文本。

```python
# 正则中的(), [] , {} 三个符号的作用

( ) 用于分组的符号
[ ] 指定匹配字符的范围，如 [a-c_B-F]
{ } 指定匹配的长度(量词表示)

import re
# 用户名匹配
# 用户名只能包含数字、字母和下划线,不能以数字开头,长度在6到16位范围
username = input('请输入用户名:')
# x = re.match(r'^[a-zA-Z_][a-zA-Z0-9_]{5,15}$', username)
x = re.fullmatch(r'[a-zA-Z_][a-zA-Z0-9_]{5,15}', username)
if x is None:
    print('输入的用户名不符合规范')
else:
    print(x)
    
# 密码匹配
# 不能包含 !@%^&*字符,必须以字母开头,长度在6到12位
password = input('请输入密码:')
y = re.fullmatch(r'[a-zA-Z][^!@#$%^&*]{5,11}', password)
if y is None:
    print('密码不符合规范')
else:
    print(y)
    
#打开文件操作
z = []
try:
    with open('demo.txt', 'r', encoding='utf8') as file:
        content = file.read()  # 读出所有的内容
        z = re.findall(r'1000phone.*', content)
        print(re.findall(r'^1000phone.*', content, re.M))

        while True:
            content = file.readline().strip('\n')
            if not content:
                break
            if re.match(r'^1000phone', content):
                z.append(content)
except FileNotFoundError:
    print('文件打开失败')

print(z)

# ip地址检测 0.0.0.0 ~ 255.255.255.255
num = input('请输入一个数字:')
#    0~9      10~99            100 ~ 199  200~209 210~219 220~229 230~239 240~249  250~255
# \d:一位数   [1-9]\d:两位数   1\d{2}:1xx  2:00~255
x = re.fullmatch(r'((\d|[1-9]\d|1\d{2}|2([0-4]\d|5[0-5]))\.){3}(\d|[1-9]\d|1\d{2}|2([0-4]\d|5[0-5]))', num)
print(x)

# 分组捕获
x = re.finditer(r'-?(0|[1-9]\d*)(\.\d+)?', '-90good87ni0ce19bye')
x = re.finditer(r'-?(0|[1-9]\d*)(\.\d+)?', '-90good87ni0ce19bye')
for i in x:
    print(i.group())
# 非捕获分组
x = re.findall(r'(?:-)?\d+(?:\.\d+)?', '-90good87ni0ce19bye')
print(x)
```

**查找**（语法格式相同）：
re.match(pattern=匹配的正则表达式,string=要匹配的字符串,flags=0标志位)

?:将分组标记为非捕获分组

match匹配开头

re.Search（扫描整个字符串，返回第一个成功的匹配）

re.Findall（扫描整个字符串，匹配所有）

re.Finditer（扫描整个字符串，找到所有的匹配，并返回一个可迭代对象）

修饰符（可选标志）：
re.l使匹配对大小写不敏感	|	re.L做本地化识别匹配	|	re.M多行匹配，影响^和$	|	re.S使.匹配包括换行在内的所有字符

 检索和替换：

re.sub用户替换字符串,re.sub(pattern=正则中的模式字符串, repl, string, count=0, flags=0)

 

### 六 GUI Tkinter



用户图形界面

| 控件                           | 描述                      |
| ------------------------------ | ------------------------- |
| Button  按钮                   |                           |
| Canvas  画布                   | 显示图形元素如线条或文本  |
| Checkbutton  多选框            | 多项选择                  |
| Entry  输入框                  |                           |
| Frame  框架                    | 一个矩形区域作为容器      |
| Label  标签                    | 文本或位图                |
| Listbox  列表框                | 显示字符串列表            |
| Menubutton  单选按钮           | 菜单项                    |
| Menu  菜单                     | 菜单栏,下拉菜单,弹出菜单  |
| Message  消息                  | 多行文本                  |
| Radiobutton  单选按钮          |                           |
| Scale  范围尺寸条              | 限定数字区间的数值刻度    |
| Scrolibar  滚动条              | 内容超出可视化区域时生效  |
| Text  文本                     | 多行文本                  |
| Toplevel  容器                 | 单独对话框                |
| Spinbox  选值框(输入)          | 可指定输入范围值的"Entry" |
| PanedWindow  窗口布局管理      | 可包含多个控件            |
| LabelFrame  容器               | 复杂窗口布局              |
| tkMessageBox  消息框           | 消息框                    |
| LabeledScale  有数字的尺寸条   |                           |
| OptionMenu  下拉式列表         |                           |
| Comboobox  组合框              |                           |
| Progressbar  进度条            |                           |
| Separator  分割线              |                           |
| Treeview  树形视图(表格/树状)  |                           |
| Notebook  笔记本               |                           |
| tix.Ballon  气泡提示框         |                           |
| scrolledtext  带滚动条的文本框 |                           |
|                                |                           |

三种布局方式:pack()自动布局	|	place()坐标值	|	grid()堆叠式

```
sticky参数用N/S/W/E表示上下左右（决定该组件的开始方向）

rowspan跨越的行数，columnspan跨越的列数；ipadx/ipady边距

<Button-1> 表示⿏标左键单击，其中的 1 换成 3 表示右 键被单击
<KeyPress-A> 表示 A 键被按下，其中的 A 可以换成其他 的键位。

bind.class绑定类别；
例：w.bind_class(“Entry”, “<Control-V>”, my_paste)
类名 + 事件类型 + 相应操作 ——Ctrl+V 表示粘贴
unbind解除绑定

其他标准对话框：simpledialog(简单对 话框)，commondialog(⼀般 对话框)，filedialog(⽂件对话框)
```

config配置控件样式

[Python使用鼠标滚轮调整tkinter应用程序窗口大小](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8ab472dcfd3d64bd6b2293f5f9351cf7a7b96a072e5c65bd7366e6bf00b05327a67b3d8648&idx=1&mid=2247491368&scene=21&sn=c7c510398d85f655cb95f41e734099e8#wechat_redirect)

[Python使用tkinter+moviepy+pyaudio开发视频播放器](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8ab441dcfd3d57a24e778a42f5b3287b39745fc1cc63d5ab0c03b2f18580116653c5e0e71d&idx=1&mid=2247491355&scene=21&sn=f31813afd694bf3ce223d1ade3229513#wechat_redirect)

[Python+tkinter实现超时无键盘操作自动退出](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8ab50bdcfd3c1d18ab65f3bc42ba38b140040d03c13851bc4afae15576166eb57126b6d368&idx=1&mid=2247491153&scene=21&sn=185d193f12af31d632831ad879518279#wechat_redirect)

[Python+turtle绘制虚线同心圆](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8ab64adcfd3f5c908e953d39bc531601427c12ad6622319abcd62defbcf760b2935d756875&idx=1&mid=2247490832&scene=21&sn=bdb0a0c077f0a5e782d119643b284ef4#wechat_redirect)

[Python在tkinter界面中显示matplotlib动画](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8ab0badcfd39ac7221c5b212e0f290fca07362a52e7c90233bd4cf0bc756883f51470abce1&idx=1&mid=2247490528&scene=21&sn=d655c0c0956f70d34239fdfee3cab4c2#wechat_redirect)

[一文掌握Python+tkinter键盘事件与鼠标事件处理](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8ab1fadcfd38ec94be47d484469e5d004c719e07435a648ebed1491af6fe237bb825ec00f1&idx=1&mid=2247490208&scene=21&sn=ff24572ad3905672e084bb66c370cb81#wechat_redirect)

[Python+tkinter实现文件拖放功能](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8ab128dcfd383ed9846bb73d322d11e59c70206e6b2e2cc77d03e9d76d75c03e1995edbbb2&idx=1&mid=2247490162&scene=21&sn=b41332a1e34fd04868033cb05f8ba75b#wechat_redirect)

[Python+tkinter根据窗体大小自动缩放并显示图像](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8abc37dcfd3521ec00424717cffb434f3cebed384785b6c8765f02b07683c5de6e4a13d6ed&idx=1&mid=2247489389&scene=21&sn=75785de3bc71d76011d1c009dbf7688b#wechat_redirect)

[使用Python编写属于自己的录音软件](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8ab9b0dcfd30a697b08928fa0d942997bb37782548db9be8180b745343226bb7f65653cb55&idx=1&mid=2247488234&scene=21&sn=8828157558da57e7e01ab4ec07dbc047#wechat_redirect)

[使用Python编写自己的个人密码管理器http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8abb25dcfd32336c8bea0af0e9cb8af23d6809916b5f0c84f22aa71cde742d5401c83a86ec&idx=1&mid=2247487615&scene=21&sn=a9d4c0b4fb6f855ec6047fdd3febd47e#wechat_redirect)

[使用Python+tkinter编写电脑桌面放大镜程序](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8aa28adcfd2b9c5ef052e009ce30d771120f21cade111e41e8cf5ca96be7991118756b8119&idx=1&mid=2247485904&scene=21&sn=c4d74cb6aa2253aa8547c178921697e9#wechat_redirect)

[80行代码使用Python+tkinter实现一个计算器](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8aa239dcfd2b2fa7165dc401a9ee04f3d3b9974e4aeadbd939fc2ca3daf6fb0e4987c86ed3&idx=1&mid=2247485795&scene=21&sn=d945abaca37b87a6539bac4a9f669d41#wechat_redirect)

[Python+tkinter模拟“记住我”自动登录原理](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8aaf6adcfd267cd11874a79a64f6da295d9dea2afb9f011a644265ebb7b62d7744bd2380eb&idx=1&mid=2247484464&scene=21&sn=736409bc0420d06ba25babbea3ad169f#wechat_redirect)

[基于Python+tkinter+pygame的音乐播放器完整源码](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8aa8e6dcfd21f0e1d4e8f5b524d05c08e49f1cebfefaede00bedfbf0a26e60265dcecd38c6&idx=1&mid=2247484348&scene=21&sn=eabacd77ff9f599d8d894bf3d8635992#wechat_redirect)

[Python使用tkinter打造自定义对话框完整代码](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8aa8eadcfd21fc42afc84fc077364fcbe44f1a1fb34714afa487a53fdb618dc86b91c47375&idx=1&mid=2247484336&scene=21&sn=45cf8186fb50710712c37d8c6ecbcdcf#wechat_redirect)

[Python+tkinter动态创建与销毁组件小案例](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8aa8c0dcfd21d677dc8872b224144579d5fbe2f2acddd85b2345c89e78fbb4d746a1bd59f3&idx=1&mid=2247484314&scene=21&sn=16eccb25325f286588ab51c19788b8f8#wechat_redirect)

[Python实现屏幕取色器功能](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8aa83edcfd21285567ae404b89797d62472620d28423b8e9dec99dd1ab74ff00732937dbcd&idx=1&mid=2247484260&scene=21&sn=569096888099edec4d5189c7e4877e43#wechat_redirect)

[Python编写抽奖式随机提问程序](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8aa83bdcfd212d8a9f2af222adb84108179fcbb07a72e629667f72b98e23fdfb0b23766b33&idx=1&mid=2247484257&scene=21&sn=116d13bc5c2382fe1eddf734ed0c95b2#wechat_redirect)

[Python使用tkinter编写图片浏览程序](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8aa815dcfd2103a4e9af9b345b5cf6fdb26da8974aa0527253583f3418751169d85d0eda2d&idx=1&mid=2247484239&scene=21&sn=fd88760ed9c6f500271229985c13df9a#wechat_redirect)

[Python实现倒计时按钮](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8aa81fdcfd210912efff7b4948abeb98622d8e020dc3be4a04e244d438a07561a1ff083898&idx=1&mid=2247484229&scene=21&sn=85fd9932d5a19a39fb0e6979c0cf2107#wechat_redirect)

[详解Python GUI版24点游戏制作过程](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8aa945dcfd20532dc4d3591f29eb5eb2e0cce9a4c93db478dd39670dd2b86497b092baf2c3&idx=1&mid=2247483935&scene=21&sn=907a482eb024b13b6b2c826df0299835#wechat_redirect)

[Python tkinter版猜数游戏](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&chksm=eb8aaaa0dcfd23b664ddf3a10eed6602a5fe139fc6a9c70936e7acf33df7921b90aa12fc427f&idx=1&mid=2247483898&scene=21&sn=d93349e27f5bf00dbf735f3f7285f135#wechat_redirect)

[Python+tkinter实现任意多层级关系的组合框](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&idx=1&mid=2247483746&scene=21&sn=348a1194b9ff95107994cd90fc5ba154#wechat_redirect)

[Python+tkinter+pillow实现屏幕任意区域截图](http://mp.weixin.qq.com/s?__biz=MzI4MzM2MDgyMQ%3D%3D&idx=1&mid=2247483721&scene=21&sn=e88d8a205e2671281d17b57ba91e2e0a#wechat_redirect)

### 七	数据库





#### **数据库Database**

 种类：MYSQL（web关系型数据库），mongoDB（非关系型数据库（爬虫）），redis（缓存），ACCESS，SQL server（微软项目），Oracle（大型项目，收费），sqlite（轻量级数据库）

区分：关系型数据库RDBMS程序/非关系型数据库

 

关系型数据库：行-名称；列-数据域，表格形式，行列组成表单，表单组成database

SQL structured query language 结构化查询语言，操作和MySQL基本一致,不区分大小写

结构化查询语言：

1. **数据查询语言**（DQL:Data Query Language）：SELECT

2. **数据操作语言**（DML：Data Manipulation Language）：INSERT，UPDATE和DELETE

3. 事务处理语言（TPL）：BEGIN TRANSACTION，COMMIT和ROLLBACK

4. 数据控制语言（DCL）：GRANT（授权）或REVOKE（回收权限）

5. 数据定义语言（DDL）：CREATE、ALTER和DROP

6. 指针控制语言（CCL）：DECLARE CURSOR，FETCH INTO和UPDATE WHERE CURRENT用于对一个或多个表单独行的操作



数据库、数据表、列、行、冗余、主键、外键、复合键、索引、参照完整性



#### 操作数据库/表

```SQL
create database [if not exists] `数据库名` charset=字符编码(utf8mb4);//创建数据库
show database/tables; //查看数据库/表
use'数据库的名字'; //选择数据库
create database/table'数据库/表名'; //创建数据库
alter database/table '数据库/表名' charset=字符集; //修改数据库
alter table '表名' drop '字段名' ; //删除字段
drop database/table [if exists] '数据库/表的名字' ;
insert into '表名' ; //数据
select * from '表名' where ...; //查数据
desc '表名'; //查字段

```



表的操作:

C: 创建（Create）	U: 更新（Update）	R: 读取（Retrieve）	

D: 删除（Delete）	I:  插入  (Insert)	 U: 更新  (Update)





#### SQL

关系型数据库Structured Query Language



语法表

| **数字where**       | **文本where** | **排序rows** | **Join连表（table）** | **算式（select/where）** | **统计（select）**      | **子表（table）**  |
| ------------------- | ------------- | ------------ | --------------------- | ------------------------ | ----------------------- | ------------------ |
| =, !=, < ,<=, >, >= | =             | ORDER BY     | JOIN ...ON...         | + - * / %                | COUNT(*), COUNT(column) | （select -）as tmp |
| BETWEEN … AND …     | ！= or <>     | ASC          | INNER JOIN            | substr                   | MIN()                   | in（select -）     |
| NOT BETWEEN … AND … | like          | DESC         | LEFT JOIN             | AS                       | MAX()                   | avg（select -）    |
| IN (…)              | NOT LIKE      | LIMIT OFFSET | RIGHT JOIN            |                          | AVG()                   |                    |
| NOT IN (…)          | %             | ORDER BY     | IS/IS NOT NULL        |                          | GROUP BY                |                    |
|                     | -             |              |                       |                          | HAVING                  |                    |
|                     | IN()          |              |                       |                          |                         |                    |
|                     | NOT IN()      |              |                       |                          |                         |                    |

 

 

语法手册：

Col（数字=n；/文本like ’%  ’）

Rows排序

Join 连接表table

Select 找什么 from 从哪找 where 按什么条件找

 

 语法词条：

 

Select title from table			--从表table查询title

Select * from table

Select title1，title2 from table where id < 5			--从表table中查找id小于5时列title1和title2的值

Select 1+2*3/4-(5%6) 			--select直接做算术运算

Select Distinct 				--选取出唯一结果的语法

Order By column ASC/DESC			--***\*结果排序\****（ASC升序/DESC降序）

Limit--返回多少行/Offset--从哪一行开始返回

SELECT * FROM table Order by Title ASC limit 5 OFFSET 5		--升序排列后列出前五个的后五个

Select Title From Movies Where Director='John Lasseter' order by Length_minutes DESC limit 1 Offset 2

--按title排列，从movies中找Director是John Lasseter的 ，条件是第三长的

***\*连表操作\****

数据库范式normalization：数据表设计的规范

多表连接技术（多表联合查询）JOINs

主键primary key（唯一属性）

INNER JOIN another_table 		--内连接

 ON mytable.id = another_table.id （两个表合并）

 

Outer Joins			--外连接（会保留不能匹配的行）

左连接LEFT JOIN（保留A）

右连接RIGHT JOIN（保留B）

全连接FULL JOIN（全保留）

Is Null/Is Not Null			--用NULL填充不存在的数据

As 			--取别名

 

***\*在查询中用到\*******\*包含表达式的例子\****

SELECT  particle_speed / 2.0 AS half_particle_speed (对结果做了一个除2）

FROM physics_data

WHERE ABS(particle_position) * 10.0 >500

​      （条件要求这个属性绝对值乘以10大于500）;

 

| Function                                  | Description                                                  |
| ----------------------------------------- | ------------------------------------------------------------ |
| **COUNT(*****)**, **COUNT(***column***)** | 计数！COUNT(*) 统计数据行数，COUNT(column) 统计column非NULL的行数. |
| **MIN(***column***)**                     | 找column最小的一行.                                          |
| **MAX(***column***)**                     | 找column最大的一行.                                          |
| **AVG(***column*)                         | 对column所有行取平均值.                                      |
| **SUM(***column***)**                     | 对column所有行求和.                                          |

 

分组统计 ：Group By 数据分组统计

 

 

**用HAVING对分组后的数据进行筛选**

SELECT group_by_column, AGG_FUNC(column_expression) AS aggregate_result_alias, …

FROM mytable

WHERE condition

GROUP BY column

HAVING group_condition;

 

**此条包含SQL所有语法**

```sql
SELECT DISTINCT column, AGG_FUNC(column_or_expression), …

FROM mytable//从上到下执行顺序

  JOIN another_table

   ON mytable.column = another_table.column

  WHERE constraint_expression

  GROUP BY column

  HAVING constraint_expression

  ORDER BY column ASC/DESC

LIMIT count OFFSET COUNT;

```

 

 

资源:

了解篇——[廖雪峰网站SQL入门篇（概述）](https://www.liaoxuefeng.com/wiki/1177760294764384)

基础篇——1.[语法手册（过一遍）](http://www.xuesql.cn/static/金老师手册.html)		 [自学SQL网lesson1-12](http://www.xuesql.cn/)		 [50题基础刷题](https://zhuanlan.zhihu.com/p/53302593)

理论篇——[廖雪峰网站SQL关系模型](https://www.liaoxuefeng.com/wiki/1177760294764384/1218728991649984)、查询数据、修改数据	 [MYSQL基础学习](https://zhuanlan.zhihu.com/p/53302593)

实战篇——[1.SQL、MYSQL环境搭建](https://zhuanlan.zhihu.com/p/37152572)	，[Navicat可视化工具](https://zhuanlan.zhihu.com/p/37155150)		 [图解SQL面试50题实战刷题（MYSQL和Navicat基础操作）](https://zhuanlan.zhihu.com/p/38354000)

 

 

操作类型：

DDL：定义数据（创建删除修改表）

DML：日常操作（添加删除更新数据）

DQL：查询数据

 

表table行rows 列columns

数据类型：整型、字符型、字符串、日期等、（NULL表示数据不存在）

 

 

每行数据为一条记录，一条记录有多个字段

 

***\*主键和外键：\******一对一、一对多、多对一、多对多的关系**

 

主键：关系表记录的唯一标识

联合主键：两个或更多的字段都设置为主键（允许有一列重复）

外键：通过class_id把数据与另一张表关联起来

***\**ALTER TABLE\**\***  **students**

***\**ADD CONSTRAINT\**\***  **fk_class_id**

***\**FOREIGN KEY\**\***  **(class_id)**

***\**REFERENCES\**\*** **classes (id);**

***\**ALTER TABLE\**\*** **students**

***\**DROP FOREIGN KEY\**\*** **fk_class_id;**

 

**注意：Windows不区分大小写，Linux/Unix区分大小写**

**任意两条记录不能重复**；不使用任何业务相关的字段作为主键；外键约束会降低数据库的性能

 

 

**创建索引**

***\**ALTER TABLE\**\*** **students**

***\**ADD INDEX\**\*** **idx_score (score)**



**查询**queries（字段选择）：

 

SELECT语法：

SELECT column（列名）, another_column, …

FROM mytable（表名）;

条件查询constraints

from

where对原始表筛选

having对分层汇总后的结果做筛选

连接语句：and和 or或

条件子句where

比较运算符：

=等于 >=大于等于 <=小于等于 !=不等于 >大于 <小于

确定（连续）范围：between ...and...

字符匹配（模糊查询）：

like %任意个字符 _一个字符

判断是否为空 is null

多个查询条件 and or

分组查询 group by / having

结果呈现 order by（排序）/ limit（限制条数）

 

连接语句 left/right/inner join

执行优先级

 

Hive单表查询完整结构：

SELECT<目标列名序列,函数>

FROM<表名>

WHERE<分区条件与检索条件>

[GROUP BY<分组依据列>]

[ORDER BY<排序依据列>]

[LIMIT N<只看结果的前N条>]

 

聚合函数：

count（id）统计表中id个数

count（distinct id）统计表中id个数（去重）

max（id）最大值min（id）最小值

sum（id）求和avg（id）平均值

 

count+distinct+if实现统计

sum+if实现分组统计（这里sum可以替换为其他聚合函数）

case when大量变形操作

 





#### MySQL

**1、安装MYSQL**

**2、连接MYSQL数据库**

**3、用户管理相关的命令**

**4、** **创建结构**：

​	A.**数据库**

show databases;  # 用来查看所有的数据库

create database <dbname> charset=utf8;  # 创建一个新的数据库，并指定编码格式为 utf8

use <dbname>  # 切换数据库

drop database <dbname>

alter database <dbname> charset=utf8;  # 修改数据库的编码方式

​	B.***\*表格\****

create table <tablename>(

id int primary key auto_increment,  # int类型的字段id，主键自增

name varchar(128),   # 至少要写字段的名字以及类型，

tel varchar(32) unique,  # 字段tel,有唯一约束

)

 

desc <tablename>;

describe <tablename>; #查看表结构

 

alter table <tablename> drop <字段名>;

show create table <talbename>; # 查看建表语句

drop table <tablename>  # 删除表格

***\*修改表格属性\*******\*:\****

alter table <tablename> rename <namename>  # 修改表格的名字

alter table <tablename> rename to <newdbname.newtablename># 将一个表移动到一个新的数据库里

alter table <tablename> add <字段名> <类型> [属性]  # 新增一个字段

alter table <tablename> add <字段名> <类型> [属性] first

alter table <tablename> add <字段名> <类型> [属性]  after <字段名>

alter table <tablename> change <字段名> <新名字> <属性> # 用来修改字段的名字和属性

alter table <tablename> modify <字段名> <属性>  # 用来修改字段的属性

 

 

简介：

MYSQL关系型数据库（本质上是软件）：多表关联
使用C/C++编写，平台可移植（支持Linux、Windows、MacOS、Solaris等）；支持多种编程语言：C/C++/Python/JAVA/Perl/PHP/Ruby；支持多线程；优化了SQL查询算法；

 

基于Linux系统下：

Sudo apt-get install mysql-server 安装数据库

 

MySQL查询：

条件/排序/聚合函数/分组/分页/连接查询/自关联/子查询

MySQL编码和数据类型：
字符集（数据存储和传输）：ASCII / LATIN1 / GB2312 / GBK / UTF-8 / UTF8MB4

查看mysql系统支持的字符集： mysql> show variables like 'character_%'; 

校对集（字符比较）：

 

数据类型：

整型：TINYINT / SMALLINT / MEDIUMINT / INT/INTEGER / BIGINT

浮点型：FLOAT / DOUBLE  定点数：DEC(M,D) / DECIMAL(M,D) 位类型：BIT(M)

字符串类型：

枚举类型enum：多选一（前端的单选框）**限制了可选值以节省空间提高了运行效率**

集合set：最多64个成员，类似于复选框

时间类型：DATE / DATATIME / TIMESTAMP / TIME / TEAR / TIMESTAMP
布尔型：bool型1 / 0
列的属性：null / not null 插入的值是否为空
SQL注释：单行 --  多行 /* */  MYSQL独有单行注释  #

 

**算术运算符**：+  -  *  /  %

**比较运算符**：= 等于（常规比较）、 <>或!= 不等于 、 <=> NULL安全的等于 、 <小于 、 <=小于等于 、 

\> 大于、 >=大于等于 、 BETWEEN存在于指定范围（范围比较） 、 IN存在于指定集合 、

 IS NULL 为NULL 、 IS NOT NULL 不为NULL 、 LIKE 通配符匹配（模糊比较） 、 REGEXP或RLIKE 正则表达式匹配

**逻辑运算符**：非：NOT或！  与：AND或&&  或： OR或||  异或： XOR

 

 

 

 

 

Python连接数据库：Python插件：PyMySQL

 

列——字段、行——记录、唯一标识——主键



### 八 网络编程



Socket网络编程 / NetAssist网络调试助手

网络通信与网络编程/IP地址/子网掩码/端口号/Socket/TCP/UDP/

```python
# 局域网的私网IP范围
10.0.0.0～10.255.255.255
172.16.0.0～172.31.255.255
192.168.0.0～192.168.255.255
```

```Python
# UDP网络程序发送数据
import socket
# 1. 创建一个UDP的socket连接
udp_socket = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
# 2. 获取用户输入的内容
data = input('请输入内容')
# 3. 准备接收方的地址和端口号
addr = ('127.0.0.1', 8080)
# 4. 将用户的输入内容进行编码，并发送到指定地址和端口
udp_socket.sendto(data.encode('gbk'), addr)
# 5. 接收传递过来的消息，并指定接受的字节大小
recv_data = udp_socket.recvfrom(1024)
# 6. 接收到的对象是一个元组，元组里有两个元素
print(recv_data)
# 6.1 元组里的第一个数据显示接收到内容
print(recv_data[0].decode('gbk'))
# 6.2 元组里的第二个数据显示发送方的地址和端口号
print(recv_data[1])
# 7. 关闭socket连接
udp_socket.close()
```



### 补充



##### `__init__.py` 

导包作用:让一个呈结构化分布(以文件夹形式组织)的代码文件夹变成可以被导入`import`的软件包

##### JSON

使用 JSON (JavaScript Object Notation)轻量级文本数据交换格式

的文件存储进度数据 ,键值对{string-value}合法格式:

```json
{
"type1": "string",
'type2': 31,	//单双引号都行(注意!JSON不支持注释)
"type3": {"name":"张三"},
"type4": ["张三","李四"],	//花中括号都行
"type5": true,	
"type6": null,
	}

```

##### py程序打包exe

```cpp
pyinstaller参数集合：

–icon=[图标路径](http://www.icontuku.com/)（pyinstaller -F --icon=my.ico XXXX.py）
-F 打包成一个exe文件
-w 小写，使用窗口，无控制台
-c 使用控制台，无窗口
-D 创建一个目录，里面包含exe以及其他一些依赖性文件 
-i  这里的i也是小写的，意思是忽略打包过程中遇到的错误，就是遇到错误也继续执行
```

##### Python术语表

| ABC                  | 编程语言                |
| -------------------- | ----------------------- |
| BOM                  | 字节序标记              |
| CPython              | C语言实现的Python解释器 |
| CRUD                 | 程序四种基本操作        |
| dunder               | 首尾两个下划线的读法    |
| listcomp             | 列表推导                |
| ORM                  | 对象关系映射器          |
| PyPI                 | Python包索引            |
| PyPy                 | Python包解释器          |
| YAGNI                | 不实现非立即需要的功能  |
| bound method         | 绑定方法                |
| codec                | 编码解码器              |
| mutator              | 变值方法                |
| aliasing             | 别名                    |
| parallel assignment  | 并行赋值                |
| ABC                  | 抽象基类                |
| Initializer          | 初始化方法              |
| storage attribute    | 储存属性                |
| accessor             | 储存方法                |
| code smell           | 代码异味                |
| singleton            | 单例                    |
| import time          | 导入时                  |
| iterator             | 迭代器                  |
| lazy                 | 惰性求值                |
| binary sequence      | 二进制序列              |
| generic function     | 泛函数                  |
| byte string          | 字节字符串              |
| decorator            | 装饰器                  |
| referent             | 指示对象                |
| truthy               | 真值                    |
| tuple unpacking      | 元组拆包                |
| metaprogramming      | 元编程                  |
| metaclass            | 元类                    |
| user-defined         | 用户定义的              |
| refcount             | 引用计数                |
| first-class function | 一等函数                |
| duck typing          | 鸭子类型                |
| serialization        | 序列化                  |
| virtual subclass     | 虚拟子类                |
| parameter            | 形参                    |
| argument             | 实参                    |
| shallow copy         | 浅复制                  |
| deep copy            | 深复制                  |
| generator            | 生成器                  |
| generator expression | 生成器表达式            |
| generator function   | 生成器函数              |
| view                 | 视图                    |
| considered harmful   | 视为有害                |
| context manager      | 上下文管理器            |



## B   --基于Tkinter的爬虫和数据分析与可视化项目-- 





## C 专业分支篇

### 爬虫



**爬虫spider——（网络）数据采集程序**

| C/S            | urllib        | Fidder            |
| -------------- | ------------- | ----------------- |
| http/https     | request       | NetAssist         |
| TCP/IP         | re,bs4        | APK               |
| cookie/Session | beautifulSoup | APP               |
| URL            | MonoGo DB     | tesseract         |
| HTML/CSS       | Thread        | Charles           |
| CSS偏移        | Selenium      | EditThisCookie    |
| JSON           | Scrapy        | Taggle JavaScript |
| JavaScript     | redis         |                   |
|                | xpath         |                   |



#### **一	概述** 

**数据来源**：Web服务器（Nginx/Apache）、数据库服务器(MySQL、Redis)、索引库（ElastichSearch）、大数据（Hbase/Hive）、视频/图片库(FTP)、云存储等

**技术**：多（单）线程/进程、网络请求库、数据解析、数据存储、任务调度等。

**用途**：测试：接口测试、功能性测试、性能测试和集成测试。

**原理**：（User-Agent指定请求头浏览器版本）伪造成浏览器向Web服务器发起HTTP请求打开网页获取内容，根据数据类型解析存储[获取-解析-保存]

**分类**:	

通用爬虫:抓取整个页面数据

聚焦爬虫:整理指定局部内容

增量式爬虫:监测网站数据更新

#### **二	工具**（库）

网络请求：urllib / requests / urllib3 / selenium / appium

数据解析：re正则 / xpath(基于元素)/ bs4 / json

数据存储：pymysql / mogodb / elasticsearch

多任务库：多线程threading / 线程队列 queue / 线程 asynio / gevent / eventlet

爬虫框架：scrapy / scrapy-redis分布式（多机爬虫）

反爬：  UA（User-Agent）策略	|	登录限制（Cookie）策略	|	请求频次（IP代理）策略	|	验证码（图片-云打码，文字或物件图片选择、滑块）策略	|	动态js（Selenium/Splash/api接口）策略

 

**补充:审查元素**：查出链接网页的规律用Chrome浏览器网页审查元素：在HTML网页右键审查元素可以打开HTML（CSS、JavaScript）源代码进行网页元素修改；刷新页面可以恢复（**需要一些前端基础知识**）





urllib.request 模块:模拟浏览器发请求

- urlopen(url | request: Request,  data=None)  data是bytes类型
- urlretrieve(url,  filename) 下载url的资源到指定的文件
- build_opener(*handlder)  构造一个不同处理组成的伪浏览器对象
  - opener.open(url|request, data=None)  发起请求
- Request 构造请求的类

urllib.parse模块

- quote(txt)  将中文字符串转成url编码
- urlencode(query: dict) 将参数的字典转成url编码，结果是key=value&key=value形式，即以 `application/x-www-form-urlencoded`作为url编码类型。

```python
from urllib.request import urlopen

# 发起网络请求
resp = urllopen('http://www.hao123.com')
assert resp.code == 200
print('请求成功')
# 保存请求的网页
# f 变量接收open()函数返回的对象的__enter__()返回结果
with open('a.html', 'wb') as f:
     f.write(resp.read())
```



- HTTPHandler HTTP协议请求处理器
- ProxyHandler(proxies={'http': 'http://proxy_ip:port'}) 代理处理
- HTTPCookieProcessor(CookieJar())
  - http.cookiejar.CookieJar 类

请求方法返回的对象是Respose

Xpath

xpath属于xml/html解析数据的一种方式， 基于元素（Element）的树形结构(Node > Element)。选择某一元素时，根据元素的路径选择，如 `/html/head/title`获取`<title>`标签。(pip install lxml)

绝对路径/相对路径

```python
//title/text()	# 提取文本
//img/@href	# 提取属性
# 位置条件
//meta[1]//@content	# 获取第一个<meta>标签
//meta[last()]//@content	# 最后一个
//meta[postition()-2]/@content	# 倒数第二个
//meta[position()<3]//@content	# 前三个
//img[@class="circle-img"]	#查找 class为circle-img的<img>标签
```



#### 三 网络编程

TCP/IP

#### 四 Http服务器

User-Agent 请求载体的身份标识

Connection:请求完毕后是否断开连接

content-tpye:服务器响应回客户端的数据类型

http/https:安全协议/安全协议(加密方式



- urllib库

  - request.urlopen()|urlretrieve()|Request|build_opener()|HTTPHandler|HTTPCookieProcessor(http.cookiejar.Cookiejar())|ProxyHandler(proxies={})
  - parse.quote()|urlencode()

- requests库(接口测试)

  - 依赖urllib3(封装了很多类-OOB)
  - request(method, url, params, data, json, files, headers,cookies, auth, proxies)
  - get(url, params, headers, proxies)
  - post(url, data, json, headers, proxies, cookies,files)
  - put(url, data, json, headers, proxies, cookies, files)
  - delete(url)
  - session()  用于存储Cookie, 可以与服务器建立长连接`Connection: keep-alive`请求或响应头。

- 请求头和响应头

  - 请求头

    ```
    # 请求头原始报文的第一行
    # GET / HTTP/1.1
    HOST: www.baidu.com
    Accept: text/html,text/*
    Referer: 
    X-Requested-with: XMLHTTPRequest
    User-Agent: 
    Cookie: 
    Content-Type:
    Content-Length:
    ```

  - 响应头(Web后端服务)

    ```
    # 原始报文的第一行
    # HTTP/1.1 200 OK
    Content-Type: text/html;charset=utf-8
    Content-Length:
    Set-Cookie: 
    Date:
    Server: 
    Cookie: 
    ```

#####  数据解析

- re解析提取

  - re.search()
  - re.findall()

- xpath提取(Element)

  - rootElement = lxml.etree.HTML(html_content)  节点对象
  - 节点对象的.xpath()提取数据
    - `/a/b/c`
    - `//div/ul//a`
    - `./li/a/@href | ./li/a/text()` 
    - `./li[1]`
    - `./li[position()<4]`
    - `./li[last()-1]`
    - `//div[@class="abc"]`
    - `//div[starts-with(@class, "abc")]`
    - `//div[ends-with(@class, "ddd")]`

- bs4( Tag )

  - rootTag = BeautifulSoup(html_content, 'lxml')

  - find('标签名'， class\_|id_)|find_all()
  - selector(CSS选择器)
  - bs4.element.Tag对象的属性
    - text|string|get_text()
    - attrs|Tag[]|Tag.get("属性名"， 默认属性值)
    - contents 所有的文本子节点
    - descendants 所有子标签节点对象

#####  数据存储

- pymysql
- csv (csv.DictWriter|csv.DictReader)
- json
- excel( xlwt|xlrd )

#####  爬虫框架

- Selenium (UI自动化测试工具)

  - 网络请求

  - 元素查找

    - find_element[s]_by_id|name|class_name|tag_name|xpath|css_selector()|link_text()

    - find_element(By, value) 查找第一个元素

      selenium.webdriver.common.by.By

    - find_elements(By, value) 查找所有元素

  - 事件交互（输入、点击、滚动、截屏、切换窗口）

  - 等待UI元素出现（用于等待Ajax加完数据）

    - selenium.webdriver.support.ui
    - selenium.webdriver.support.excepted_conditions as ec

    ```python
    ui.WebDriverWait(driver, timeout).until(
       ec.visibility_of_all_elements_located(
       	(By, value)
       ),
       timeout_msg
    )
    ```

- Scrapy|Scrapy-Redis

  - 五大核心组件两个中间件

    ```
    - Engin
    - Scheduler
    - Spider 
    - Downloader
    - ItemPipeline
    ```

    

    ```
    SpiderMiddlerware
    	- process_spider_input(self, response, spider)
    	- process_spider_output(self, response, results, spider)
    	- process_spider_exception(self, resposne, exct, spider)
    	- process_start_requests(self, start_reques
    	ts, spider)
    ```

    

    ```
    DownloaderMiddleware
    	- process_request(self, request, spider)
    	- process_response(self, request, response, spider)
    	- process_exception(self, request, excpt, spider)
    ```

    两个中间件都存在的方法

    ```
    @classmethod
    from_crawler(cls, crawler)
    ```

  - 解析数据时

    - response.css()|xpath()  返回SelectorList或Selector
    - Selector对象的方法
      - get()
      - extract() 
      - extract_first()
      - css()|xpath()

  - scrapy.Response对象的属性

    - status
    - encoding 可以指定字符集编码
    - headers
    - cookies
    - text 
    - body

  - scrapy.Request初始化参数

    - url
    - callback 指定回调函数
    - meta   向parse解析方法回传数据的dict类型的元数据
    - headers
    - cookies
    - priority  请求优先级
    - dont_filter 是否检查过滤重复的URL

  - 两个爬虫类

    - scrapy.Spider
      - 重写parse()
      - 指定start_urls = []
    - scrapy.spiders.CrawlSpider
      - 指定start_urls-> list 和 rules -> tuple
      - scrapy.spiders.Rule类初始化参数
        - link_extractor
          - scrapy.linkextractors.LinkExtractor 初始化参数
            - allow
            - deny
            - restrict_xpaths
            - restrict_css
        - callback: str
        - follow: bool

- 反爬虫的策略

  - UA （百度、安居）
  - Cookie
  - Referer（读书网的图片资源下载）
  - IP代理
  - 字体CSS加密(大众点评)
  - 图片验证码
  - 滑块验证码
  - 动态JS
  - 短信验证码

- 分布式爬虫

  - scrapy-redis 消息中间件使用redis

- 爬虫的部署【Linux熟悉】

  - 云服务器部署
  - docker部署
  - scrapyd部署

二、mongodb

##### docker部署

```
docker pull mongo
```



```
docker run -itd --name mongo_server1 -p 27017:27017 mongo
```

如果是在云服务启动的，则在`服务器的安全组规则`中添加`27017`端口访问的规则。

#####  数据结构

- 文档：  指一条数据， 在javascript的以js对象来表示，在python以dict对象来表示。
- 集合:     指多条数据组成的对象，在javascript中以js数组表示，在python以list对象表示。
- 数据库： 多个集合组成了库



#####  常用操作

- show dbs

- show collections

- use dushu  打开或创建dushu数据库

- db.createCollection('集合名')

- db.集合名.drop()

- db.dropDatabase()

- db.集合名.insert()|save()

- db.集合名.update(条件{}, 更新的数据{ $set: { }}, upsert, multi)

  - upsert 为真时，当条件没有匹配数据时，将更新的数据插入到集合中, 反之为假时，则什么也不做。
  - multi, 为真时， 当条件匹配多条数据时，将会更新所有的数据，反之，只更新每一条数据。

- db.集合名.remove(条件 { })

  删除user集合中文档的name属性包含`成`所有的记录

  ```js
  db.user.remove({name: {$regex: '成'}})
  ```

- db.集合名.find(条件{ }， 保留属性{name: 1}).pretty()

  - 逻辑关系
    - $or
    - $ne
    - $lt 
    - $gt
    - $lte
    - $gte
  - 正则表示
    - $regex









### Linux

#### 系统安装

A：虚拟机安装Linux Ubuntu开发系统（未采纳）

B：电脑双系统https://www.cnblogs.com/masbay/p/11627727.html

基于Windows10安装Linux Ubuntu 双系统

基本信息：DELL Ispiron 5488 单硬盘（C盘 D盘）WIndows 系统UEFI格式

工具：

UItralSo 软牒通 软件(用软牒通向U盘写入镜像文件)

U盘 （>2G)

Ubuntu镜像文件 ：Ubuntu-20.04.2.0-desktop-cmd64.iso

Windows(NIFS)分区：压缩卷 D	80G用来装新系统

*分区是因为两个系统文件存储格式不同，防止混乱* 

```
BIOS boot manager(F12快捷键)
	--Security boot Secure		[Disabled]
	--Intel RST					[Disabled]
System Configuration	--SATA Operation
```

——双系统切换：

Windows10 	RAID ON	boot manager

Ubuntu20.4	ACHI		   ubuntu



Set Individual OS(Ubuntu):
Language(语言)/regon（地区）/keyboard(键盘)/Account(账户)/Password(密码)

Ubuntu 分区（手动分区）：

​	efi		200MB	逻辑分区/起始位置	安装启动项

​	swap	8G		   逻辑分区/起始位置	交换空间

​	/			40G		主分区/起始位置		ext4日志文件系统（根目录）

​	/home  剩余空间 逻辑分区/起始位置   ext4日志文件系统（存储）

  

#### 开发环境

##### 快捷键

*快捷键HotKey可以在设置里自己配置*

Super+M启动终端		Alt+F4关闭所有窗口		Super+C 锁屏

Alt+Tab切换窗口		Alt+空格  直接切换		Ctrl +Print 截图剪切

Shift+Super+S 屏幕截图		Ctrl+ Super +D最小化所有窗口



##### Shell指令

1.程序安装：

基于Debian(Ubuntu)的deb或源文件（rpm基于Red hat)

deb包安装 dpkg -i xxx		卸载 dpkg -r xxx 

2.常用程序

Ubuntu Software

PyCharm Professional Edition/Visual Studio Code/Vim

Typora /FireFox/Google Chrom



3.Shell 常用指令





















#### 常见问题

##### 网络DNS配置

##### 信息转移

##### 播放视频









解压文件

```

一 常用tar命令
# 压缩文件 file1 和目录 dir2 到 test.tar.gz
tar -zcvf test.tar.gz file1 dir2
# 解压 test.tar.gz（将 c 换成 x 即可）
tar -zxvf test.tar.gz
# tar -zxvf flash_player_npapi_linux.x86_64.tar.gz
# 列出压缩文件的内容
tar -ztvf test.tar.gz 

-z : 使用 gzip 来压缩和解压文件
-v : --verbose 详细的列出处理的文件
-f : --file=ARCHIVE 使用档案文件或设备，这个选项通常是必选的
-c : --create 创建一个新的归档（压缩包）
-x : 从压缩包中解出文件


二 Windows zip rar

rar
# 压缩文件
rar a -r test.rar file
# 解压文件
unrar x test.rar
zip
# 压缩文件
zip -r test.zip file
# 解压文件
unzip test.zip
a : 添加到压缩文件
-r : 递归处理
x : 以绝对路径解压文件
```





操作系统OS



### 数据分析



##### Excel

Python中与excel相关的模块：

excel插件：Wind数据

——xlrd库：从excel中读取数据，支持xls、xlsx
——xlwt库：对excel进行修改操作，不支持对xlsx格式的修改
——xlutils库：在xlw和xlrd中，对一个已存在的文件进行修改。
——openpyxl：主要针对xlsx格式的excel进行读取和编辑。
——xlsxwriter
pip install openpyxl，xlrd，xlwt安装环境


Excel中的三大对象：

    WorkBook：工作簿对象
    Sheet：表单对象
    Cell：表格对象

常用操作：

import openpyxl

创建一个工作簿

wb = openpyxl.Workbook()

创建一个test_case的sheet表单

wb.create_sheet('test_case')

保存为一个xlsx格式的文件

wb.save('cases.xlsx')

读取excel中的数据

第一步：打开工作簿

wb = openpyxl.load_workbook('cases.xlsx')

第二步：选取表单

sh = wb['Sheet1']

第三步：读取数据

参数 row:行  column：列

ce = sh.cell(row = 1,column = 1)   # 读取第一行，第一列的数据
print(ce.value)

按行读取数据 list(sh.rows)

print(list(sh.rows)[1:])     # 按行读取数据，去掉第一行的表头信息数据

for cases in list(sh.rows)[1:]:
    case_id =  cases[0].value
    case_excepted = cases[1].value
    case_data = cases[2].value
    print(case_excepted,case_data)

关闭工作薄

wb.close()

##### Numpy



矩阵Matrix(维度数组)/科学计算

N维数组对象ndarray,一系列同类型数据的集合,以0下标为开始进行集合中元素的索引,axis N维数组

元素类型相同的表为axes,axes的数量称为rank

传入dtype可迭代对象创建Numpy数组:np.array/np.arange/np.line

不需要传入可迭代对象:

np.linspace等间距/np.random.random	0-1间随机数

amin/amax/ptp/percentile/median/mean/std

特殊操作:ravel	reshape	resize

数学模块:

线性代数numpy.linalg	傅里叶变换numpy.fft	矩阵对象numpy.matlib	随机函数numpy.random

数据类型

| 数据类型   | 描述                                                 |
| ---------- | ---------------------------------------------------- |
| bool_      | 布尔（True或False），存储为一个字节                  |
| int_       | 默认整数类型（与Clong相同；通常是int64或int32）      |
| INTC       | 与Cint（通常为int32或int64）相同                     |
| INTP       | 用于索引的整数（与Cssize_t相同；通常是int32或int64） |
| INT8       | 字节（-128至127）                                    |
| INT16      | 整数（-32768至32767）                                |
| INT32      | 整数（-2147483648至2147483647）                      |
| Int64的    | 整数（-9223372036854775808至9223372036854775807）    |
| UINT8      | 无符号整数（0到255）                                 |
| UINT16     | 无符号整数（0到65535）                               |
| UINT32     | 无符号整数（0到4294967295）                          |
| UINT64     | 无符号整数（0到18446744073709551615）                |
| float_     | float64的简写。                                      |
| float16    | 半精度浮点：符号位，5位指数，10位尾数                |
| FLOAT32    | 单精度浮点数：符号位，8位指数，23位尾数              |
| float64    | 双精度浮点：符号位，11位指数，52位尾数               |
| complex_   | complex128的简写。                                   |
| complex64  | 复数，由两个32位浮点数（实部和虚部）                 |
| complex128 | 复数，由两个64位浮点数（实部和虚部）                 |



```python
1. 构建对象
import numpy as np
（1）通过list
a = [[1, 2, 3], [1, 2, 4], [2, 3, 4]]
b= np.array(a)

(2)内置的方法
np.zeros((2, 3))# 构建2行3列的全0 数组
np.ones((2, 3))# 构建2行3列的全1 数组
np.empty((2, 3))# 构建2行3列的空值 数组
np.full((2, 3), 10)# 构建2行3列的数组,所有元素填充10
np.eye(4)# 构建类似于3*3的单位矩阵


（3）通过随机数
np.random.randn(2, 3)# 正态分布
np.random.randint(0, 10, (2, 3))#构建2行3列 在0-9的区间随机数值
np.random.rand((2, 3))#构建2*3 的数组， 数组里面的值服从均匀分布

（4）通过reshape()修改数组形状
np.arange(0, 100, 1).reshape(10, 10)	# 构建10*10的数组 值从0-100 间隔为1的递增(start/stop/step)

2.astype转换数据类型

In [31]: arr = np.array([1, 2, 3, 4, 5])

In [32]: arr.dtype
Out[32]: dtype('int64')

In [33]: float_arr = arr.astype(np.float64)

In [34]: float_arr.dtype
Out[34]: dtype('float64')

dtype查看数据类型

（1）同shape大小数组的运算
 o = arr + arr
 o = np.add(arr, arr)# 加
 p = arr - arr
 p = np.subtract(arr, arr) # -
 q = arr * arr
 q = np.multiply(arr, arr) # *

 r = arr / arr
 r = np.divide(arr, arr) # /

 (2) array和标量之间的运算
 arr + 1 #跟数组里面每个元素+1
 1 / arr # 取倒数
 arr ** 0.5 # 求平方根           arr ** 2  求平方



 2.取数   默认的如果没有'，'的则为行 例如arr[:5] 则为行 取前五行 arr[,:5] 取前五列
（1）切片索引
arr = np.arange(0, 100, 1).reshape(10, 10) # 构建10行10列，从0-100 逐渐递增的数组
b = arr[:5, 2:4]/arr[:5][:, 2:4]# 针对行和列做切片索引
c = arr[:5] # 针对行做切片索引     [0, 5]
b = arr[:, 2:4]# 针对列做切片索引  [ 2, 4)

(2) 花式索引
arr = np.arange(0, 100, 1).reshape(10, 10)
e = arr[[4, 2, 1], :]# 针对行花式索引,从第4 2 1 行排列开始 依次排序
e = arr[:, [-4, -2, -1]]# 针对列花式索引从1， 2， 4列开始排序 如果不加'-'则会从4，2，1开始排序
g = arr[[4, 3, 2], [1, 2, 4]]# 取出来的数对应的索引（4， 1）， （3， 2）， （2， 4）
i = arr[[4, 2, 1], :][:, [5, 2, 1]]# 取出来的数第4 2 1 行和 5 2 1 列 形成3*3数组        从第4行 的5 2 1 列组合一起 依次排序在第一行， 接着2 ，1行依次
i = arr[np.ix_([4, 2, 1], [5, 2, 1])]# 同上

（3）布尔型索引
I：针对数组里面的每一个位置进行bool判断
arr = np.arange(0, 100, 1).reshape(10, 10)
bool_arr = arr > 50 # 布尔型的矩阵
arr[bool_arr]#  取出来的数是一个列表， bool_arr 对应的TRUE的位置的数

II：只针对行或列进行bool取数
arr = np.arange(0, 6, 1).reshape(3, 2)
bool_inx = [True, False, True]
arr[bool_inx]# 针对行，通过bool取数      取行数为true的行
bool_col = [False, True]
arr[:, bool_col]# 针对列，通过bool取数

索引
a[1] # 取第二行数据
a[:2] # 取前两行数据
a[::2] # 每隔一行取一次
a[1:] # 取第2行后面所有行
a[[0,-1]] # 取第一行和最后一行
a[:,1] # 取第2列
a[:,1:3] # 取第2列到第3列
a[:,[0,3]] # 取第1列和第4列
a[1:3:,1:3] # 取第2、3行中的第2、3列


基本统计
df.sum(axis=0, skip_na=True) # a统计每一列的总和,零长度的数组的sum为0
df.count（）# 每一列的数量
series.count（）
df.mean() # 每一列的均值，算数平均数，零长度的mean为nan
df.median() # 中位数
df.describe() # 返回常规一些统计量：count、mean、min、max、分位数


导入/导出
np.save()/np.load()#存储或者导出一个array
np.savez()/np.load()#存储或者导出多个array
np.savetxt('filename.txt',arr,delimiter='分隔符')/np.loadtxt('filename.txt',delimiter='分隔符')#针对txt格式的导入和导出


元素值小于5的数值替换为0
np.where(a<5, 0, 1)


a = np.arange(12)
b=a 	# 赋值
b = a.copy()	# 深复制(产生新对象新内存操作互不影响)


间接排序： argsort和lexsort

In [174]: values = np.array([5, 0, 1, 3, 2])
In [175]: indexer = values.argsort()

lexsort跟argsort差不多， 只不过它可以⼀次性对多个键数组执⾏间接排
序（ 字典序） 。 假设我们想对⼀些以姓和名标识的数据进⾏排序：
In [182]: first_name = np.array(['Bob', 'Jane', 'Steve', 'Bill', 'Barbara'])
In [183]: last_name = np.array(['Jones', 'Arnold', 'Arnold', 'Jones', 'Walters
In [184]: sorter = np.lexsort((first_name, last_name))
In [185]: zip(last_name[sorter], first_name[sorter])

```







##### pandas

Excel



核心数据结构：

series（一维数组）数据+数据标签
DataFrame（二维数组）列，坐标轴+标签，即series的字典项

DataFrame行索引+列索引
cloumns列索引
index行索引

#函数实例
df1=df
print(df.dropna())

csv模式（存为utf-8）
encodeing="gbk"转码
head()显示前几行
shape获取数据表有几行几列
isnull查找缺失值
dropna删除存在缺失值的行
dropna（how='all'）)只删除全为空值的行
fillna(0)将缺失值填充为0

#根据不同的列填充把不同的值
df=df1
prnit("将比例填充为0，将时间填充为2020/7/20","*"*15)
dateTime_p=datetime.datetime.strptime("2020/9/25 00:00:00",r'%Y/%m/%d %H:%M:%S')

#删除名称相同的行
print(df.drop_duplicates(subset="名称",keep="last"),"\n")

#数据类型转换
print(df["a"].astype("float64"))

#更改索引值

df.index=[1,2,3,4,5]
df.set_index#不改变原来的表格，赋值
#重命名索引
df=df.rename(column={"a":"b"})#列

print(df.iloc[:,0:3],'\n')
原理：切片索引。
选择从第一列到第四列所有行（不含第四列）

print(df.loc[["行名称"]])
选择第几行

print(df[(df["条件"]>300) & (df["条件2"]>20)])

条件超过三百，条件2超过20

数值替换：
	df=df.replace(1,2)#将1替换成2

	多对一替换：
	df=df.replace([1,2],3)#将1,2替换成3
	
	多对多替换：
	df=df.replace({1:2,3:4})#将1替换成2,3替换成4

数值排序：
	print(df.sort_values(by=["app"],ascending=True))#按app升序排列
	print(df.sort_values(by=["app"，"apple"],ascending=[False,True]))#按app降序排列，按apple升序排列
	print(df.sort_values(by=["app"],asending=False/True,na_position="firat/last"))#按app从晚到早/从早到晚排，空值排在开始，最后

数值排名：
	rank（ascending=True/False，method="average"/first"/"min"/"max"）

数值删除：
	drop（axis=1/0）#1列0行

数值计数：



新插入行/列，行列互换，apply函数
求和、均值、方差、中位数等数值 
时间类型
数据分组和数据透视表 
表格的拼接
将结果导出为excel和csv文件





### 数据可视化



#####  Matplotlib

pyplot绘图数据可视化



```python
import matplotlib.pyplot as plt

plt.xlabel('设置横轴标签',fontsize=15)	# 标签大小15
plt.ylabel('设置纵轴标签')
plt.title('标题')
plt.legend()	# 生成默认图例
plt.legend(loc=0/1/2/3/4/5/6/7/8/9/10)	#不同数值对应不同位置
plt.bar(left,height,alpha=0,color,edgecolor,label,lw)
plt.figure()	# 画布
plt.show()	# 展示图形

```



可视化示例图:

OpenCV图片颜色转换/安德鲁曲线和平行坐标图/饼图/裁剪图片并旋转指定区域/弹簧张力高纬数据图/等值线图/点线图/二维核密度估计图/盒形图/热力图/小提琴图/分组散点图(random随机生成)/矩阵散点图/对角线直方图/多功能绘制/分类变量绘制/关键字控制/特定关系绘制/六边形图/圈图/热力地图/三维曲面图/散点图和直方图/时间序列图/直方图和密度函数/条形图/网状图/线性相关图/箱线图

##### mql_toolkits.mplot3d

```python
from mql_tookits.mplot3d import Axes3d
```



##### seaborn

##### sklearn

##### Scipy

##### Tableau

快速分析和迅捷商业智能:

##### Echarts

### 计算机网络

### 前端web

HTML / CSS / JavaScript

bootstrap框架 / js框架 / UI框架



### 人工智能AI

## C  --大作业--







## D 毕业设计



### 开题报告--选题

### 文献综述--收集资料(中&外)

参考文献

### 毕业论文

理论联系实际













