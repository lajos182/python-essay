**Python-essay**
<!-- TOC -->

- [1. 第一部分  Python简介与版本介绍](#1-第一部分--python简介与版本介绍)
    - [1.1. Python简介](#11-python简介)
    - [1.2. Python的设计模式](#12-python的设计模式)
    - [1.3. 单例模式](#13-单例模式)
        - [1.3.1. 使用`__new__`方法](#131-使用__new__方法)
        - [1.3.2. 使用装饰器](#132-使用装饰器)
        - [1.3.3. 使用元类](#133-使用元类)
        - [1.3.4. import方法](#134-import方法)
    - [1.4. Python中的元类(metaclass)](#14-python中的元类metaclass)
    - [1.5. Python自省](#15-python自省)
        - [1.5.1. 访问对象的属性](#151-访问对象的属性)
        - [1.5.2. `insepect`模块自省](#152-insepect模块自省)
    - [1.6. Python中的重载](#16-python中的重载)
    - [1.7. <a href="#1.7">新式类和旧式类</a>](#17-a-href17新式类和旧式类a)
    - [1.8. 鸭子模型](#18-鸭子模型)
    - [1.9. Python中的作用域](#19-python中的作用域)
    - [1.10. GIL线程全局锁](#110-gil线程全局锁)
    - [1.11. Python里的拷贝](#111-python里的拷贝)
    - [1.12. Python垃圾回收机制](#112-python垃圾回收机制)
        - [1.12.1. 引用计数](#1121-引用计数)
        - [1.12.2. 标记-清除机制](#1122-标记-清除机制)
        - [1.12.3. 分代技术](#1123-分代技术)
    - [1.13. Python2.x与Python3.x区别](#113-python2x与python3x区别)
- [2. 第二部分  Python语言基础](#2-第二部分--python语言基础)
    - [2.1. 标识符、变量与常量](#21-标识符变量与常量)
    - [2.2. 数据类型](#22-数据类型)
        - [2.2.1. 字符串格式化](#221-字符串格式化)
        - [2.2.2. 列表、元组、字典、集合的区别](#222-列表元组字典集合的区别)
    - [2.3. 运算符与流程控制](#23-运算符与流程控制)
        - [2.3.1. 运算符](#231-运算符)
        - [2.3.2. 流程控制](#232-流程控制)
    - [2.4. 函数使用](#24-函数使用)
        - [2.4.1. 函数的基本定义](#241-函数的基本定义)
        - [2.4.2. 变量作用域（LEGB）](#242-变量作用域legb)
        - [2.4.3. 内置函数、模块函数及基本数据结构函数](#243-内置函数模块函数及基本数据结构函数)
        - [2.4.4. 匿名函数](#244-匿名函数)
        - [2.4.5. 递归函数](#245-递归函数)
        - [2.4.6. 闭包与装饰器](#246-闭包与装饰器)
        - [2.4.7. 迭代器与生成器](#247-迭代器与生成器)
        - [2.4.8. 高级函数](#248-高级函数)
        - [2.4.9. 匿名、递归、闭包、高级函数总结](#249-匿名递归闭包高级函数总结)
        - [2.4.10. <a href='#IO编程'>目录管理与文件操作相关模块函数</a>](#2410-a-hrefio编程目录管理与文件操作相关模块函数a)
        - [2.4.11. 时间、日期和日历相关模块函数](#2411-时间日期和日历相关模块函数)
        - [2.4.12. 短信邮件相关模块函数](#2412-短信邮件相关模块函数)
    - [2.5. 模块使用](#25-模块使用)
    - [2.6. 异常处理](#26-异常处理)
    - [2.7. 面向对象(继承性、多态性、封装性)](#27-面向对象继承性多态性封装性)
        - [2.7.1. 类和对象的基本定义](#271-类和对象的基本定义)
        - [2.7.2. 常见的魔法函数](#272-常见的魔法函数)
        - [2.7.3. 枚举类的使用](#273-枚举类的使用)
        - [2.7.4. 类的继承](#274-类的继承)
        - [2.7.5. 多继承](#275-多继承)
        - [2.7.6. 多态性](#276-多态性)
        - [2.7.7. 封装性](#277-封装性)
        - [2.7.8. 类属性](#278-类属性)
        - [2.7.9. 类方法(classmethod)](#279-类方法classmethod)
        - [2.7.10. 静态方法(staticmethod)](#2710-静态方法staticmethod)
        - [2.7.11. 属性函数](#2711-属性函数)
        - [2.7.12. 对象判断](#2712-对象判断)
    - [2.8. IO编程](#28-io编程)
        - [2.8.1. 文件读写](#281-文件读写)
        - [2.8.2. `StringIO`和`BytesIO`](#282-stringio和bytesio)
        - [2.8.3. `bytes`函数的使用](#283-bytes函数的使用)
        - [2.8.4. 序列化](#284-序列化)
    - [2.9. 异常处理](#29-异常处理)
    - [2.10. 正则表达式](#210-正则表达式)
        - [2.10.1. 正则基础](#2101-正则基础)
        - [2.10.2. 正则规则](#2102-正则规则)
        - [2.10.3. 正则高阶](#2103-正则高阶)
    - [2.11. 进程](#211-进程)
        - [2.11.1. 进程简介](#2111-进程简介)
        - [2.11.2. 进程的并发与并行](#2112-进程的并发与并行)
        - [2.11.3. 进程管理](#2113-进程管理)
        - [2.11.4. 进程锁](#2114-进程锁)
        - [2.11.5. 自定义进程](#2115-自定义进程)
        - [2.11.6. 进程池](#2116-进程池)
        - [2.11.7. 数据共享](#2117-数据共享)
        - [2.11.8. 共享内存](#2118-共享内存)
        - [2.11.9. 多进程应用举例](#2119-多进程应用举例)
    - [2.12. 线程](#212-线程)
        - [2.12.1. 线程简介](#2121-线程简介)
        - [2.12.2. 线程模块](#2122-线程模块)
        - [2.12.3. 数据共享](#2123-数据共享)
        - [2.12.4. 线程锁](#2124-线程锁)
        - [2.12.5. 自定义线程](#2125-自定义线程)
        - [2.12.6. 定时线程](#2126-定时线程)
        - [2.12.7. 信号传递(`Event`)](#2127-信号传递event)
        - [2.12.8. 多核CPU(Python无法利用多线程实现多核任务)](#2128-多核cpupython无法利用多线程实现多核任务)
        - [2.12.9. 进程 vs 线程](#2129-进程-vs-线程)
    - [2.13. 异步`IO`](#213-异步io)
        - [2.13.1. 计算密集型与`IO`密集型](#2131-计算密集型与io密集型)
        - [2.13.2. 协程](#2132-协程)
        - [2.13.3. `asyncio`](#2133-asyncio)
        - [2.13.4. `async`/`await`](#2134-asyncawait)
        - [2.13.5. `aiohttp`](#2135-aiohttp)
    - [2.14. 网络编程](#214-网络编程)
        - [2.14.1. 相关概念](#2141-相关概念)
        - [2.14.2. `TCP`编程](#2142-tcp编程)
        - [2.14.3. `UDP`编程](#2143-udp编程)
- [3. 第三部分  Python与数据库](#3-第三部分--python与数据库)
    - [3.1. `MySQL`](#31-mysql)
        - [3.1.1. `MySQL`(`Ubuntu`)的安装](#311-mysqlubuntu的安装)
        - [3.1.2. 数据库定义语言(`DDL`)](#312-数据库定义语言ddl)
        - [3.1.3. 数据库操作语言(`DML`)](#313-数据库操作语言dml)
        - [3.1.4. 数据库查询语言(`DQL`)](#314-数据库查询语言dql)
        - [3.1.5. 数据控制语言(`DCL`)](#315-数据控制语言dcl)
        - [3.1.6. 多表联合查询](#316-多表联合查询)
        - [3.1.7. 多表联合操作](#317-多表联合操作)
        - [3.1.8. 事务处理语言(`DTL`)](#318-事务处理语言dtl)
        - [3.1.9. 外键索引(约束)](#319-外键索引约束)
        - [3.1.10. 数据清空(`DELETE`与`TRUNCATE`)](#3110-数据清空delete与truncate)
        - [3.1.11. 数据库的备份与恢复](#3111-数据库的备份与恢复)
        - [3.1.12. `Python`操作`MySql`](#3112-python操作mysql)
            - [3.1.12.1. `MySQLdb`](#31121-mysqldb)
            - [3.1.12.2. `mysqlclient`](#31122-mysqlclient)
            - [3.1.12.3. `PyMySQL`](#31123-pymysql)
            - [3.1.12.4. `peewee`](#31124-peewee)
            - [3.1.12.5. `SQLAlchemy`](#31125-sqlalchemy)
            - [3.1.12.6. `Flask-SQLAlchemy`](#31126-flask-sqlalchemy)
    - [3.2. `Redis`](#32-redis)
        - [3.2.1. `Redis`的安装与连接测试](#321-redis的安装与连接测试)
        - [3.2.2. `Redis`命令](#322-redis命令)
        - [3.2.3. `Python`操作`Redis`](#323-python操作redis)
            - [3.2.3.1. 简单连接](#3231-简单连接)
            - [3.2.3.2. 连接池](#3232-连接池)
            - [3.2.3.3. 详细操作命令](#3233-详细操作命令)
            - [3.2.3.4. 管道(`pipeline`)](#3234-管道pipeline)
            - [3.2.3.5. 发布和订阅](#3235-发布和订阅)
    - [3.3. `MongoDB`](#33-mongodb)
        - [3.3.1. `MongoDB`简介](#331-mongodb简介)
        - [3.3.2. `MongoDB`基本操作](#332-mongodb基本操作)
        - [3.3.3. `MongoDB`进阶操作](#333-mongodb进阶操作)
        - [3.3.4. 权限认证](#334-权限认证)
        - [3.3.5. `Python`操作`MongoDB`](#335-python操作mongodb)
- [4. 第四部分  Linux相关知识](#4-第四部分--linux相关知识)
    - [4.1. `Linux`系统简介](#41-linux系统简介)
    - [4.2. `Linux`目录结构及`vim`](#42-linux目录结构及vim)
    - [4.3. 文件操作](#43-文件操作)
        - [4.3.1. 常识命令](#431-常识命令)
        - [4.3.2. 查看文件](#432-查看文件)
        - [4.3.3. 文件及目录](#433-文件及目录)
        - [4.3.4. 用户及用户组](#434-用户及用户组)
    - [4.4. 文件权限](#44-文件权限)
    - [4.5. 文件搜索](#45-文件搜索)
    - [4.6. 系统服务](#46-系统服务)
        - [4.6.1. 压缩与解压](#461-压缩与解压)
        - [4.6.2. 网络服务](#462-网络服务)
        - [4.6.3. 服务监测](#463-服务监测)
        - [4.6.4. 进程管理](#464-进程管理)
        - [4.6.5. 防火墙(`ufw`)](#465-防火墙ufw)
        - [4.6.6. 远程连接(`ssh:22`)](#466-远程连接ssh22)
        - [4.6.7. 软件安装](#467-软件安装)
        - [4.6.8. 管道及`xargs`](#468-管道及xargs)
        - [4.6.9. 重定向](#469-重定向)
- [5. 第五部分  `shell`编程](#5-第五部分--shell编程)
    - [5.1. `shell`简介](#51-shell简介)
    - [5.2. `shell`变量](#52-shell变量)
    - [5.3. 变量类型](#53-变量类型)
    - [5.4. 字符串操作](#54-字符串操作)
    - [5.5. 数组操作](#55-数组操作)
    - [5.6. `seq`命令](#56-seq命令)
    - [5.7. `expr`命令](#57-expr命令)
    - [5.8. 各种运算](#58-各种运算)
    - [5.9. 分支结构](#59-分支结构)
    - [5.10. 循环结构](#510-循环结构)
    - [5.11. 函数使用](#511-函数使用)
- [6. 第六部分  Python-Flask框架](#6-第六部分--python-flask框架)
- [7. 第七部分  Python-Django框架](#7-第七部分--python-django框架)
- [8. 第八部分  Python-Tornado框架](#8-第八部分--python-tornado框架)
- [9. 第九部分  Python爬虫基础](#9-第九部分--python爬虫基础)
- [10. 第十部分  Python-Scrapy与分布式爬虫](#10-第十部分--python-scrapy与分布式爬虫)

<!-- /TOC -->
# 1. 第一部分  Python简介与版本介绍

## 1.1. Python简介

+ Python是一种**解释型**(不需要编译)、**面向对象**、**动态数据类型**的交互式语言，Python是由由荷兰人Guido van Rossum于1989年发明，第一个公开发行版发行于1991年。

+ **Python的优势**：

  + **易于学习**：Python有相对较少的关键字，结构简单，有明确定义的语法，学习起来相对简单。 
  + **易于阅读**：Python代码的定义比较清晰，易于阅读。 
  + **易于维护**：Python的成功在于它的源代码是相当容易维护。
  + **具有一个广泛的标准库**：Python的最大优势之一是具有丰富的库，可跨平台，兼容性较好。
  + **互动模式**：互动模式的支持，您可以从终端输入执行代码并获得结果的语言，互动的测试和调试代码的片段。 

  + **可移植**：基于其开放源代码的特性，Python已经被移植到许多平台。 
  + **可扩展性**：如果需要一段运行很快的关键代码，或者想要编程一些不愿开放的算法，你可以使用c或者c++完成那部分程序，然后从你的Python程序中进行调用。 
  + **GUI编程**：Python支持GUI可以创建和移植到许多系统调用。 
  + **可嵌入**：你可以将Python嵌入到c/c++程序中，让你的程序用户得到“脚本”的能力。

+ **缺点**：

  + **运行速度慢**：和C程序相比比较慢，因为Python是解释型语言，代码在执行时会一行一行的编译成CPU能理解的机器码，这个翻译过程非常耗时，所以很慢。而C程序是运行前直接编译成CPU能执行的机器码，所以非常快。

  +  **代码不能加密**：如果要发布Python程序，实际上就是发布源代码，这一点与C语言不同,C语言不能发布源代码，只需要把编译后的机器码（也就是windows上常见的xxx.exe文件）发布出去。要从机器码反推出C代码是不可能的，所以，凡是编译型的语言，都没有这个问题，而解释型的语言，则必

## 1.2. Python的设计模式

**设计模式的定义**：为了解决面向对象系统中重要和重复的设计封装在一起的一种代码实现框架,可以使得代码更加易于扩展和调用。

- **设计模式的基本要素**：模式名称、问题、解决方案、效果。

  **设计模式的六大原则**：	

  - 开闭原则：一个软件实体,如类,模块和函数应该对扩展开发,对修改关闭.既软件实体应尽量在不修改原有代码的情况下进行扩展。
  - 里氏替换原则：所有引用父类的方法必须能透明的使用其子类的对象。
  - 依赖倒置原则：高层模块不应该依赖底层模块,二者都应该依赖其抽象,抽象不应该依赖于细节,细节应该依赖抽象,换而言之,要针对接口编程而不是针对实现编程。
  - 接口隔离原则：使用多个专门的接口,而不是使用单一的总接口,即客户端不应该依赖那些并不需要的接口。
  - 迪米特法则：一个软件实体应该尽可能的少与其他实体相互作用。
  - 单一职责原则：不要存在多个导致类变更的原因.即一个类只负责一项职责。



**Python的设计模式**：

![the design pattern of python](https://github.com/lajos182/python-essay/blob/master/images/the%20design%20pattern%20of%20python.png)



二十三设计模式案例详情，可参考：https://www.cnblogs.com/Liqiongyu/p/5916710.html



## 1.3. 单例模式

> **单利模式**是一种常用的软件设计模式。在它的核心结构中只包含一个被称为单例类的特殊类。通过单例模式可以保证系统中一个类只有一个实例而且该实例易于外界访问，从而方便对实例个数的控制并节约系统资源。如果希望在系统中某个类的对象只能存在一个，单例模式是最好的解决方案。
>
> ```
> `__new__()`在`__init__()`之前被调用，用于生成实例对象。利用这个方法和类的属性的特点可以实现设计模式的单例模式。单例模式是指创建唯一对象，单例模式设计的类只能实例 **这个绝对常考啊.绝对要记住1~2个方法,当时面试官是让手写的.**
> ```



### 1.3.1. 使用`__new__`方法

`__new__`是真正创建实例对象的方法，所以重写基类的`__new__`方法，以此来保证创建对象的时候只生成一个实例 

```python
class Singleton(object):
    _instance = None
    def __new__(cls, *args, **kwargs):
        if cls._instance == super(Singlento, cls).__new__(cls, *args, **kwargs)
        return cls._instance

class Foo(Signleton):
    pass

foo1 = Foo()
foo2 = Foo()

print(foo1 is foo2) # True
```

### 1.3.2. 使用装饰器

装饰器维护一个字典对象instances，缓存了所有单例类，只要单例不存在则创建，已经存在直接返回该实例对象。

```python
def singleton(cls):
    instances = {}
    def wrapper(*args, **kwargs):
        if cls not in instances:
            instances[cls] = cls(*args, **kwargs)
        return instance[cls]
    return wrapper

@singleton
class Foo(object):
    pass

foo1 = Foo()
foo2 = Foo()

print(foo1 is foo2) # True
```

### 1.3.3. 使用元类

元类（参考：[深刻理解Python中的元类](http://blog.jobbole.com/21351/)）是用于创建类对象的类，类对象创建实例对象时一定会调用`__call__`方法，因此在调用`__call__`时候保证始终只创建一个实例即可，`type`是python中的一个元类。

```python
class Singleton(type):
    def __call__(cls, *args, **kwargs):
        if not hasattr(cls, '_instance'):
            cls._instance = super(Singleton, cls).__call__(*args, **kwargs)
        return cls._instance
 
 
class Foo(object):
    __metaclass__ = Singleton
 
 
foo1 = Foo()
foo2 = Foo()
 
print(foo1 is foo2)  # True
```

### 1.3.4. import方法

import作为python的模块，是天然的单例模式，因为模块在第一次导入时，会生成 `.pyc` 文件，当第二次导入时，就会直接加载 `.pyc` 文件，而不会再次执行模块代码。因此，我们只需把相关的函数和数据定义在一个模块中，就可以获得一个单例对象了。如果我们真的想要一个单例类，可以考虑这样做：

```python
class My_Singleton(object):
    def foo(self):
        pass
 
my_singleton = My_Singleton()
```

将上面的代码保存在文件 `mysingleton.py` 中，然后这样使用：

```python
from mysingleton import my_singleton
 
my_singleton.foo()
```

[**单例模式伯乐在线详细解释**](http://python.jobbole.com/87294/)

## 1.4. Python中的元类(metaclass)

这个非常的不常用,但是像ORM这种复杂的结构还是会需要的,详情请看:<http://stackoverflow.com/questions/100003/what-is-a-metaclass-in-python>，中文看这个解释很详细[深刻理解Python中的元类](http://blog.jobbole.com/21351/)

Python处处皆对象，类其实也是对象，使用`class`关键字时，Python会自动创建此对象。但与Python中的大多数内容一样，`type`为您提供了手动执行此操作的方法。[`type`](http://docs.python.org/2/library/functions.html#type)有一个完全不同的能力，它也可以动态创建类。`type`可以将类的描述作为参数，并返回一个类。

```python
type(类名, 类名的元组(针对继承的情况，可以为空), 包含属性的字典(名称和值))
>>> Foo = type('Foo', (), {'bar': True})
>>>	print(Foo)
True
>>> f = Foo()
>>> print(f)
<__main__.Foo object at 0x8a9b84c>
>>> print(f.bar)
True
```

## 1.5. Python自省

这个也是python彪悍的特性.

自省就是面向对象的语言所写的程序在运行时,所能知道对象的类型.简单一句就是运行时能够获得对象的类型.比如`type()`，`dir()`，`getattr()`，`hasattr()`，`isinstance()`

### 1.5.1. 访问对象的属性

`dir([obj])`：调用这个方法将返回包含obj大多数属性名的列表（会有一些特殊的属性不包含在内）。obj的默认值是当前的模块对象。

`hasattr(obj, attr)`：这个方法用于检查obj是否有一个名为attr的值的属性，返回一个布尔值。

`getattr(obj, attr)`：调用这个方法将返回obj中名为attr值的属性的值，例如如果attr为’bar’，则返回obj.bar。

`setattr(obj, attr, val)`：调用这个方法将给obj的名为attr的值的属性赋值为val。例如如果attr为’bar’，则相当于obj.bar = val。

```python
class Cat(object):

    def __init__(self, name, *args, **kwargs):
            self.name = name

    def sayHi(self):
        print(self.name)

cat = Cat('kitty')
print(cat.name)
cat.sayHi()
print(dir(cat)) # 获取实例的属性名，以列表形式返回
>>> ['__class__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__', '__lt__', '__module__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '__weakref__', 'name', 'sayHi']

if hasattr(cat, 'name'): # 检查实例是否有这个属性
    setattr(cat, 'name', 'tiger') # same as: a.name = 'tiger'
print(getattr(cat, 'name')) # same as: print(a.name)
getattr(cat, 'sayHi')() # same as: cat.sayHi()
```

### 1.5.2. `insepect`模块自省

`is{module|class|function|method|builtin}(obj)`：检查对象是否为模块、类、函数、方法、内建函数或方法。

`isroutine(obj)`：用于检查对象是否为函数、方法、内建函数或方法等等可调用类型。用这个方法会比多个is*()更方便，不过它的实现仍然是用了多个is*()。

`getmembers(object[, predicate])`：这个方法是dir()的扩展版，它会将dir()找到的名字对应的属性一并返回，形如[(name, value), …]。另外，predicate是一个方法的引用，如果指定，则应当接受value作为参数并返回一个布尔值，如果为False，相应的属性将不会返回。使用is*作为第二个参数可以过滤出指定类型的属性。

`getmodule(object)`：返回object的定义所在的模块对象。

`get{file|sourcefile}(object)`：获取object的定义所在的模块的文件名|源代码文件名（如果没有则返回None）。用于内建的对象（内建模块、类、函数、方法）上时会抛出TypeError异常。

`get{source|sourcelines}(object)`：获取object的定义的源代码，以字符串|字符串列表返回。代码无法访问时会抛出IOError异常。只能用于module/class/function/method/code/frame/traceack对象。

`getargspec(func)`：仅用于方法，获取方法声明的参数，返回元组，分别是(普通参数名的列表, *参数名, **参数名, 默认值元组)。如果没有值，将是空列表和3个None。如果是2.6以上版本，将返回一个命名元组(Named Tuple)，即除了索引外还可以使用属性名访问元组中的元素。

`getargvalues(frame)`：仅用于栈帧，获取栈帧中保存的该次函数调用的参数值，返回元组，分别是(普通参数名的列表, *参数名, **参数名, 帧的locals())。如果是2.6以上版本，将返回一个命名元组(Named Tuple)，即除了索引外还可以使用属性名访问元组中的元素。

`getcallargs(func[, *args][, **kwds])`：返回使用args和kwds调用该方法时各参数对应的值的字典。这个方法仅在2.7版本中才有。

`getmro(cls)`：返回一个类型元组，查找类属性时按照这个元组中的顺序。如果是新式类，与cls.`__mro__`结果一样。但旧式类没有`__mro__`这个属性，直接使用这个属性会报异常，所以这个方法还是有它的价值的。

`currentframe()`：返回当前的栈帧对象。

## 1.6. Python中的重载

引自知乎:<http://www.zhihu.com/question/20053359>

函数重载的目的：解决**可变参数类型**、**可变参数个数**两大问题。

另外，一个基本的设计原则是，仅仅当两个函数除了参数类型和参数个数不同以外，其功能是完全相同的，此时才使用函数重载，如果两个函数的功能其实不同，那么不应当使用重载，而应当使用一个名字不同的函数。

函数功能相同，但是参数类型不同，python 如何处理？答案是根本不需要处理，因为 python 可以接受任何类型的参数，如果函数的功能相同，那么不同的参数类型在 python 中很可能是相同的代码，没有必要做成两个不同函数。

函数功能相同，但参数个数不同，python 如何处理？大家知道，答案就是缺省参数。对那些缺少的参数设定为缺省参数即可解决问题。因为你假设函数功能相同，那么那些缺少的参数终归是需要用的。

## 1.7. <a href="#1.7">新式类和旧式类</a>

[stackoverflow]([stackoverflow](http://stackoverflow.com/questions/54867/what-is-the-difference-between-old-style-and-new-style-classes-in-python))

**在Python 2.1中，旧式类是用户可用的唯一风格。**

（旧式）类的概念与类型的概念无关：如果`x`是旧式类的实例，则`x.__class__` 指定类的类`x`，但`type(x)`始终是`<type   'instance'>`。

这反映了这样一个事实，即所有旧式实例独立于其类，都使用一个称为实例的内置类型实现。

**Python 2.2中引入了新式类，以统一类和类型的概念**。新式类只是用户定义的类型，不多也不少。

如果x是新样式类的实例，那么`type(x)`通常是相同的`x.__class__`（尽管不能保证 - 允许新样式类实例覆盖返回的值`x.__class__`）。

**引入新式类的主要动机是提供具有完整元模型的统一对象模型**。

它还具有许多直接的好处，例如能够对大多数内置类型进行子类化，或引入“描述符”，从而启用计算属性。

**出于兼容性原因，默认情况下类仍为旧式**。

通过将另一个新样式类（即类型）指定为父类来创建新样式类，或者如果不需要其他父类，则创建“顶级类型”对象。

除了返回的类型之外，新样式类的行为在许多重要细节中与旧样式类的行为不同。

其中一些更改是新对象模型的基础，就像调用特殊方法的方式一样。其他是针对兼容性问题之前无法实现的“修复”，例如在多重继承的情况下的方法解析顺序。

**Python 3只有新式的类**。

无论你是否是子类`object`，类都是Python 3中的新风格。这篇文章很好的介绍了新式类的特性: <http://www.cnblogs.com/btchenguang/archive/2012/09/17/2689146.html>

> 一个旧式类的深度优先的例子

```python
class A():
    def foo1(self):
        print('A')

class B(A):
    def foo2(self):
        pass
    
class C(A):
    def foo1(self):
        print('C')
        
class D(B, C):
    pass

d = D()
d.foo1()
>>> C
```

**按照经典类的查找顺序从左到右深度优先的规则，在访问d.foo1()的时候,D这个类是没有的..那么往上查找,先找到B,里面没有,深度优先,访问A,找到了foo1(),所以这时候调用的是A的foo1()，从而导致C重写的foo1()被绕过。但在新式类种，按照广度优先的原则，访问d.foo1()时，D没有，继续找B，发现B里面也没有foo1()，再找C， C中有foo1()，直接就调用该方法，输入结果就是C**。

## 1.8. 鸭子模型

`Python`崇尚鸭子类型，即‘如果看起来像、叫声像而且走起路来像鸭子，那么它就是**鸭子**

`python`程序员通常根据这种行为来编写程序。例如，如果想编写现有对象的自定义版本，可以继承该对象。

也可以创建一个外观和行为像，但与它无任何关系的全新对象，后者通常用于保存程序组件的松耦合度。

## 1.9. Python中的作用域

Python中，程序的变量并不是哪个位置都可以访问的，访问权限决定于这个变量是在哪里赋值的。变量的作用域决定了在哪一部分程序可以访问哪个特定的变量名称。Python的作用域一共有4种，分别是：

- L（Local） 局部作用域
- E（Enclosing）闭包函数外的函数中
- G（Global）全局作用域
- B（Bulit-in）内置作用域（内置函数所在模块的范围）

**Python执行时查找作用域的顺序是L-E-G-B**，即：先在局部找，局部找不到去局部外的局部(闭包)，然后是全局再到内建

```python
g_count = 0 # 全局作用域
def outer():
    o_count = 1 # 闭包函数外的函数中
    def inner():
        i_count = 2 # 局部作用域
```



## 1.10. GIL线程全局锁

线程全局锁(Global Interpreter Lock),即Python为了保证线程安全而采取的独立线程运行的限制,说白了就是一个核只能在同一时间运行一个线程.**对于io密集型任务，python的多线程起到作用，但对于cpu密集型任务，python的多线程几乎占不到任何优势，还有可能因为争夺资源而变慢。**

见[Python 最难的问题](http://www.oschina.net/translate/pythons-hardest-problem)

解决办法就是多进程和下面的协程(协程也只是单CPU,但是能减小切换代价提升性能).

## 1.11. Python里的拷贝



## 1.12. Python垃圾回收机制

`Python GC`主要使用引用计数（`reference counting`）来跟踪和回收垃圾。在引用计数的基础上，通过“标记-清除”（`mark and sweep`）解决容器对象可能产生的循环引用问题，通过“分代回收”（`generation collection`）以空间换时间的方法提高垃圾回收效率。

### 1.12.1. 引用计数

`PyObject`是每个对象必有的内容，其中`ob_refcnt`就是做为引用计数。当一个对象有新的引用时，它的`ob_refcnt`就会增加，当引用它的对象被删除，它的`ob_refcnt`就会减少.引用计数为0时，该对象生命就结束了。

优点:

1. 简单
2. 实时性

缺点:

1. 维护引用计数消耗资源
2. 循环引用

### 1.12.2. 标记-清除机制

基本思路是先按需分配，等到没有空闲内存的时候从寄存器和程序栈上的引用出发，遍历以对象为节点、以引用为边构成的图，把所有可以访问到的对象打上标记，然后清扫一遍内存空间，把所有没标记的对象释放。

### 1.12.3. 分代技术

分代回收的整体思想是：将系统中的所有内存块根据其存活时间划分为不同的集合，每个集合就成为一个“代”，垃圾收集频率随着“代”的存活时间的增大而减小，存活时间通常利用经过几次垃圾回收来度量。

Python默认定义了三代对象集合，索引数越大，对象存活时间越长。

举例： 当某些内存块M经过了3次垃圾收集的清洗之后还存活时，我们就将内存块M划到一个集合A中去，而新分配的内存都划分到集合B中去。当垃圾收集开始工作时，大多数情况都只对集合B进行垃圾回收，而对集合A进行垃圾回收要隔相当长一段时间后才进行，这就使得垃圾收集机制需要处理的内存少了，效率自然就提高了。在这个过程中，集合B中的某些内存块由于存活时间长而会被转移到集合A中，当然，集合A中实际上也存在一些垃圾，这些垃圾的回收会因为这种分代的机制而被延迟。

## 1.13. Python2.x与Python3.x区别

[Python2.x与Python3.x区别](https://github.com/lajos182/python-essay/blob/master/images/Python2.x%E4%B8%8EPython3.x%E7%9A%84%E5%8C%BA%E5%88%AB.pdf)

# 2. 第二部分  Python语言基础

## 2.1. 标识符、变量与常量

**标识符**：开发人员在程序中自定义的一些符合和名称，其实就是一串字符串，如变量名、函数名等

Python标识符规则：只能由数字、字符和下划线组成，开头不能是数字，不能是关键字，大小写敏感且见名知义，要遵循小驼峰原则。

![标识符](https://github.com/lajos182/python-essay/blob/master/images/Identifier.png)

```python
import keyword
print(keyword.kwlist) # 关键字列表
>>>['False', 'None', 'True', 'and', 'as', 'assert', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
```

**变量**：在程序运行过程中，其值可以改变的量。

变量命名原则：尽量做到见名知意、尽量使用英文、推荐使用全小写加下划线的方式，如`user_name`

**常量**：程序运行期间不会改变的数据，如`a = 1`。在python中没有常量，通常使用大写字母加下划线的方式模拟，如：`USER_NAME = 'xiaoming'`

![变量与常量](https://github.com/lajos182/python-essay/blob/master/images/variable%20and%20constant.png)

代码注释：单行注释（`# 注释内容`）、多行注释（`'''注释'''`, `"""注释"""`）

## 2.2. 数据类型

数据类型是为了处理不同的运算而存在，python中的数据类型有：**整型(int)**、**浮点(float)**、**字符串(str)**、**列表(list)**、**元组(tuple)**、**字典(dict)**、**集合(set)**、**空(NoneType)**

### 2.2.1. 字符串格式化

在 Python 3.6 之前，字符串格式化方法主要有两种：`%格式化` 和 `str.format()`，Python3.6提供了一种新的字符串格式化方法：`f-string`

- (1)`%-格式化`从 Python 刚开始时就存在了，堪称「一届元老」，但是 [Python 官方文档](https://link.zhihu.com/?target=https%3A//docs.python.org/3/library/stdtypes.html%23printf-style-string-formatting)中并不推荐这种格式化方式：

  > 这里描述的格式化操作容易表现出各种问题，导致许多常见错误（例如无法正确显示元组和字典）。 使用较新的格式化字符串文字或 str.format() 可以有助于避免这些错误。这些替代方案还提供了更强大，灵活和可扩展的格式化文本方法。

  ```python
  >>> name = 'lajos'
  >>> age = 18
  >>> 'hello, %s, your age is %s ?' %(name, age)
  'hello, lajos, your age is 18?'
  ```

- (2)`str.formar()`从Python2.6开始引入，它使用普通函数调用语法，并且可以通过 `__format__()` 方法为对象进行扩展。

  ```python
  >>> "hello, {}. you are {}?".format(name,age)
  'hello, hoxis. you are 18?'
  ```

  ```python
  >>> "hello, {1}. you are {0}?".format(age,name)
  'hello, hoxis. you are 18?'
  ```

  ```python
  >>> "hello, {name}. you are {age1}?".format(age1=age,name=name)
  'hello, hoxis. you are 18?'
  ```

  ```python
  >>> person = {"name":"hoxis","age":18}
  >>> "hello, {name}. you are {age}?".format(**person)
  'hello, hoxis. you are 18?'
  ```

- (3)`f-Strings`是指以 `f` 或 `F` 开头的字符串，其中以 `{}` 包含的表达式会进行值替换。f-string 里的 f 也许可以代表 `fast`，它比 %格式化方法和 str.format() 都要快：

  ```python
  >>> name = 'hoxis'
  >>> age = 18
  >>> f"hi, {name}, are you {age}" # 替换字符串
  'hi, hoxis, are you 18'
  >>> F"hi, {name}, are you {age}"
  'hi, hoxis, are you 18'
  
  >>> f"{name.lower()} is handsome." # 调用函数
  'hoxis is handsome.'
  
  >>> class Person:
  ...     def __init__(self,name,age):
  ...         self.name = name
  ...         self.age = age
  ...     def __str__(self):
  ...         return f"{self.name} is {self.age}" # 在类中使用
  ...     def __repr__(self):
  ...         return f"{self.name} is {self.age}. HAHA!"
  ...
  >>> hoxis = Person("hoxis",18)
  >>> f"{hoxis}"
  'hoxis is 18'
  >>> f"{hoxis!r}"
  'hoxis is 18. HAHA!'
  >>> print(hoxis)
  hoxis is 18
  >>> hoxis
  hoxis is 18. HAHA!
  
  
  >>> name = 'hoxis'
  >>> age = 18
  >>> status = 'Python'
  >>> message = {
  ...     f'hi {name}.'
  ...     f'you are {age}.'
  ...     f'you are learning {status}.'
  ... }  # 多行f-string
  >>>
  >>> message
  {'hi hoxis.you are 18.you are learning Python.'}
  ```

（4）`f-string`在python3.8中加入新特性，可以在表达式的末尾添加`=`,此时可以同时显示表达式和值

```pyton
>>> python = 3.8
>>> f'{python=}'
'python = 3.8'
```

### 2.2.2. 列表、元组、字典、集合的区别

|      | 特点                                                         |
| :--- | :----------------------------------------------------------- |
| 列表 | 列表是一组任意类型的值，按照一定的顺序组合而成； <br /> 通过索引来标识元素，第一个索引为0；需要注意的是索引可以是负值；<br /> 3列表中元素是任意类型的，包括列表类型； <br />可以进行合并，删除，索引，切片等操作； 5 定义表使用中括号。 |
| 元组 | 元组是任意对象的有序集合（这一点和列表相同）；<br />元组是不可变的（不能 增，删，改），但可以对元组进行合并；<br />元组的速度比列表要快；<br />定义元组使用小括号；<br />需要注意的是定义一个元素时需要加上逗号，例如tuple=（333，）。 |
| 字典 | 字典是通过键值对进行存储的，所以字典没有顺序；<br />字典是通过键值进行索引的且键值必须唯一； <br />字典可以进行增，删，改，查等操作，可以包含任意其他类型；<br />定义字典使用大括号，各个键值对之间使用逗号隔开。 |
| 集合 | 集合是简单对象的无序不重复元素集合； <br />集合分为可变集合set（元素是可哈希的），不可变集合frozenset（元素不可哈希）；<br />可以进行去除重复元素；<br />可以进行并集，交集，差集等。 |

字典的创建方法：

+ 直接创建：`dict = {'name': 'earth', 'port': 80}`

  ```python
  class dict(**kwarg)             # **kwargs -- 关键字
  class dict(mapping, **kwarg)    # mapping -- 元素的容器。
  class dict(iterable, **kwarg)   # iterable -- 可迭代对象。
  
  dict1 = {"a": 1, "b": 2}
  dict2 = {"c": 3}
  dict3 = dict(dict1, **dict2) # dict3 = {"a": 1, "b": 2, "c": 3}
  ```

+ 工厂方法：

  ```python
  items = [('name', 'earth'), ('port', 80)]
  dict1 = dict(items)
  dict2 = dict((['name', 'earth'], ['port', '80']))
  ```

+ `fromkeys()`方法

  ```python
  dict1 = {}.fromkeys(('x', 'y'), -1)  # {'x': -1, 'y': -1}
  dict2 = {}.fromkeys(('x', 'y'))   # {'x': None, 'y': None}
  ```

## 2.3. 运算符与流程控制

### 2.3.1. 运算符

![标识符](https://github.com/lajos182/python-essay/blob/master/images/operate.png)

运算符优先级：无需记录运算符的优先级，需要的时候添加()即可。

灵活的`or`：`a = False or 2`， 赋值前会判断前面的值，若为真则使用，若为假，则使用or后面的值

**海象表达式`:=`:**python3.8引入的新语法，将给变量赋值，这个变量可以是表达式的一部分。

```python
# 用在if中可以避免调用len()两次
if (n := len(a)) > 10:
    print(f'List is too long ({n} elements, expected <= 10)')

# 正则表达式匹配和获取结果的时候
discount = 0.00
if (mo := re.search(r'(\d+)% discount', advertisement)):
    discount = float(mo.group(1)) / 100.0

# 用在while循环语句中，可以同时取值，并判断是否为空
while (block := f.read(256) != ''):
    process(block)

```

### 2.3.2. 流程控制

![流程控制](https://github.com/lajos182/python-essay/blob/master/images/flow%20control.png)

列表生成式：

```python
print([i for i in range(1, 11)])
print([i*2 for i in range(1, 11)])
print([i*i for i in range(1, 11)])
print([str(i) for i in range(1, 11)])
print([i for i in range(1, 11) if i % 2 == 0])
```

+ **冒泡排序法**：每次比较相邻的两个元素，不合适就交换，依次向后，一圈下来可以确定一个元素；需要使用双重循环，外层循环控制循环的圈数， 内层控制一圈怎么交换

  ```python
  def bubble_sort(lt, key=None, reverse=False):
      for i in range(len(lt) - 1):
          for j in range(len(lt) - 1 - i):
              if key == None:
                  temp = lt[i] <= lt[i + 1] if reverse else lt[i] > lt[i + 1]
              else:
                  temp = key(lt[i]) <= lt[i + 1] if reverse else key(lt[i]) > key(lt[i + 1])
              if temp:
                  lt[i], lt[i + 1] = lt[i + 1], lt[i]
      print(lt)
      
      lt1 = [1, 5, 2, 1, 4, 9]
  lt2 = [
  	{'name': 'xiaoming', 'age': 12, 'height': 160},
      {'name': 'xiaohua', 'age': 17, 'height': 140},
      {'name': 'xiaogang', 'age': 11, 'height': 180}
  ]
  choose_sort(lt1)
  choose_sort(lt2, key=lamamb x: x['age'])
  ```

+ **选择排序法**：每一次从待排序的数据元素中选出最小（或最大）的一个元素，存放在序列的起始位置，直到全部待排序的数据元素排完。

  ```python
  def choose_sort(lt, key=None, reverse=False):
      for i in range(len(lt) - 1):
          for j in range(i + 1, len(lt)):
              if key == None:
                  temp = lt[i] <= lt[j] if reverse else lt[i] > lt [j]
              else:
                  temp = key(lt[i]) <= key(lt[j]) if reverse else key(lt[i]) > key(lt[j])
              if temp:
                  lt[i], lt[j] = lt[j], lt[i]
      print(lt)
     
  
  lt1 = [1, 5, 2, 1, 4, 9]
  lt2 = [
  	{'name': 'xiaoming', 'age': 12, 'height': 160},
      {'name': 'xiaohua', 'age': 17, 'height': 140},
      {'name': 'xiaogang', 'age': 11, 'height': 180}
  ]
  choose_sort(lt1)
  choose_sort(lt2, key=lamamb x: x['age'])
  ```

## 2.4. 函数使用

### 2.4.1. 函数的基本定义

**函数**：具有特定功能的一段代码。

函数的优点：

+ 解决代码的重复书写问题
+ 可以将功能的实现者和使用者分开，提高开发效率
+ 增加的代码的可移植性

**函数参数**：

- 形参：形式参数，函数定义处的参数
- 实参：实际参数，函数调用处的参数
- 必传参数：也叫位置参数，前面定义的函数中使用的都是必传参数，调用时的形式必须要与定义的一致。
- 默认参数：也称关键字参数，就是有默认值的参数，必须放在最后
- 可变长度参数：函数调用时传递必定义时的参数要多，多出来的参数会保存在`args`和`kwargs`中

`*args与**kwargs`的区别：

+ 用`*args`和`**kwargs`只是为了方便并没有强制使用它们。
+ `*args`接受多余的位置参数，转化程元组`tuple`形式，`**kwargs`接受N个关键字参数，转换成字典`dict`形式

*的特殊用法：

```python
 def show(a, b):
      print(a, b)

  l = [1, 2]
  # 略显啰嗦
  # show(l[0], l[1])
  # 精简方法
  show(*l)


  def show2(a='aa', b='bb'):
      print(a, b)

  d = {'a':'apple', 'b':'banana'}

  # show2(a=d['a'], b=d['b'])
  # 上面方式的简单书写方法
  show2(**d)
```

位置参数：调用参数时比较灵活，加不加关键字都可以，但python3.8引入新的语法控制这种灵活性，`'/'`之前的参数必须不加关键字，`'*'`之后的参数必须加关键字，其他参数依旧随意。

```python
# python3.8之前定义函数
def center(txt, border='=', width=50):
    return f'{txt}'.center(width, border)

# 调用结果：
>>>center('python')
'=========================python========================'
>>>center('python', '*', 10)
'**python**'
>>>center('python', border='*', width=10)
'**python**'
>>>center(txt='python', border='*', width=10)
'**python**'

# python3.8新特性：
def center(txt, /, border='=', *, width=50):
     return f'{txt}'.center(width, border)
# 调用结果
>>> center(txt = '中心',border='$',width = 10)
Traceback (most recent call last):
  File "<pyshell#68>", line 1, in <module>
    center(txt = '中心',border='$',width = 10)
TypeError: center() got some positional-only arguments passed as keyword arguments: 'txt'
>>>center( '中心','$', 10)
Traceback (most recent call last):
  File "<pyshell#69>", line 1, in <module>
    center( '中心','$', 10)
TypeError: center() takes from 1 to 2 positional arguments but 3 were given
>>> center('中心',border='$',width = 10)
'$$$$中心$$$$'
>>> center('中心','$',width = 10)
'$$$$中心$$$$'
```

### 2.4.2. 变量作用域（LEGB）

LEGB规则：local > enclosed > global > bulit-in

+ （1）**块级作用域**：Python不存在块级作用域，下民的代码可以正常运行。

  ```python
  if True:
      name = 'xiaoming'
  
  print(name)
  ```

+ （2）**局部作用域**：定义在函数内部的变量叫局部变量，只能在函数内部使用。

  ```python
  def test():
      a = 1
  
  test()
  # 此处会报错，提示变量未定义
  # print(a)
  ```

+ （3）**全局作用域**：定义在函数外部的变量叫全局变量，哪里都可以使用(但是不能修改，除非使用`global`)

  ```python
  a = 10
  def test():
      # 加上这句代码，就可以在函数内部修改全局变量
      global a
      a = 1
  
  test()
  print(a)
  ```

+ （4）**闭包函数外的函数中**：

  ```python
  def wai():
        age = 20
        def nei():
            # 使用外层函数的局部变量，加上nonlocal姐可以修改外部函数的局部变量
            nonlocal age
            age = 30
            print(age)
        nei()
        print(age)
  
    wai()
  ```

### 2.4.3. 内置函数、模块函数及基本数据结构函数

![内置函数、模块函数及基本数据结构函数](https://github.com/lajos182/python-essay/blob/master/images/builtin%2C%20module%2C%20str%2C%20list%2C%20tuple%2C%20set%2C%20dict.png)

### 2.4.4. 匿名函数

**匿名函数`lambda`**：就是没有名字的函数，使用`lambda`关键字定义。

特点：

- 以lambda开头
- 后面跟上该匿名函数的参数，多个参数使用逗号隔开
- 最后一个参数的后面跟上冒号':'
- 冒号的后面跟上一个表达式，这个表达式就是返回值，不需要使用`return`

### 2.4.5. 递归函数

**递归函数**： 函数内部调用函数本身的函数叫递归函数

特点：

- 代码简洁
- 可读性差(不易理解)
- 瞬间占用内存较大，没有终止条件会立即崩溃
- 有些领域禁止使用(安全领域：汽车电子)
- 只有在不得不使用的时候再使用(目录操作)

斐波那契数列(1,1,2,3,5,8,13,21,34,...)

```python
def fibonacci(n):
    if n == 1 or n == 2:
        return 1
    return fibonacci(n-2) + fibonacci(n-1)

print(fibonacci(6))
```

### 2.4.6. 闭包与装饰器

**闭包**：外部函数中定义一个内部函数，内部函数中使用了外部函数的变量，外部函数将内部函数作为返回值返回。提高了代码的可重复使用性.

```python
def wai(n):
    def nei():
        return n*n
    return nei

f1 = wai(3)
print(f1())
```

**装饰器**：本质就是一个函数，该函数接受一个函数作为参数，返回一个闭包，而且闭包中执行传递进来的函数，闭包中可以在函数执行的前后添加额外的功能。

**装饰器的作用就是为已经存在的对象添加额外的功能**。

```python
def zhuangshiqi(func):
    def wrapper(*args, **kwargs):
        return func(*args, **kwargs) + 10
    return wrapper

@zhuangshiqi
def pingfang(n):
    return n * n

print(pingfang(4))
```

### 2.4.7. 迭代器与生成器

+ **迭代器(Iterator)**：可以使用`for-in`进行遍历，并且可以使用next依次获取元素的对象。

  可以使用`isinstance`判断是否是迭代器。

  ```python
  from collections import Iterator
  
  l = (i for i in range(10))
  print(isinstance(l, Iterator))
  ```

+ **生成器(generator)**：为了解决内存突然变大的问题，Python引入了生成器。它是一种他叔的迭代器。

  + 产生条件：

    + 将列表生成式中的`[]`改为`()`

      ```python
      # 数据量特别大时，会造成内存占用突然增大
      # l2 = [i for i in range(10000)]
      # 生成器
      l2 = (i for i in range(2))
      # 使用next获取生成器中值，一次一个，遍历结束会报错StopIteration
      print(next(l2))
      ```

    + 通常在函数中使用`yield`关键字

      ```python
      def test(n):
      	for i in range(1, n+1):
            	yield i
      ```

  + 特性

    - 可以使用`next`获取数据，一次一个，结束时会报错
    - 只能遍历一遍
    - 可以转换为列表
    - 可以使用`for-in`遍历

### 2.4.8. 高级函数

+ **可迭代对象**：可以使用`for-in`遍历的对象，我们都称之为可迭代对象。字符串、列表、元组、集合、字典等都不是迭代器，他们都是可迭代对象。

可以使用`isinstance`判断是否是可迭代对象：

```python
from collections import Iterable
print(isinstance(l, Iterable))
print(isinstance(lt, Iterable))
```

+ **高级函数map**：格式`map(func, lt)`，接受两个参数，一个函数和一个可迭代对象，返回一个生成器，将`func`依次作用于`lt`

  ```python
  l = [1,2,3,4,5]
  m = map(lambda x:x*x, l) # 迭代器
  ```

+ **高级函数filter**：格式`filter(funct, lt)`，使用`func`依次作用于每个元素，处理结果为`True`保留下来。

  ```python
  l = [1,2,3,4,5]
  
  # 提取偶数
  f = filter(lambda x:x%2==0, l)
  
  print(list(f))
  ```

+ **高级函数reduce**：格式`reduce(func, lt)`, 接受两个参数，一个函数和一个可迭代对象，首先取两个元素，使用`func`处理，结果和第三个元素继续使用`func`处理，直到结束，返回处理的结果。

  ```python
  from functools import reduce
  
  l = [1,2,3,4,5]
  
  # 求和
  print(reduce(lambda x, y:x+y, l))
  
  # 转换为12345
  print(reduce(lambda x, y:x*10+y, l))
  ```

+ **高级函数sorted**：格式`sorted(func, lt)`, 内建函数，用于对可迭代快递的每个元素进行排序，生成新的对象。

  ```python
  l = [
      {'name':'xiaowang', 'age':18,'height':150},
      {'name':'xiaogang', 'age':20,'height':140},
      {'name':'xiaohong', 'age':19,'height':145},
  ]
  
  l2 = sorted(l, key=lambda x:x['age'], reverse=True)
  
  print(l2)
  ```

  注意：`sort`也可用来排序，它是`list`的排序方法，用于对列表的成员进行排序，而且改变的是原列表。

### 2.4.9. 匿名、递归、闭包、高级函数总结

![ 匿名、递归、闭包、高级函数总结](https://github.com/lajos182/python-essay/blob/master/images/recursive%2C%20lamada%2C%20closure%2C%20iteator%2C%20decorator%2C%20generator%2C%20iterable.png)

### 2.4.10. <a href='#IO编程'>目录管理与文件操作相关模块函数</a>

+ **目录管理(`os`)**

  ```python
  # system, 执行系统命令
  os.system('cls')
  
  # name, 获取操作系统名称，nt代表Windows, posix代表unix
  print(os.name)
  
  # environ, 获取环境变量
  os.environ.get('path')
  os.environ.get(['path'])
  os.getenv('path')
  
  # getcwd, 获取当前工作目录
  os.getcwd()
  
  # mkdir, 创建目录，该方法创建中间目录会报错
  os.mkdir('hello')
  
  # makedirs, 创建目录，会创建中间目录
  os.makedirs('a/b/c')
  
  # rmdir, 删除目录，只能删除空目录
  os.rmdir('a')
  
  # rename, 修改文件名(可以是目录)
  os.rename('a', 'c')
  
  # stat, 查看文件信息
  os.stat('123.py')
  
  # listdir, 列出直接子文件
  os.listdir('c')
  ```

  `path`函数

  ```python
  from os import path
  # 提取文件后缀（切割文件名与后缀）
  name, ext = path.splitext('789.py')
  print(name, ext)
  
  # 提取目录名（最后一个目录分隔符的前面内容）
  print(path.dirname('123/456/789.py'))
  
  # 提取文件名(包括后缀)
  print(path.basename('123/456/789.py'))
  
  # 切割文件名和目录
  print(path.split('123/456/789.py'))
  
  # 判断文件是否存在（可以是目录）
  print(path.exists('123.py'))
  
  # 判断是否是目录文件
  print(path.isdir('c'))
  
  # 判断是否是普通文件
  print(path.isfile('123.py'))
  
  # 获取普通文件大小
  print(path.getsize('01-os.py'))
  # 不可以获取目录大小，始终是0
  print(path.getsize('c'))
  ```

+ **文件管理**

  + 打开文件（`open`）：`fp = open('00-test.txt', 'r')`

    ```python
    # 参数1：文件路径名；参数2：打开方式；参数3：编码格式，一般不用指定，系统会自动识别处理
    # 打开方式：
    r：只读方式，文件不存在会报错
    w：只写方式，文件不存在创建文件，文件存在清空内容
    a：追加方式，文件不存在则创建，文件存在直接打开(不会清空内容)，只能向最后追加内容
    r+：在r方式下添加写的功能
    w+：在w方式下添加读的功能
    a+：在a方式下添加读的功能
    
    在上面的模式上添加b，表示二进制方式打开：rb、wb、ab、rb+、wb+、ab+
    1.文件的读写数据全部是bytes类型，没有添加b的方式全部是str类型
    
    # 编码方式
    ascii：美国信息交换标准代码
    ansi：扩展的ascii
    gb2312：中国的ansi
    gbk：扩展的gb2312
    
    unicode：是一套理论，实现方式不限
    utf-8：可变长度的unicode实现，对中文的支持比较友好
    ```

  + 关闭文件（`close`）：`fp.close()`

  + 文件读写

    ```python
    # 读取指定长度内容
    # ret = fp.read(3)
    # 写入内容
    fp.write('hello')
    
    # 读取一行，包括换行符
    print(fp.readline())
    
    # 读取所有行，返回一个列表
    print(fp.readlines())
    
    # 是否可读
    print(fp.readable())
    
    # 是否可写
    print(fp.writable())
    ```

  + **`read`、`readline`和`readlines`的区别，如何读取大文件**

    > **`read()方法`**：读取整个文件，将文件内容放到一个字符串变量中，如果需要对文件按行进行处理，则不可用该方法。如果文件大于可用内存(好几个G的)，不可能使用这种处理，系统会报错：`MemoryError`
    >
    > **`readline()方法`**： 读取下一行，每只读取文件的一行，通常也是读取到的一行内容放到一个字符串变量中，返回`str`类型。内存不够时使用，一般不太用。
    >
    > **`readlines()方法`**：**读取整个文件所有行，保存在一个列表(`list`)变量中，每行作为一个元素，但读取大文件会比较占内存。**
    >
    > **大文件读取数据**：处理大文件是很容易想到的就是将大文件分割成若干小文件处理，处理完每个小文件后释放该部分内存（分块读取）。这里用了**`iter` & `yield`**

    + 分块读取（`yield`）：将大文件分割成若干小文件处理，处理完每个小文件后释放该部分内存

      ```python
      # 分块读取
      def read_chunk(file_name, trunk_size):
          fp = open(file_name, 'rb') # 创建文件对象，也是一个可迭代对象
          # while True:
          #     content = fp.read(trunk_size)
          #     if not content:
          #         break
          #     yield content
          content = fp.read(trunk_size)
          while content:
              content = fp.read(trunk_size)
              yield content
            
      if __name__ == '__main__':
          file_name = r'F:\AngularJS学习资料\第一章  AngularJS教程.md'
          for i in read_chunk(file_name, 50):
              print(i)
      ```

    + 使用`with`（操作可迭代对象）：对可迭代对象 `fp`，进行迭代遍历：`for line in fp`，会自动地使用缓冲`IO`（`buffered IO`）以及内存管理，而不必担心任何大文件的问题。

      ```python
      with open(r'F:\AngularJS学习资料\第一章  AngularJS教程.md', 'rb') as fp:
          for line in fp:
              print(line)
      ```


  + 文件指针

    ```python
    # 返回文件指针的操作位置
    print(fp.tell())
    
    # 设置偏移
    # 参数1：偏移量
    # 参数2：参考位置，0：开头，1：当前，2：末尾
    # 定位到末尾
    fp.seek(0, 2)
    ```

    > 带`b`的方式`seek`没有异常；不带`b`的时候，相对于当前位置无法偏移，相对于末尾只能偏移0

  + 文件删除

    ```python
    import os
    os.remove('02-test.py')
    ```

+ **文件高级操作`shutil`**:

  + **`copyfileobj(fsrc, fdst, length=16*1024)`**：将`fsrc`文件内容复制至`fdst`文件，`length`为`fsrc`每次读取的长度，用做缓冲区大小

    ```python
    import shutil
    fp1 = open('file.txt', 'r')
    fp2 = open('file_copy.txt', 'a+')
    shutil.copyfileobj(fp1, fp2, length=1024)
    ```

  + **`copyfile(src, dst)`**：将`src`文件内容复制至`dst`文件，若`dst`文件不存在，将会生成一个`dst`文件；若存在将会被覆盖

    ```python
    import shutil
    shutil.copyfile("file.txt","file_copy.txt")
    ```

  + **`copymode(src, dst, follow_symlinks=True)`**：将`src`文件权限复制至`dst`文件，文件内容，所有者和组不受影响。`dst`路径必须是真实的路径，并且文件必须存在，否则将会报文件找不到错误。`follow_symlinks`为`Python3`新增参数，设置为`False`时，`src`, `dst`皆为软连接，可以复制软连接权限，如果设置为`True`，则当成普通文件复制权限。默认为`True`。

    ```python
    import shutil
    shutil.copymode("file.txt","file_copy.txt")
    ```

  + **`copystat(src, dst, follow_symlinks=True)`**：将权限，上次访问时间，上次修改时间以及`src`的标志复制到`dst`。文件内容，所有者和组不受影响。`follow_symlinks`设置为`False`时，`src`, `dst`皆为软连接，可以复制软连接权限、上次访问时间，上次修改时间以及`src`的标志，如果设置为`True`，则当成普通文件复制权限。默认为`True`。

    ```python
    import shutil
    shutil.copystat("file.txt","file_copy.txt")
    ```

  + **`copy(src, dst, follow_symlinks=True)`**： 将文件`src`复制至`dst`。`dst`可以是个目录，会在该目录下创建与`src`同名的文件，若该目录下存在同名文件，将会报错提示已经存在同名文件。权限会被一并复制。本质是先后调用了`copyfile`与`copymode`而已。`follow_symlinks`和上面作用相同。

    ```python
    improt shutil,os
    shutil.copy("file.txt","file_copy.txt")
    # 或者
    shutil.copy("file.txt",os.path.join(os.getcwd(),"copy"))
    ```

  + **`copy2(src, dst, follow_symlinks=True)`**：将文件`src`复制至`dst`。`dst`可以是个目录，会在该目录下创建与`src`同名的文件，若该目录下存在同名文件，将会报错提示已经存在同名文件。权限、上次访问时间、上次修改时间和`src`的标志会一并复制至`dst`。本质是先后调用了`copyfile`与`copystat`方法而已。`follow_symlinks`和上面作用相同。

    ```python
    improt shutil,os
    shutil.copy2("file.txt","file_copy.txt")
    # 或者
    shutil.copy2("file.txt",os.path.join(os.getcwd(),"copy"))
    ```

  + **`ignore_patterns(*patterns)`**：忽略模式，用于配合`copytree()`方法，传递文件将会被忽略，不会被拷贝。`patterns`是文件名称、元组。

  + **`copytree(src, dst, symlinks=False, ignore=None, `copy_function=copy2,
                 ignore_dangling_symlinks=False`)`**：拷贝文档树，将`src`文件夹里的所有内容拷贝至`dst`文件夹，文件夹不存在会自动创建。`symlinks`代表是否复制软连接，`True`复制软连接，`False`不复制，软连接会被当成文件复制过来，默认`False`。`ignore`为忽略模式，可传入`ignore_patterns()`。`copy_function`为拷贝文件的方式，可传入一个可执行的处理函数，默认为`copy2`，`ignore_dangling_symlinks`设置为`False`，拷贝指向文件已删除的软连接时，将会报错，如果想消除这个异常，可以设置此值为True，默认为`False`。

    ```python
    import shutil,os
    folder1 = os.path.join(os.getcwd(),"aaa")
    # bbb与ccc文件夹都可以不存在,会自动创建
    folder2 = os.path.join(os.getcwd(),"bbb","ccc")
    # 将"abc.txt","bcd.txt"忽略，不复制
    shutil.copytree(folder1,folder2,ignore=shutil.ignore_patterns("abc.txt","bcd.txt")
    ```

  + **`rmtree(path, ignore_errors=False, onerror=None)`**：移除文档树，将文件夹目录删除。`ignore_errors`代表是否忽略错误，默认`False`，`onerror`定义错误处理函数，需传递一个可执行的处理函数，该处理函数接收三个参数：函数、路径和`excinfo`

    ```python
    import shutil,os
    folder1 = os.path.join(os.getcwd(),"aaa")
    shutil.rmtree(folder1)
    ```

  + **`move(src, dst, copy_function=copy2)`**：将`src`移动至`dst`目录下。若`dst`目录不存在，则效果等同于`src`改名为`dst`。若`dst`目录存在，将会把`src`文件夹的所有内容移动至该目录下面。`copy_function`为拷贝文件的方式，可传入一个可执行的处理函数，默认为`copy2`。

    ```python
    import shutil,os
    # 示例一，将src文件夹移动至dst文件夹下面，如果bbb文件夹不存在，则变成了重命名操作
    folder1 = os.path.join(os.getcwd(),"aaa")
    folder2 = os.path.join(os.getcwd(),"bbb")
    shutil.move(folder1, folder2)
    # 示例二，将src文件移动至dst文件夹下面，如果bbb文件夹不存在，则变成了重命名操作
    file1 = os.path.join(os.getcwd(),"aaa.txt")
    folder2 = os.path.join(os.getcwd(),"bbb")
    shutil.move(file1, folder2)
    # 示例三，将src文件重命名为dst文件(dst文件存在，将会覆盖)
    file1 = os.path.join(os.getcwd(),"aaa.txt")
    file2 = os.path.join(os.getcwd(),"bbb.txt")
    shutil.move(file1, file2)
    ```

  + **`disk_usage(path)`**：获取当前目录所在硬盘使用情况。`path`表示文件夹或文件路径，`windows`中必须是文件夹路径，`linux`中可以是文件路径和文件夹路径。

    ```python
    import shutil.os
    path = os.path.join(os.getcwd(),"aaa")
    info = shutil.disk_usage(path)
    print(info)   # usage(total=95089164288, used=7953104896, free=87136059392)
    ```

  + **`chown(path, user=None, group=None)`**：修改路径指向的文件或文件夹的所有者或分组。

    ```python
    import shutil,os
    path = os.path.join(os.getcwd(),"file.txt")
    shutil.chown(path, user="root", group="root")
    ```

  + **`which(cmd, mode=os.F_OK | os.X_OK, path=None)`**： 获取给定的`cmd`命令的可执行文件的路径。

    ```python
    import shutil
    print(shutil.which('pip'))  # D:\Python\Python36\Scripts\pip.EXE
    ```

  + **`make_archive(base_name, format, root_dir, …)`**：生成压缩文件。`base_name`指压缩文件的文件名，不允许有扩展名(因为会根据压缩格式生成相应的扩展名)，`format`表示压缩格式，`root_dir`表示将指定文件夹进行压缩。

    ```python
    import shutil,os
    base_name = os.path.join(os.getcwd(),"aaa")
    format = "zip"
    root_dir = os.path.join(os.getcwd(),"aaa")
    # 将会root_dir文件夹下的内容进行压缩，生成一个aaa.zip文件
    shutil.make_archive(base_name, format, root_dir)
    ```

  + **`get_archive_formats()`**：获取支持的压缩文件格式。目前支持的有：`tar`、`zip`、`gztar`、`bztar`。在Python3还多支持一种格式`xztar`。

  + **`unpack_archive(filename, extract_dir=None, format=None)`**：解压操作，`extract_dir`解压至的文件夹路径，文件夹可以不存在，会自动生成。`format`解压格式，默认为`None`，会根据扩展名自动选择解压格式。

    ```python
    import shutil,os
    zip_path = os.path.join(os.getcwd(),"aaa.zip")
    extract_dir = os.path.join(os.getcwd(),"aaa")
    shutil.unpack_archive(zip_path, extract_dir)
    ```

  + **`get_unpack_formats()`**：获取支持的解压文件格式。目前支持的有：`tar`、`zip`、`gztar`、`bztar`和`xztar`。

![目录及文件管理](https://github.com/lajos182/python-essay/blob/master/images/os%20and%20shutil.png)

+ **经典练习**

  + 实现一个拷贝文件的功能，提醒：要考虑超大文件问题，如:依次读取1024字节，循环读取

    ```python
    import os
    def copy_file(source, target):
        if not os.path.exists(source):
            print('源文件不存在！')
            return
        if os.path.isdir(source):
            print('源文件是目录文件，无法拷贝！')
            return
        if os.path.abspath(source) == os.path.abspath(target):
            print('复制的地址与源文件相同，无法进行复制！')
            return 
        if os.path.isdir(target):
            target = os.path.join(target, os.path.basename(source))
        source_fp = open(source, 'rb')
        target_fp = open(target, 'wb')
        content = source_fp.read(1024)
        while content:
            target_fp.write(content)
            content = source_fp.read(1024)
        source_fp.close()
        target_fp.close()
    ```

  + 递归拷贝一个文件夹

    ```python
    def copy_dir(source, target):
        if not os.path.exists(source):
            print('原文件不存在！')
            return
        if os.path.isfile(target):
            print('源文件不是目录文件！')
        if os.path.isfile(target):
            print('目标地址不是目录，无法进行拷贝')
            return
        if os.path.abspath(source) == os.path.abspath(target):
            print('复制的地址与源文件相同，无法进行复制')
            return
        if not os.path.exists(target):
            os.makedirs(target)
        source_list = os.listdir(source)
        for item in source_list:
            source_name = os.path.join(source, item)
            target_name = os.path.join(target, item)
            if os.path.isfile(source_name):
                copy_file(source_name, target_name) # 拷贝单个文件
            else:
                copy_dir(source_name, target_name) # 递归拷贝
     copy_dir('a', 'b')         
    ```

  + 递归删除一个文件夹(或文件)

    ```python
    import os
    def delete_dir(source):
        if not os.path.exists(source):
            print('要删除的文件不存在！')
            return
        if os.path.isfile(source):
            os.remove(source)
        source_list = os.listdir(source)
        for item in source_list:
            source_path = os.path.join(source, item)
            if os.path.isfile(source_path):
                os.remove(source_path)
            else:
                delete_dir(source_path)
        os.rmdir(source)
    delete_dir('../ccc')
    ```

  + 递归统计一个文件夹的大小

    ```python
    import os
    def get_size(source):
        size = 0
        if not os.path.exists(source):
            print('当前文件(夹)不存在！')
            return
        if os.path.isfile(source):
            size += os.path.getsize(source)
            return size
        source_list = os.listdir(source)
        for item in source_list:
            source_path = os.path.join(source, os.path.basename(item))
            if os.path.isfile(source_path):
                size += os.path.getsize(source_path)
            else:
                size += get_size(source_path)
        return size
    
    print(get_size('a_a.py'))
    ```

  + 移动文件夹

    ```python
    def move_dir(source, target):
        if not os.path.exists(source):
            print('不存在该文件，无法移动')
            return
        if os.path.abspath(source) == os.path.abspath(target):
            print('源文件地址与指定的地址相同，无法进行移动')
            return
        if os.path.isfile(source):
            source_fp = open(source, 'r')
            target_fp = open(target, 'w')
            content = source_fp.read(1024)
            while content:
                target_fp.write(content)
                content = source_fp.read(1024)
            source_fp.close()
            target_fp.close()
            os.remove(source)
        else:
            if not os.path.exists(target):
                os.makedirs(target)
            source_list = os.listdir(source)
            for item in source_list:
                source_item = os.path.join(source, item)
                target_item = os.path.join(target, item)
                move_dir(source_item, target_item)
            os.rmdir(source)
    
    move_dir('a', 'c')
    ```

  + 目录整理

    ```python
    # 将目录按后缀进行分类，后缀相同的放到后缀字母大写的文件中，没有后缀的放置在'OTHERS'中，文件夹放在'DIRS'中
    import os, shutil
    def clean_dir(source):
        if os.path.isfile(source) or not os.path.exists(source):
            print('当前目录无法整理，请查询你要整理的目录！') 
            return
        source_list = os.listdir(source)
        for item in source_list:
            source_path = os.path.join(source, item)
            if os.path.isfile(source_path):
                suffix = source_path.rsplit('.', 1)
                if len(suffix) == 2:
                    SUFFIX = os.path.join(source, suffix[1].upper())
                    if not SUFFIX:
                        os.mkdir(SUFFIX)
                    shutil.move(source_path, SUFFIX)
                else:
                    OTHERS = os.path.join(source, 'OTHERS')
                    if not OTHERS:
                        os.mkdir(OTHERS)
                    shutil.move(source_path, OTHERS)
            else:
                DIRS = os.path.join(source, 'DIR')
                if not DIRS:
                    os.mkdir(DIRS)
                shutil.move(source_path, DIRS)
    ```

### 2.4.11. 时间、日期和日历相关模块函数

+ **`time`模块**：

  + `sleep`：休眠指定的秒数(可以是小数)

  + `localtime`： 将一个时间戳转换为`time.struct_time`类型的对象(类似于元组)

    ```python
    import time
    print(time.localtime())
    >>> time.struct_time(tm_year=2019, tm_mon=4, tm_mday=28, tm_hour=9, tm_min=25, tm_sec=34, tm_wday=6, tm_yday=118, tm_isdst=0)
    ```

    > 年、月、日、时、分、秒、星期(0~6)、今年的第几天、夏令时

  + `mktime`：根据元组形式的时间生成一���时间戳

    ```python
    import time
    print(time.mktime((2019, 4, 28, 9, 25, 34, 6, 118, 0))) # 注意一定是一个元组
    >>> 1556414734.0
    ```

  + `strftime`：将一个元组形式的时间格式化为字符串，不传时间默认转换当前时间

    ```python
    time.strftime('%Y-%m-%d %H:%M:%S %w %W', local_time)
    >>> '2019-04-28 09:34:53 0 16'
    # 注意与datetime.datetime.strftime的区别，datetime.datetime.strftime(time, '%Y-%m-%d %H:%M:%S:%f')
    ```

  + `gmtime`：将一个时间戳转换为元组形式，不传默认转换当前时间

    ```python
    print(time.gmtime())
    # time.struct_time(tm_year=2019, tm_mon=4, tm_mday=28, tm_hour=1, tm_min=50, tm_sec=27, tm_wday=6, tm_yday=118, tm_isdst=0)
    ```

  + `asctime`：将一个元组形式的时间转换为标准格式字符串，不传参数转换当前时间

    ```python
    print(time.asctime())
    # 'Sun Apr 28 09:49:13 2019'
    ```

  + `timezone`：0时区减去当前时区的秒数

    ```python
    print(time.timezone)  #  -28800
    ```

+ **`datetime`模块**：

  + `date()`：获取一定格式的时间，`print(date(2019, 5. 3)), # 2019-05-03`

    + `d = date.today()`：获取今天的时间
    + `d.fromtimestamp()`：将时间戳转化为日期， `print(d.fromtimestamp(time.time()))`

    + `d.isoformat()`：标准格式字符
    + `d.isocalendar()`：日历显示形式，如(年，第几周， 星期几)
    + `d.isoweekday()`：获取星期(1~7)
    + `d.weekday()`: 获取星期(0~6)
    + `d.strftime()`：格式化，`print(d.strftime('%y-%m-%d'))`
    + `d.timetuple()`：转化为元组

  + `time()`：获取一定格式的时间，`tm = time()`
    + `tm.hour`：获取小时
    + `tm.minute`：获取分钟
    + `tm.second`：获取秒数
    + `tm.strftime()`：时间格式化，`print(tm.strftime('%H:%M:%S'))`

  + `datetime`：
    + `datetime.now()`：获取本地时间
    + `datetime.utcnow()`：获取UTC时间(格林尼治时间)
    + `datetime.fromtimestamp()`：将一个时间戳转化为`datetime`
    + `datetime.fromtimestamp.strftime('%Y-%m-%d %H:%M:%S')`：格式化显示

  + `timedelta()`:
    + `delta = timedelta()`：获取时间差，`print(timedelta(days=2, hours=2, seconds=56))`
    + `delta.days`：获取天数
    + `delta.seconds`：获取天数外的秒数
    + `delta.total_seconds()`：获取总秒数

+ **`calendar`模块**：

  + `calendar`：获取某一年的日历

    ```python
    # 获取某一年的日历, 参数：年份， w =列宽， l= 行宽，m = 控制每行打印月份数， c=每个月份之间的间距
    c = calendar.calendar(2018, w=3, l=2, m=2, c=10)
    ```

  + `month`：获取指定年指定月份的日历：

    ```python
    # 获取指定年指定月的日历
    m = calendar.month(2018, 3)
    ```

  + `isleap`：判断是否是闰年

    ```python
    print(calendar.isleap(2062))
    ```

  + `leapdays`：判断两个年份之间的瑞年的个数([起始，结束))

    ```python
    print(calendar.leapdays(1992, 2018))
    ```


![时间、日期、日历](https://github.com/lajos182/python-essay/blob/master/images/time%2C%20calendar%20and%20datemate.png)

### 2.4.12. 短信邮件相关模块函数

+ **`hashlib`**：用来进行`hash`或者`md5`加密，而且这种加密是不可逆的，所以这种算法又被称为摘要算法。其支持`Openssl`库提供的所有算法，包括`md5`、`sha1`、`sha224`、`sha256`、`sha512`等。

  + `md5()`：创建一个`md5`加密模式的`hash`对象，可以指定需要加密的字符串

  + `update()`：设置加密字符串，创建`md5`对象就不必指定了，不能两个地方都指定

  + `hexdigest()`：获取加密后的摘要(32位)

    ```python
    import hashlib
    md = hashlib.md5() 
    md.update('123456'.encode('utf-8'))
    print(md.hexdigest()) # e10adc3949ba59abbe56e057f20f883e
    
    md = hashlib.md5('123456'.encode('utf-8')) # 如果添加参数，就相当于多进一层加密
    md.update('123456'.encode('utf-8'))
    print(md.hexdigest()) # ea48576f30be1669971699c09ad05c94
    
    ```

+ **`urlib`**：提供了一系列用于操作`URL`的功能，是`Python`的标准库

  + `request`：发送`http`请求

    + `urlopen()`：访问目标网址，结果是一个`http.client.HTTPResponse`对象，默认访问方法是`GET`，当在该方法中传入`data`参数时，则会发起`POST`请求。

      ```markdown
      urlopen(url, data=None, [timeout, ]*, cafile=None, capath=None, cadefault=False, context=None)
      ```

      ```python
      from urllib import request
      rep = request.urlopen('http://www.baidu.com')
      print(rep.read().decode('utf-8'))
      
      # urlopen返回对象提供方法：
      　　# read() , readline() ,readlines() , fileno() , close() ：对HTTPResponse类型数据进行操作。
      　　# info()：返回HTTPMessage对象，表示远程服务器返回的头信息。
      　　# getcode()：返回Http状态码。
      　　geturl()：返回请求的url。
      ```

      ```python
      from urllib import request
      # 设置timeout，如果请求时间超出，那么就会抛出异常
      resp = request.urlopen('http://httpbin.org', data='word=hello'.encode('utf-8'), timeout=10)
      print(resp.read().decode('utf-8'))
      ```

    + `Reuqest()`：传入的`request`对象，而不是一个`url`

      ```markdown
      urllib.request.Request(url, data=None, headers={}, origin_req_host=None, unverifiable=False, method=None)
      
      url--访问的地址。
      data--此参数为可选字段，其中传递的参数需要转为bytes，如果是字典我们只需要通过urlencode转换即可。
      headers--http相应headers传递的信息，构造方法：headers参数传递，通过调用Request对象的add_header()方法来添加请求头。
      origin_req_host--指的是请求方的host名称或者IP地址。
      unverifiable--用来表明这个请求是否是无法验证的，默认是False。意思就是说用户没有足够权限来选择接收这个请求的结果。如果没有权限，这时unverifiable的值就是True 。
      method--用来指示请求使用的方法，比如GET，POST，PUT等
      ```

      ```python
      # 使用urllib模拟微博登录
      from urllib import request
      from urllib.parse import urlencode
      print('Login to weibo.cn...')
      email = input('Email: ')
      passwd = input('Password: ')
      login_data = urlencode([
          ('username', email),
          ('password', passwd),
          ('entry', 'mweibo'),
          ('client_id', ''),
          ('savestate', '1'),
          ('ec', ''),
          ('pagerefer', 'https://passport.weibo.cn/signin/welcome?entry=mweibo&r=http%3A%2F%2Fm.weibo.cn%2F')
      ])
      req = request.Request('https://passport.weibo.cn/sso/login')
      req.add_header('Origin', 'https://passport.weibo.cn')
      req.add_header('User-Agent', 'Mozilla/6.0 (iPhone; CPU iPhone OS 8_0 like Mac OS X) AppleWebKit/536.26 (KHTML, like Gecko) Version/8.0 Mobile/10A5376e Safari/8536.25')
      req.add_header('Referer', 'https://passport.weibo.cn/signin/login?entry=mweibo&res=wel&wm=3349&r=http%3A%2F%2Fm.weibo.cn%2F')
      rep = request.urlopen(req, data=login_data.encode('utf-8'))
      print(rep.read().decode('utf-8'))
      ```

    + 添加`Cookie`：使用`request.build_opener`方法来进行构造`opener`

      ```python
      from http import cookiejar
      from urllib import request
      
      url = 'http://httpbin.org/cookies'
      # 创建一个cookiejar对象
      cookie = cookiejar.CookieJar()
      # 使用HTTPCookieProcessor创建cookie处理器
      cookies = request.HTTPCookieProcessor(cookie)
      # 并以它为参数创建Opener对象
      opener = request.build_opener(cookies)
      # 使用这个opener来发起请求
      resp = opener.open(url)
      print(resp.read().decode())
      ```

      或者也可以把这个生成的`opener`使用`install_opener`方法来设置为全局的。则之后使用`urlopen`方法发起请求时，都会带上这个`cookie`。

      ```python
      # 将这个opener设置为全局的opener
      request.install_opener(opener)
      resp = request.urlopen(url)
      ```

    + 设置`Proxy`代理：使用爬虫来爬取数据的时候，常常需要使用代理来隐藏我们的真实`IP`。

      ```python
      from urllib import request
      
      url = 'http://httpbin.org/ip'
      proxy = {'http':'50.233.137.33:80','https':'50.233.137.33:80'}
      # 创建代理处理器
      proxies = requet.ProxyHandler(proxy)
      # 创建opener对象
      opener = request.build_opener(proxies)
      resp = opener.open(url)
      print(resp.read().decode())
      ```

  + `error`：处理请求过程中出现的异常

    用 try-except来捕捉异常,主要的错误方式就两种` URLError`（错误信息）和`HTTPError`(错误编码)。

    ```python
    from urllib import request, error
    try:
        data= request.urlopen(url)
        print(data.read().decode('utf-8'))
    except error.HTTPError as e:  # 错误编码
        print(e.code)
    except error.URLError as e:   # 错误信息
        print(e.reason)
    ```

  + `parse`：解析`url`

    + `urlencode()`将字典转化为`key1=value1&key2=value2`格式

      ```python
      from urllib.parse import urlencode
      data = {
          'name': 'lajos',
          'age': 18
      }
      print(urlencode(data))  # name=lajos&age=18
      ```

    + `urlparse()`：解析`url`中的所有参数，得到的是`urllib.parse.ParseResult`对象

    + `parse_qs()`：将`url`请求参数转化为字典

      ```python
      from urllib.parse import parse_qs, urlparse
      url = 'http://www.baidu.com/abc/def?name=lajos&age=18'
      url_parse = urlparse(url)
      print(url_parse) # ParseResult(scheme='http', netloc='www.baidu.com', path='/abc/def', params='', query='name=lajos&age=18', fragment='')
      print(url_parse.query) # name=lajos&age=18
      print(parse_qs(url_parse.query)) # {'name': ['lajos'], 'age': ['18']}
      ```

  + `robotparser`：解析`robots.txt`文件

+ **`http.client`**：网络请求

  ```python
  import http.client
  
  # 创建连接(相当于浏览器)
  connect = http.client.HTTPConnection('www.baidu.com')
  # 发送请求(GET/POST)
  connect.request(method='GET', url='http://www.baidu.com')
  # 获取响应
  resp = connect.getresponse()
  # 打印响应内容，读取并解码
  print(resp.read().decode('utf-8'))
  ```

+ **`邮件发送smtplib`**：提供了一种很方便的途径发送电子邮件。它对smtp协议进行了简单的封装。

  + `SMTP()`:（`Simple Mail Transfer Protocol`)即简单邮件传输协议,它是一组用于由源地址到目的地址传送邮件的规则，由它来控制信件的中转方式。

    ```python
    import smtplib
    smtp_obj = smtplib.SMTP([host, [, port [, local_hostname]]])
    # host: SMTP 服务器主机。 你可以指定主机的ip地址或者域名如: runoob.com，这个是可选参数。
    # port: 如果你提供了host参数, 你需要指定SMTP服务使用的端口号，一般情况下SMTP端口号为25。
    # local_hostname: 如果 SMTP 在你的本机上，你只需要指定服务器地址为 localhost 即可。
    ```

  + `SMTP.sendmail()`：发送邮件

    ```python
    SMTP.sendmail(from_addr, to_addrs, msg[, mail_options, rcpt_options])
    # from_addr: 邮件发送者地址。
    # to_addrs: 字符串列表，邮件发送地址。
    # msg: 发送消息，格式是字符串，一般包含标题，发信人，收件人，邮件内容，附件等
    ```

  ```python
  import smtplib
  from email.mime.text import MIMEText
  from email.header import Header
  from email.mime.multipart import MIMEMultipart
  import os
  
  # 邮箱服务器
  mail_server  = 'smtp.qq.com'
  # 用户名
  mail_user = '13249732498@qq.com'
  # 密码或授权码，为了不公开可以通过环境变量的方式获取
  mail_password = os.environ.get('MAIL_PASSWORD') or '123456'
  # 邮件消息
  def send_mail(to_addrs):
      try:
          message = '你好，欢迎注册xxx平台，激活请点击右边链接 <a href="http://www.baidu.com">点击激活</a>'
          # 将邮件字符串消息转换邮件格式，若内容是HTML需要指定第二个参数为'html'
          message = MIMEText(message, 'html')
          # 设置主题
          message['Subject'] = Header('账户激活')
          # 设置显示的发件人
          message['From'] = Header(mail_user)
          # 设置显示的收件人，可以给多个人发邮件
          message['To'] = Header(to_addrs)
          # 创建邮件对象
          mail = smtplib.SMTP(mail_server, 25)
          # 登录服务器
          mail.login(mail_user, mail_password)
          # 发送邮件
          mail.sendmail(mail_user, to_addrs, message.as_string())
          mail.quit()
      except Exception:
          ret = False
      return ret
  
  ret = send_mail('1823423231@qq.com, 23423412@163.com')
  if ret:
      print('邮件发送成功！')
  else:
      print('邮件发送失败！')
  ```

  ```python
  import smtplib
  from email.mime.text import MIMEText
  from email.header import Header
  from email.mime.multipart import MIMEMultipart
  import os
  
  # 邮箱服务器
  mail_server  = 'smtp.qq.com'
  # 用户名
  mail_user = '1287174078@qq.com'
  # 密码或授权码，为了不公开可以通过环境变量的方式获取
  mail_password = os.environ.get('MAIL_PASSWORD') or 'qwewqrewr'
  # 邮件消息
  def send_mail(to_addrs):
      try:
          message = MIMEMultipart()
          # 设置主题
          message['Subject'] = Header('账户激活')
          # 设置显示的发送人
          message['From'] = Header(mail_user)
          # 设置显示的收件人，可以给多个人发邮件
          message['To'] = Header(to_addrs)
          body = '这是Python邮件发送测试.....'
          # 邮件正文内容
          message.attach(MIMEText(body, 'plain'))
          # 构造附件1，传送当前目录下的 test.txt 文件
          att1 = MIMEText(open('test1.txt', 'rb').read(), 'base64', 'utf-8')
          att1['Content-Type'] = 'application/octet-stream'
          att1["Content-Disposition"] = 'attachment; filename="test.txt"'
          message.attach(att1)
          # 构造附件2，传送当前目录下的 runoob.txt 文件
          att2 = MIMEText(open('yunda.py', 'rb').read(), 'base64', 'utf-8')
          att2["Content-Type"] = 'application/octet-stream'
          att2["Content-Disposition"] = 'attachment; filename="yunda.py"'
          message.attach(att2)
          # 创建邮件对象
          mail = smtplib.SMTP(mail_server, 25)
          # 登录服务器
          mail.login(mail_user, mail_password)
          
          # 发送邮件
          mail.sendmail(mail_user, to_addrs, message.as_string())
          mail.quit()
      except Exception:
          ret = False
      return ret
  
  ret = send_mail('1825871201@qq.com')
  if ret:
      print('邮件发送成功！')
  else:
      print('邮件发送失败！')
  ```

+ **短信发送**：常使用短信发送平台，如阿里、云之讯、秒滴

  + 该案例使用阿里短信平台对接，需要的参数如下：

    > **安装Python环境的依赖包**：`pip install aliyun-python-sdk-core`，使用于**`python2.6.5`**及其更高版本
    >
    > `accessKeyId`：主账号`AccessKey`的ID
    > `accessSecret`：主账号的密钥
    > `SignName`：短信签名名称
    > `PhoneNumbers`：要发送的电话号码
    > `TemplateCode`：短信模板ID，例如`'SMS_153055065'`
    > `TemplateParam`：短信模板变量对应的实际值，`JSON`格式，如`'{"code": "1234"}'`

    ```python
    # 将对应的参数替换即可进行调用阿里云短信服务平台
    from aliyunsdkcore.client import AcsClient
    from aliyunsdkcore.request import CommonRequest
    client = AcsClient('<accessKeyId>', '<accessSecret>', 'default')
    
    request = CommonRequest()
    request.set_accept_format('json')
    request.set_domain('dysmsapi.aliyuncs.com')
    request.set_method('POST')
    request.set_protocol_type('https') # https | http
    request.set_version('2017-05-25')
    request.set_action_name('SendSms')
    
    request.add_query_param('SignName', 'lajos')
    request.add_query_param('PhoneNumbers', '15299013421')
    request.add_query_param('TemplateCode', 'SMS_135695051')
    request.add_query_param('TemplateParam', '{"code": "1123"}')
    
    response = client.do_action(request)
    print(str(response, encoding='utf-8'))
    ```

![短信邮件相关](https://github.com/lajos182/python-essay/blob/master/images/hashlip%2C%20urllib%2C%20http.client.png)

## 2.5. 模块使用

**模块**：模块就像一个工具包一样，里面有很多工具(函数、类)，使用时需要通过`import`导入。

分类：①标准库：`random`、`sys`、`os`、`time`；②第三方：已经写好的特定功能的模块，你可以直接使用pip命令安装；③自定义：自己写的

```python
import random					# 导入
import random as rdm			# 导入并起别名
from time import sleep			# 指定导入
from time import sleep as sp	# 指定导入并起别名
from random import *            # 模糊导入
```

**自定义模块**：新建一个文件，不与其他模块同名，该文件名就是模块，导入方式于官方的相同。文件名(模块名)就是命名空间，不同命名空间下的标识符可以同名，当使用几个模块中相同的（函数）标识符时，可以通过命名空间或起别名解决。

**测试模块**：当一个模块作为主模块运行时，`__ name __ `的值为` '__ main __'`，当被其他模块导入使用时，值为模块名。

```python
if __name__ == '__main__':
    print('测试代码')
```

**包**：多个模块放在同一目录下，目录下有一个`__ init __.py`文件，这个目录就是一个包。一个目录要想成为一个包，必须包含一个` __ init __.py`文件，即使该文件为空(可以简化导入书写)

**修改pip源**：在用户的家目录创建`pip`目录，并创建`pip.ini`，添加如下内容：

```ini
[global]
index-url = http://mirrors.aliyun.com/pypi/simple/
trusted-host = mirrors.aliyun.com
```

**pip命令**：安装软件包，自动会安装相关的依赖

```tx
安装软件包：pip install 包名
卸载软件包：pip uninstall 包名
列表显示包：pip list
查看指定包：pip show 包
检测哪些包需要更新：pip list --outdated
升级包：pip install --upgrade 包名
输出已安装的包列表：pip freeze > requirements.txt
pip帮助：pip help
```

## 2.6. 异常处理



## 2.7. 面向对象(继承性、多态性、封装性)

### 2.7.1. 类和对象的基本定义

+ **类**：具有相同特征（属性和行为）事物的抽象。其实是一种自定义的数据类型。

+ **对象**：某个类的具象。其实是某个类型的变量。

  > 定义类需要使用关键字：**class**，也可以使用元类进行定义
  >
  > 类名：原则上只要符合标识符的命名规范即可，但是我们通常使用大驼峰风格(每个单词首字母大写)命名
  >
  > 不要忘记类名后面的冒号`:`
  >
  > 类的内容要进行缩进
  >
  > 行为(方法)：通过函数体现，与外面定义函数的方式相似，第一个参数默认是self
  >
  > **属性**：通过变量体现，属性是动态添加的，因此在定义时可以不体现
  >
  > 成员访问：成员属性(对象.属性名)，成员方法(对象.方法名())

  ![类的属性与方法](https://github.com/lajos182/python-essay/blob/master/images/class.png)

+ 示例：小明手里有两张牌，左手♥K，右手♠A，问：小明交换两手的牌后，手里分别是什么？

  + 思路：

    > 先找到对象：小明、左手、♥K、♠A、右手
    >
    > 根据对象抽象出来对应的类：人、牌、手
    >
    > 写出对应的逻辑，反过来完善抽象出来的类
    >
    > 按照题目的要求创建对应的对象，调用相关的方法

  + 代码：

    ```python
    class Poker(object):
    
        def __init__(self, color, number):
            self.color = color
            self.number = number
        
        def __str__(self):
            return f'{self.color}{self.number}'
    
    # 创建两张牌
    p1 = Poker('♥', 'K')
    p2 = Poker('♠', 'A')
           
    class Hand(object):
    
        def __init__(self, poker=None):
            self.poker = poker
    
        def hold_poker(self, poker):
            self.poker = poker
    
    # 创建左右手对象
    left_hand = Hand(p1)
    right_hand = Hand(p2)
    
    class Person(object):
    
        def __init__(self, name, left_hand, right_hand):
            self.name = name
            self.left_hand = left_hand
            self.right_hand = right_hand
    
        def show(self):
            print(f'{self.name}张开手', end=':')
            print(f'左手--{self.left_hand.poker}', end=',')
            print(f'右手--{self.right_hand.poker}')
    
        def swap(self):
            self.left_hand.poker, self.right_hand.poker = self.right_hand.poker, self.left_hand.poker
            print(f'{self.name}交换两手的牌')
    
    # 创建小明对象
    xiaoming = Person('小明', left_hand, right_hand)
    # 展示手里的牌
    xiaoming.show()
    # 交换两手牌
    xiaoming.swap()
    # 再次展示手里的牌
    xiaoming.show()
    ```

+ **`self`和`cls`区别**：

  + `python`并未对类中方法的第一个参数名字做限制，只不过是开发人员的习惯性用法。

  + `self`一般指类的实例，表示一个具体的实例本身，如果使用`@staticmethod`，就可以无视这个`self`，而将这个方法当成一个普通的函数使用。

  + `cls`表示这个类的本身

### 2.7.2. 常见的魔法函数

**魔法函数**：在python中，有一些内置好的特定的方法，这些方法在进行特定的操作时会自动被调用，称之为魔法方法。

+ **`__init__()`**：**初始化函数**，在创建实例对象为其赋值时使用，在`__new__`之后，`__init__`必须至少有一个参数`self`，这个就是`__new__`返回的实例，`__init__`是在`__new__`的基础上可以完成一些其它初始化的动作，`__init__`不需要返回值。这种方法常被人称为**构造方法**。

+ **`__new__()`**：很多人认为`__init__`是类的构造函数，其实不太确切，`__init__`更多的是负责初始化操作，相当于一个项目中的配置文件，`__new__`才是真正的构造函数，创建并返回一个实例对象，如果`__new__`只调用了一次，就会得到一个对象。**继承自`object`的新式类才有`__new__`这一魔法方法**，`__new__`至少必须要有一个参数`cls`，代表要实例化的类，此参数在实例化时由`Python`解释器自动提供，**`__new__`必须要有返回值，返回实例化出来的实例（很重要）**，这点在自己实现`__new__`时要特别注意，可以`return`父类__new__出来的实例，或者直接是`object`的`__new__`出来的实例，若`__new__`没有正确返回**当前类`cls`**的实例，那`__init__`是不会被调用的，即使是父类的实例也不行。

  + 创建对象的步骤：

    ```markdown
    (1)首先调用__new__得到一个对象
    (2)调用__init__为对象添加属性
    (3)将对象赋值给变量
    ```

  + `__init__`和`__new__`两个魔法方法的例子：

    ```python
    class A(object):
        pass
    
    class B(A):
        
        def __init__(self):
            print('__init__被调用......')
    
        def __new__(cls):
            print('__new__被调用......')
            print(id(cls))
            # 此处采用了参数A而不是cls，__new__没有正确返回当前类cls的实例
            return object.__new__(A)
    
    b = B()
    print(b, type(b))
    print(id(A), id(B))
    
    # 运行结果
    >>> __new__被调用......
    >>> 2219588983608
    >>> <__main__.A object at 0x00000204CA658400> <class '__main__.A'>
    >>> 2219588982664 2219588983608
    ```

    + 从运行结果可以看出，`__new__`中的参数`cls`和B的`id`是相同的，表明`__new__`中默认的参数`cls`就是B类本身，而在`return`时，并没有正确返回当前类`cls`的实例，而是返回了其父类A的实例，因此`__init__`这一魔法方法并没有被调用，此时`__new__`虽然是写在B类中的，但其创建并返回的是一个A类的实例对象。

    ```python
    # 现在将return中的参数A变为cls，再来看一下运行结果：
    class A(object):
        pass
    
    class B(A):
        
        def __init__(self):
            print('__init__被调用......')
    
        def __new__(cls):
            print('__new__被调用......')
            print(id(cls))
            # 此处采用了参数A而不是cls，__new__正确返回当前类cls的实例
            return object.__new__(cls)
    
    b = B()
    print(b, type(b))
    print(id(A), id(B))
    
    # 运行结果
    >>> __new__被调用......
    >>> 2483180430712
    >>> __init__被调用......
    >>> <__main__.B object at 0x0000024229AC93C8> <class '__main__.B'>
    >>> 2483180427880 2483180430712
    ```

    + 可以看出，当`__new__`正确返回其当前类`cls`的实例对象时，`__init__`被调用了，此时创建并返回的是一个B类的实例对象。

+ **`__class__()`**：获取已知随想的类（对象.`__class__`）

  ```python
  print(b.__class__)
  >>> <class '__main__.B'>
  ```

  + 当一个类中的某个成员属性是所有该类的对象的公共属性时，可以这样使用：

    ```python
    class A(object):
        count = 0
        def add_count(self):
            # self.__class__.count不再是单纯的某个对象私有的属性，而是类的所有实例对象的共有属性,它相当于self.A.count
            self.__class__.count += 1
            # self.count += 1
    
    a = A()
    a.add_count()
    print('*********a***********', a.count)
    >>> *********a*********** 1
    b = A()
    b.add_count()
    print('*********b***********', b.count)
    >>> *********b*********** 2
    ```

+ **`__slots__`**: 用来限制实例属性
  
  ```python
  class Student(object):
    __slots__ = ('name', 'age')

  >>> s = Student()
  >>> s.name = 'Michael
  >>> s.age = 20
  >>> s.score = 80
  Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  AttributeError: 'Student' object has no attribute 'score'
  ```

+ **`__str__()`**：该函数要求返回一个字符串，当实例对象作为`print`参数打印时会打印该字符串。当打印一个类时，`print`首先调用的时类里面定义的`__str__`

  ```python
  class A(object):
     
      def __init__(self, attr):
          self.attr = attr
  
      def __str__(self):
          return f'a的属性是{self.attr}'
  
  a = A('name')
  print(a)
  >>> a的属性是name
  print(A)
  >>> <class '__main__.A'>
  ```

+ **`__repr__()`**：是给机器用的，在Python解释器里面直接敲对象名再回车后调用的方法。在没有str时就相当于它本身的作用

  ![__repr__用法](https://github.com/lajos182/python-essay/blob/master/images/__repr___%20and%20__str__.png)

+ **`__del__()`**：对象在程序运行结束之后进行垃圾回收的时候调用这个方法，来释放资源。此时，此方法是被自动调用的。总而言之，`__del__`魔法方法是在对象没有变量再引用，其**引用计数**减为0，进行垃圾回收的时候自动调用的。

  ```python
  class A(object):
      num_count = 0 # 共有属性
      def __init__(self, name):
          self.name = name
          A.num_count += 1
          print(name, A.num_count)
  
      def __del__(self):
          A.num_count -= 1
          print('Del', self.name, A.num_count)
      
      def test(self):
          print('aaa')
  
  aa = A('hello')
  bb = A('world')
  cc = A('!!!!!')
  print('over')
  
  >>> hello 1
  world 2
  !!!!! 3
  over
  Del hello 2
  Del world 1
  Del !!!!! 0
  ```

+ **`__delattr__()`**：删除一个对象的属性时调用

+ **`__getattr__()`**：当访问不存在的对象属性时，系统会自动调用

+ **`__getattribute__()`**：访问存在的属性时调用（先调用该方法，查看是否存在该属性，若不存在，接着去调用`__getattr__`）

+ **`__setattr__()`**：设置成员属性时，系统会自动调用

  ```python
  class A(object):
      
      def __getattr__(self, item):
          print('访问不存在属性时调用__getattr__')
          try:
              return item
          except KeyError:
              raise AttributeError(f"'Dict' object has no attribute {item}")
      
      def __getattribute__(self, item):
          print('访问存在属性时调用__getattribute__')
          return object.__getattribute__(self, item) # 非绑定方法要显式传递self
  
      def __setattr__(self, item, value):
          print('设置对象成员属性的时候，自动调用__setattr__')
          self.__dict__[item] = value
  
      def __delattr__(self, item):
          print('销毁对象成员属性的时候，自动调用__delattr__')
          print('del', item)
  
  a = A()
  a.name = 'xiaoming'
  >>> 设置对象成员属性的时候，自动调用__setattr__
  访问存在属性时调用__getattribute__
  print(a.age)
  >>> 访问存在属性时调用__getattribute__
  访问不存在属性时调用__getattr__
  del a.name
  >>> 销毁对象成员属性的时候，自动调用__delattr__
  del name
  ```

+  **`__setitem__()`**：当对对象按照字典设置键值对时，会自动触发该方法

+ **`__getitem__()`**：当对对象按照字典操作根据键获取值时，会自动触发该方法

+ **`__delitem__()`**：当做字典操作，删除键值对时，自动触发该方法

  ```python
  class A(object):
      
      def __setitem__(self, key, value):
          print('调用了__setitem__方法')
          self.__dict__[key] = value
  
      def __getitem__(self, item):
          print('调用了__getitem__方法')
          return self.__dict__[item]
  
      def __delitem__(self, key):
          print('调用了__delitem__方法')
          del self.__dict__[key]
  
  a = A()
  a['name'] = name
  >>> '调用了__setitem__方法'
  print(a['name'])
  >>> '调用了__getitem__方法'
  name
  del a['name']
  >>> '调用了__delitem__方法'
  ```

+ **`__iter__()`**：只要定义了`__iter__()`方法对象，就可以使用迭代器访问，这意味着，我们可以迭代我们自己定义的对象。

  ```python
  class A(object):
      
      def __init__(self):
          self._obj = []
      
      def __iter__(self):
          return iter(self._obj)
  
      def add(self, obj):
          self._obj.append(obj)
  
  a = A()
  a.add(1)
  a.add(2)
  for i in a:
      print(i)
  ```

+ **`__call__()`**：当实例被当做函数进行调用时会触发

  ```python
  class A(object):
      
      def __init__(self):
          self.name = 'xiaoming'
      
      def __call__(self, age):
          return f'I am {self.name}, my age is {age} years old!'
  
  a = A()
  print(a(18))
  >>> I am xiaoming, my age is 18 years old!
  ```

+ **`__len__()`**：`len`调用后会调用对象的`__len__`函数，我们可以为其定制输出

  ```python
  class A(object):
      
      def __init__(self, array):
          self.array = array
  
      def __len__(self):
          return len(self.array) + 100
  
  a = A([1, 2, 3, 4, 5])
  print(len(a))
  >>> 105
  ```

### 2.7.3. 枚举类的使用

+ 当我们需要定义常量时，通常使用大写变量通过整数来定义，例如月份，好处时简单，缺点是类型是`int`，并且仍然是变量。

 ```python
 JAN = 1
 FEB = 2
 MAR = 3
 ...
 NOV = 11
 DEC = 12
 ```

+ 更好的办法是为这样的枚举类型定义一个`class`类型，然后每个常量都是`class`的一个唯一实例。Python提供了`Enum`类来实现这个功能:

```python
from enum import Enum

Month = Enum('Month', ('Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'))

# 这样我们就获得了Month类型的枚举类，可以直接使用Month.Jan来引用一个常量，或者枚举它的所有成员：
for name, member in Month.__members__.items():
    print(name, '=>', member, ',', member.value)
```

+ 自定义枚举类：更精确的控制枚举类型，可以从`Enum`派生出自定义类,使用`@unique`装饰器可以帮助我们检查保证没有重复值

```python
from enum import Enum, unique

@unique
class Weekday(Enum):
    Sun = 0 # Sun的value被设定为0
    Mon = 1
    Tue = 2
    Wed = 3
    Thu = 4
    Fri = 5
    Sat = 6

# 访问这些枚举类型的方法：
>>> day1 = Weekday.Mon
>>> print(day1)
Weekday.Mon
>>> print(Weekday.Tue)
Weekday.Tue
>>> print(Weekday['Tue'])
Weekday.Tue
>>> print(Weekday.Tue.value)
2
>>> print(day1 == Weekday.Mon)
True
>>> print(day1 == Weekday.Tue)
False
>>> print(Weekday(1))
Weekday.Mon
>>> print(day1 == Weekday(1))
True
>>> Weekday(7)
Traceback (most recent call last):
  ...
ValueError: 7 is not a valid Weekday
>>> for name, member in Weekday.__members__.items():
...     print(name, '=>', member)
...
Sun => Weekday.Sun
Mon => Weekday.Mon
Tue => Weekday.Tue
Wed => Weekday.Wed
Thu => Weekday.Thu
Fri => Weekday.Fri
Sat => Weekday.Sat
```

+ 枚举类的使用

```python
from enum import Enum, unique

class Gender(Enum):
    Male = 0
    Female = 1

class Student(object):
    def __init__(self, name, gender):
        self.name = name
        self.gender = gender

# 测试
mary = Student('Mary', name, Gender.Female):
if mary.gender == Gender.Female:
    print('测试通过')
else：
    print('测试失败')
```

### 2.7.4. 类的继承

+ **继承**：父类的属性和方法子类可以直接拥有的称为继承。

  ```python
  class Animal(object):
  
      def __init__(self, name):
          self.name = name
  
      def run(self):
          print('动物一般都喜欢跑！')
  
  class Dog(Animal):
  
      pass
  
  d = Dog('wangcai')
  # 直接继承父类的属性
  print(d.name)
  # 直接拥有父类的方法
  d.run()
  >>> wangcai
  动物一般都喜欢跑！
  ```

+ **派生**：子类在父类的基础上衍生出来的新的特征(属性和方法)。

  ```python
  class Animal(object):
  
      def __init__(self, name):
          self.name = name
  
      def run(self):
          print('动物一般都喜欢跑！')
  
  class Rabbit(Animal):
      # 添加方法
      def eat(self):
          print('爱吃萝卜和青菜！')
  
  rabbit = Rabbit('xiaobai')
  rabbit.eat()
  >>> 爱吃萝卜和青菜！
  # 添加属性
  rabbit.color = 'white'
  print(rabbit.color)
  >>> white
  ```

+ **重写**：父类的方法完全不合适，子类需要全部的覆盖。或者是父类的方法合适，但需要完善。

  ```python
  class Animal(object):
  
      def run(self):
          print('动物一般都喜欢跑！')
  
      def eat(self):
          print('小动物也是一天三顿！')
  
  class Cat(Animal):
      # 当父类的方法完全不合适时，可以覆盖重写
      def run(self):
          print('喜欢走猫步！')
      # 父类的方法合适，但是子类需要添加内容完善功能
      def eat(self):
          # 调用父类方法，不建议使用
          # Animal.eat(self)
          # super(Cat, self).eat()
          # 类名及self可以不传
          super().eat()
          print('最喜欢吃鱼！')
  
  jerry = Cat()
  jerry.run()
  >>> 喜欢走猫步！
  jerry.eat()
  >>> 小动物也是一天三顿！
  最喜欢吃鱼！
  ```

### 2.7.5. 多继承

+ **多继承**：继承多个父类，会涉及到查找顺序(MRO)、重复调用(钻石继承，也叫菱形继承问题)等。

  ```python
  class Father(object):
      def __init__(self, money):
          self.money = money
  
      def play(self):
          print('play basketball')
  
      def eat(self):
          print('喜欢吃红烧肉！')
  
  class Mother(object):
      def __init__(self, face_value):
          self.face_value = face_value
  
      def makeup(self):
          print('like make up')
  
      def eat(self):
          print('喜欢吃饺子！')
  
  class Son(Father, Mother):
      def __init__(self, money, face_value, hobby):
          # 多继承时无法使用super()，因为super()只可以再单继承中使用，当然子类也可以扩展自己的属性
          Father.__init__(self, money)
          Mother.__init__(self, face_value)
          self.hobby = hobby
  
  son = Son(500, 100, 'IT')
  print(son.money)
  >>> 500
  print(son.face_value)
  >>> 100
  # eat继承的父类都有该方法，会根据继承的顺序谁在前继承谁
  son.eat()
  >>> 喜欢吃红烧肉！
  son.makeup()
  >>> like make up
  son.play()
  >>> play basketball
  ```

+ `MRO`即`method resolution order`，用于判断子类调用的属性来自于哪个父类。在Python2.3之前，`MRO`是基于**深度优先算**法的，自2.3开始使用`C3`算法，定义类时需要继承`object`，这样的类称为**新式类**，否则为**旧式类**。案例可查看<a name='#1.7'>第一部分(1.7)新式类和旧式类</a>

  ![旧式类和新式类](https://github.com/lajos182/python-essay/blob/master/images/MRO%20and%20C3.png)

### 2.7.6. 多态性

+ **多态**：一种食物的多种形态。

+ 案例：

  + 如果要定义两个类(猫和老鼠)，他们分别都有`name`属性和`eat`方法，代码实现：

    ```python
    class Cat(object):
        def __init__(self, name):
            self.name = name
        def eat(self):
            print(f'{self.name}在吃！')
            
    class Mouse(object):
        def __init__(self, name):
            self.name = name
        def eat(self):
            print(f'{self.name}在吃！')
    tom = Cat('tom')
    jerry = Mouse('jerry')
    tom.eat()
    >>> tom在吃！
    jerry.eat()
    >>> jerry在吃！
    ```

  + 如果有100种动物，他们都有`name`属性和`eat`方法，当然不需要这样写，就把这些动物都继承自一个基类。(如果一种植物也有这个属性和方法时，也可以继承自这个基类，这就是**鸭子模型**)。

    ```python
    class Animal(object):
         def __init__(self, name):
            self.name = name
        def eat(self):
            print(f'{self.name}在吃！')
            
    class Cat(Animal):
        def __init__(self, name):
            return super(Cat, self).__init__(name)
    
    class Mouse(Animal):
        def __init__(self, name):
            return super().__init__(name)
    tom = Cat('tom')
    jerry = Mouse('jerry')
    tom.eat()
    >>> tom在吃！
    jerry.eat()
    >>> jerry在吃！   
    ```

  + 如果人要给100种动物喂食物，如何实现呢？

    ```python
    class Person(object):
        '''
        def feedCat(self, cat):
            print('给你食物！')
            cat.eat()
        
        def feedMouse(self, mouse):
            print('给你食物！')
            mouse.eat()
        '''
        # 只需要写一种方法，直接给这些动物继承的基类作为一个对象
        def feed_animal(self, animal):
            print('给你食物')
            animal.eat()
    per = Person()
    # tom和jerry都继承自动物
    per.feed_animal(tom)
    per.feed_animal(jerry)     
    ```

### 2.7.7. 封装性

**封装**：隐藏对象的属性和实现细节，仅对外提供公共访问方式。这样的好处：**将变化隔离**、**便于使用**、**提高复用性**、**提高安全性**。

**封装原则**：①将不需要对外提供的内容都隐藏起来；②把属性都隐藏，提供公共方法对其访问

**广义的封装**：把属性函数都放到类里。

**侠义的封装**：定义私有成员。

+ **访问权限**：

  + 共有的：类中的普通属性和方法，默认都是公有的，可以在类的内部、外部、子类中使用

  + 私有的：其实仅仅是一种变形操作，类中所有双下划线开头的名称(`__x`)都会自动变形成：`_类名__x`的形式。只能在本类的内部使用，不能再外部及子类中使用，且有些方法或属性 不希望被子类继承。

  ```python
  class Person(object):
  
      def __init__(self, name, age):
          self.name = name
          # 在属性的前面添加两个'_'，外部访问，系统内部的除外
          # 默认的属性名：__age => _Person__age
          self.__age = age
  
      def eat(self):
          print('民以食为天！')
      
      #  在方法的前面添加两个'_'
      def __inner(self):
          print('私有方法，不想让外部调用！')
  
      def test(self):
          # 在类的内部可以访问私有属性和方法
          print(self.__age)
          self.__inner()
          self.eat()
  
  p = Person('老王', 50)
  # 默认所有的属性和方法都是公有的，就是在类的外面可以直接使用
  p.eat()
  >>> 民以食为天！
  print(p.name)
  >>> 老王
  # 以下两句会报错，提示没有相关的属性或方法
  # p.__inner()
  # print(p.__age)
  # 可以通过系统修改的名称找到，但是强烈建议不要这样使用
  print(p._Person__age)
  >>> 18
  p._Person__inner()
  >>> 私有方法，不想让外部调用！
  # 调用类的内部方法可以访问
  p.test()
  
  class Man(Person):
      
      def __inner(self):
          print('我想覆盖父类的属性，但没有办法！')
  
      def eat(self):
          print('我就是爱吃肉！')
  
  m = Man('lajos', 18)
  m.test()
  >>> 18
  私有方法，不想让外部调用！ # 子类无法修改父类的方法
  我就是爱吃肉！ # 这个eat()不是私有方法，被覆盖
  
  ```

+ **封装与扩展性**

  > 封装在于明确区分内外，使得类实现者可以修改封装内的东西而不影响外部调用者的代码；而外部使用者只需要知道一个接口(函数)，只要接口(函数)名、参数不变，合作基础使用者的代码永远无需改变。这就是提供一个良好的——或者说，只要接口这个基础约定不变，则代码改变不足为虑。

  ```python
  # 类的设计者
  class Room(object):
  
      def __init__(self, name, owner, width, length, high):
          self.name = name
          self.owner = owner
          self.__width = width
          self.__length = length
          self.__high = high
      
      def tell_area(self): # 对外提供的接口，隐藏了内部的实现细节，此时我们想求的是面积
          return self.__width * self.__length
  
  r1 = Room('卧室', 'egon', 20, 20, 20)
  print(r1.tell_area()) # 使用者调用接口tell_area
  >>> 400
  
  # 类的设计者，轻松的扩展了功能，而类的使用者完全不需要改变自己的代码
  class Room:
      def __init__(self,name,owner,width,length,high):
          self.name=name
          self.owner=owner
          self.__width=width
          self.__length=length
          self.__high=high
      def tell_area(self): 
          # 对外提供的接口，隐藏内部实现，此时我们想求的是体积,内部逻辑变了,只需求修该下列一行就可以很简答的实现,而且外部调用感知不到,仍然使用该方法，但是功能已经变了
          return self.__width * self.__length * self.__high
  
  
  # 对于仍然在使用tell_area接口的人来说，根本无需改动自己的代码，就可以用上新功能
  prnit(r1.tell_area())
  >>> 8000
  ```

### 2.7.8. 类属性

**类属性**：定义类时，卸载类中，但是方法外的属性，通常放在类的开头位置。

```python
class Person(object):
    nation = 'China'

    def __init__(self, name):
        self.name = name
        self.nation = '中国'
# 通过类名访问类属性
print(Person.nation)
# print(Person.name)
# 通过对象也可一访问类属性，但是不建议
# 当对象有同名的成员属性时，使用的就是成员属性
p = Person('xiaoming')
print(p.nation)

# 也可以动态添加
Person.hello = 'hello'
print(Person.hello)

# 特殊的类属性
# 表示的类名字字符串，对象没有该属性
print(Person.__name__)
# 表示父类构成的元组，对象没有该属性
print(Person.__bases__)

# 存储类相关的信息
print(Person.__dict__)
print(p.__dict__)
```

### 2.7.9. 类方法(classmethod)

**类方法**：定义时使用装饰器`@classmethod`，通过类名进行调用。可以创建对象或者简介的创建对象，对外提供简单易用的接口。传入的第一个参数为`cls`，是类本身，并且，类方法可以通过类直接调用，或通过实例直接调用。但无论哪种调用方式，最左侧传入的参数一定是类本身。

```python
class A(object):

    @classmethod
    def func(cls):
        print('我是类方法！')

A.func() # 通过类直接调用
a = A()
a.func() # 通过实例对象调用
```

### 2.7.10. 静态方法(staticmethod)

**静态方法**：使用装饰器`@staticmethod`进行装饰，定义是不需要第一个参数`cls`。调用过程中，无需进行实例化。

```python
class A(object):

    @staticmethod
    def func():
        print('我是静态方法！')
A.func() # 通过类直接调用
a = A()
a.func() # 通过实例对象调用
```

> 重点来了：[**Python中的实例方法、类方法和静态方法有什么区别？**](https://blog.csdn.net/sinat_41898105/article/details/80661798)
>
> 三种方法都可以通过对象进行调用，但类方法和静态方法无法访问对象属性，类方法通过对象调用获取的仍是类属性（并非对象属性）；普通方法无法通过类名调用，类方法和静态方法可以，但静态方法不能进行访问，仅仅只是通过传值得方式（与函数调用相同）

### 2.7.11. 属性函数

**属性函数**：将方法当作属性一样调用，保护或处理特定属性。

```python
import hashlib
class User(object):
    
    def __init__(self, username, password):
        self.username = username
        self.__password = password

    # 使用property装饰的方法，可以当作属性访问
    # 可以保护特定的属性
    @property
    def password(self):
        print('有人想直接获取密码！')
        # 可以给出警告提醒
        return self.__password
    
    # 当设置password属性是，会自动调用该方法
    @password.setter
    def password(self, password):
        print('注意了，有人想修改密码', password)
        # 可以对密码进行特定处理，然后保存
        md = hashlib.md5()
        md.update(password.encode('utf-8'))
        self.__password = md.hexdigest()

user = User('xiaoming', '123456')
print(user.username)
# 很多时候直接访问密码是不需要的，也是不安全的
# 直接访问password属性，自动回调用使用property修饰后的password方法
print(user.password)
# 修改属性时会调用setter装饰的方法
user.password = '654321'
```

### 2.7.12. 对象判断

+ **判断一个对象是否可以像函数一样进行调用？**

  ```python
  class A(object):
      def __call__(self, *args, **kwargs):
          print('++++')
  
  def test():
      pass
  
  
  # 不能使用isinstance方法判断一个对象是否是函数
  # isinstance(test, function)
  
  # 打印时仍然是function类型
  # print(type(test))
  
  # 判断一个对象是否可以像函数一样调用
  print(callable(test))
  >>> True
  a = A()
  print(callable(a))
  >>> True
  
  # 判断对象是否拥有call属性
  print(hasattr(test, 'call'))
  >>> False
  print(hasattr(a, 'call'))
  >>> False
  
  # 判断是否是函数
  from inspect import isfunction
  print(isfunction(test))
  >>> True
  print(isfunction(a))
  >>> False
  ```

## 2.8. IO编程

### 2.8.1. 文件读写

读写文件是最常见的IO��作。Python内置了读写文件的函数，用法和C是兼容的。

读写文件前，我们先必须了解一下，在磁盘上读写文件的功能都是由操作系统提供的，现代操作系统不允许普通的程序直接操作磁盘，所以，读写文件就是请求操作系统打开一个文件对象（通常称为文件描述符），然后，通过操作系统提供的接口从这个文件对象中读取数据（读文件），或者把数据写入这个文件对象（写文件）。

详细的操作见<a name='#IO编程'>4.10</a>

+ 字符编码

要读取非UTF-8编码的文本文件，需要给`open()`函数传入`encoding`参数，例如，读取GBK编码的文件, 遇到有些编码不规范的文件，你可能会遇到UnicodeDecodeError，因为在文本文件中可能夹杂了一些非法编码的字符。遇到这种情况，`open()`函数还接收一个`errors`参数，表示如果遇到编码错误后如何处理。最简单的方式是直接忽略.

```python
>>> f = open('/Users/Administrator/gbk.txt', 'r', encoding='gbk')
>>> f.read()
'测试'
>>> f = open('/Users/Administrator/gbk.txt', 'r', encoding='gbk', errors='ignore)
```

### 2.8.2. `StringIO`和`BytesIO`

很多时候，数据读写不一定是文件，也可以在内存中读写。

+ `StringIO`：在内存中读写`str`

  + 要把`str`写入`StringIO`，我们需要先创建一个`StringIO`，然后，像文件一样写入即可：

    ```python
    >>> from io import StringIO
    >>> f = StringIO()
    >>> f.write('hello')
    5
    >>> f.write(' ')
    1
    >>> f.write('world!')
    6
    # `getvalue()`方法用于获取写入后的`str`
    >>> print(f.getvalue())
    hello world!
    ```
  + 要读取`StringIO`,可以用一个`str`初始化`StringIO`,然后像文件一样读取

    ```python
    >>> from io import StringIO
    >>> f = StringIO('Hello!\nHi!\nGoodbye!')
    >>> while True:
    ...     s = f.readline()
    ...     if s == '':
    ...         break
    ...     print(s.strip())
    ...
    Hello!
    Hi!
    Goodbye!
    ```
+ `BytesIO`：`StringIO`操作的只能是`str`，如果要操作二进制数据，就需要使用`BytesIO`。
  
  + `BytesIO`实现了在内存中读写`bytes`，我们创建一个`BytesIO`，然后写入一些`bytes`。请注意，写入的不是`str`，而是经过`UTF-8`编码的`bytes`。
    
    ```python
    >>> from io import BytesIO
    >>> f = BytesIO()
    >>> f.write('中文'.encode('utf-8'))
    6
    >>> print(f.getvalue())
    b'\xe4\xb8\xad\xe6\x96\x87'
    ```
  + 和`StringIO`类似，可以用一个`bytes`初始化`BytesIO`，然后，像读文件一样读取。
    
    ```python
    >>> from io import BytesIO
    >>> f = BytesIO(b'\xe4\xb8\xad\xe6\x96\x87')
    >>> f.read()
    b'\xe4\xb8\xad\xe6\x96\x87'
    ```

### 2.8.3. `bytes`函数的使用

`bytes`函数返回一个新的`bytes`对象，该对象是一个0<=x<=256区间的整数不可变序列，它是`bytearray`的不可变版本。

+ `bytes([source[, encoding[, errors]]])`：返回一个新的`bytes`对象
    - 如果`source`为整数，则返回一个长度为`source`的初始化数组
    - 如果`source`为字符串，则按照指定的`encoding`将字符串转化为字节序列
    - 如果`source`为可迭代类型，则元素必须[0, 255]中的整数
    - 如果`source`为与`buffer`接口一致的对象，则此对象也可以被用于初始化`bytearray`
    - 如果没有输入任何参数，默认就是初始化数组为0个元素

```python
a = bytes([1, 2, 3, 4])
print(a)
print(type(a))
>>>  b'\x01\x02\x03\x04'
<class 'bytes'>

a = [0xe0, 0xb9, 0x80, 0xe0, 0xb8, 0xa7, 0xe0, 0xb9, 0x87, 0xe0, 0xb8, 0x9a, 0xe0,0xb9, 0x84, 0xe0, 0xb8, 0x8b, 0xe0, 0xb8, 0x95, 0xe0, 0xb9, 0x8c]
b  = bytes(a)
print(b)
c = b.decode('utf-8')
print(c)
>>> b'\xe0\xb9\x80\xe0\xb8\xa7\xe0\xb9\x87\xe0\xb8\x9a\xe0\xb9\x84\xe0\xb8\x8b\xe0\xb8\x95\xe0\xb9\x8c'
เว็บไซต์
```

### 2.8.4. 序列化

+ 一般数据持久化存储采用三种方式：**普通文件**、**数据库**、**序列化**

+ **`pickle`**：`pickle.dump(obj, fp)`将对象存储到文件，`pickle.load(fp)`将文件转化为对象

  ```python
  import pickle
  class Person(object):
      def __init__(self, name, age):
          self.name = name
          self.age = age
      
  # 存储：对象=>文件
  xiaoming = Person('xiaoming', 18)
  fp = open('text.txt', 'wb')
  pickle.dump(xiaoming, fp)
  print('对象数据存储完毕！')
  fp.close()
  
  # 读取：文件=>对象
  fp = open('text.txt', 'rb')
  xiaoming = pickle.load(fp)
  print(xiaoming.name, xiaoming.age)
  fp.close()
  ```
 `json`：如果我们要在不同的编程语言之间传递对象，就必须把对象序列化为标准格式，比如XML，但更好的方法是序列化为JSON，因为JSON表示出来就是一个字符串，可以被所有语言读取，也可以方便地存储到磁盘或者通过网络传输。JSON不仅是标准格式，并且比XML更快，而且可以直接在Web页面中读取，非常方便。

|**JSON类型**|**Python类型**|
|:---:|:---:|
|{}|dict|
|[]|list|
|"string"|str|
|1234.56|int或float|
|true/false|True/False|
|null|None|

`Python`内置的`json`模块提供了非常完善的`Python`对象到`JSON`格式的转换。我们先看看如何把`Python`对象变成一个`JSON`.`dumps()`方法返回一个`str`，内容就是标准的`JSON`。类似的，`dump()`方法可以直接把`JSON`写入一个`file-like Object`。

```python
>>> import json
>>> d = dict(name='Bob', age=20, score=88)
>>> json.dumps(d)
'{"age": 20, "score": 88, "name": "Bob"}'
```

要把`JSON`反序列化为`Python`对象，用`loads()`或者对应的`load()`方法，前者把`JSON`的字符串反序列化，后者从`file-like Object`中读取字符串并反序列化。由于`JSON`标准规定`JSON`编码是`UTF-8`，所以我们总是能正确地在`Python`的`str`与`JSON`的字符串之间转换。

```python
>>> json_str = '{"age": 20, "score": 88, "name": "Bob"}'
>>> json.loads(json_str)
{'age': 20, 'score': 88, 'name': 'Bob'}
```

`Python`的`dict`对象可以直接序列化为`JSON`的{}，不过，很多时候，我们更喜欢用`class`表示对象，比如定义Student类，然后序列化：

```python
import json

class Student(object):
    def __init__(self, name, age, score):
        self.name = name
        self.age = age
        self.score = score

s = Student('Bob', 20, 88)
print(json.dumps(s))

>>> Traceback (most recent call last):
  ...
TypeError: <__main__.Student object at 0x10603cc50> is not JSON serializable
# 这是因为`dumps()`在序列化对象时，需要提供可选参数
# 可选参数default就是把任意一个对象变成一个可序列为JSON的对象，我们只需要为Student专门写一个转换函数，再把函数传进去即可：
def student_to_dict(std):
    return {
        'name': std.name,
        'age': std.age,
        'score': std.score
    }
>>> print(json.dumps(s, default=student_to_dict))
{"age": 20, "name": "Bob", "score": 88}
>>> print(json.dumps(s, default=lambda obj: obj.__dict__))
```

同样的道理，如果我们要把JSON反序列化为一个Student对象实例，`loads()`方法首先转换出一个dict对象，然后，我们传入的`object_hook`函数负责把`dict`转换为Student实例：

```python
def dict_to_student(d):
    return Student(d['name'], d['age'], d['score'])
>>> json_str = '{"age": 20, "score": 88, "name": "Bob"}'
>>> print(json.loads(json_str, object_hook=dict2student))
<__main__.Student object at 0x10cd3c190>
```

## 2.9. 异常处理

+ **错误**：程序运行前的语法问题，如：关键字、缩进、括号不成对等。
+ **异常**：在程序运行过程中出现的错误，如：变量未定义、除数为0、属性不存在等。
+ **异常处理**：异常处理可以认为是一种特殊的路程控制语句，可以提高代码的健壮性。

+ **基本结构**：

  ```python
  try:
      print('正常执行')
      # print(a)
      print(3/0)
  except Exception as e:
      # Exception是所有异常的基类，因此此处可以捕获所有异常
      print('出现异常，进行处理')
      print(e)
  
  print('其他代码')
  ```

+ 捕获多个异常：

  ```python
  try:
      # print(a)
      # print(3/0)
      fp = open('123.txt')
  except NameError as e:
      print('NameError:', e)
  except ZeroDivisionError as e:
      print('ZeroDivisionError:', e)
  except Exception as e:
      print('other:', e)
  ```

+ 也可以对多种异常进行分组处理：

  ```python
  try:
      # print(a)
      # print(3/0)
      fp = open('123.txt')
  except (NameError, ZeroDivisionError) as e:
      # 将特定的某些异常统一处理，写到元组中即可
      print(e)
  except:
      print('其他异常')
  ```

+ `else`和`finally`：

  ```python
  try:
      print('正常执行')
      print(a)
  except:
      print('出现异常')
  else:
      # 出现异常就不执行了
      print('正常结束')
  finally:
      # 无论有误异常都会执行
      print('无论如何都执行')
  ```

  > `else`：在没有异常的时候会执行，出现异常就不执行了
  >
  > `finally`：无论是否有异常，都会执行

+ **抛出异常`raise`**：

  ```python
  try:
      print('开始')
      # 根据代码逻辑的需要，手动抛出特定的异常
      raise Exception('手动抛出异常')
      print('一切正常')
  except Exception as e:
      print('出现异常:', e)
  
  print('结束')
  ```

+ 异常嵌套：`try-except`结构中嵌套`try-except`结构

  ```python
  print('我要去上班，什么事情都不能阻止我上班的脚步')
  try:
      print('我准备骑电动车')
      raise Exception('昨天晚上那个缺德的家伙把我充电器给拔了，无法骑车')
      print('骑电动车提前到达公司')
  except Exception as e:
      print(e)
      try:
          print('我准备坐公交')
          raise Exception('等了20分钟一直没有公交车，果断放弃')
          print('坐公交准时到达公司')
      except Exception as e:
          print(e)
          print('我准备打车')
          print('打车还是快，一会就到公司了')
  
  print('热情满满的开始一天的工作')
  ```

+ 自定义异常类：继承自异常的基类(`Exception`)

  ```python
  # 自定义异常类，名字通常以Exception结尾
  class MyException(Exception):
      def __init__(self, msg):
          self.msg = msg
  
      def __str__(self):
          # repr键变量转换成字符串，若本身是字符串则不必要
          # return repr(self.msg)
          return self.msg
  
      def deal(self):
          print('异常已处理')
  
  try:
      print('正常执行')
      raise MyException('手动抛出定义异常')
  except MyException as e:
      print(e)
      e.deal()
  ```

+ 特殊使用：

  + 场景：做文件操作时，中间无论读写，也无论有误异常，最终一定要把文件关闭

  + `with`：使用`with`，不必再关系文件的关闭问题，`with`语句块结束后一定会确保文件关闭

    ```python
    # fp = open('test.txt', 'rb')
    # # 各种读写操作
    # fp.close()
    
    # 使用with，无需关心文件的关闭问题
    with open('test.txt', 'rb') as fp:
        content = fp.read(5)
        print(content)
    ```

## 2.10. 正则表达式

### 2.10.1. 正则基础

**应用场景**：特定规律字符串的查找、替换、切割等；邮箱格式、url等的验证；爬虫项���，提取特定的有效内容；很多应用的配置文件

**使用原则**：只要能够通过自负床等相关函数能够解决的，就不要使用正则；正则的执行效率比较低，会降低代码的可读性；

**基本使用**：正则式通过`re`模块提供支持的，相关函数包括`match`、`search`、`findall`、`compile`

+ `match`：从头惊醒匹配，知道就立即返回正则结果对象，没有就返回`None`
+ `search`：匹配全部内容，任意位置，只要找到，立即返回正则结果对象，没有返回`None`
+ `findall`：匹配所有内容，返回匹配结构组成的列表，没有返回`None`
+ `compile`：根据字符串生成正则表达式的对象，用于特定正则匹配，通过`match`、`search`、`findall`

### 2.10.2. 正则规则

+ 单个字符：

  ```markdown
  普通字符：就是一对一的完全匹配
  []：中间的任意一个字符
  	[a-z]：表示a到z的任意字符
  	[0-9]：表示0到9的任意字符
  	[^abc]：除abc之外的字符
  . ：匹配'\n'以外的任意字符
  \d：所有的数字字符，等价于[0-9]
  \D：所有的非数字字符，等价于[^0-9]
  \w：所有的数字、字母、中文、下划线等 (就是字的意思)
  \W：\w之外的所有字符
  \s：所有的空白字符，如：空格、\t、\n、\r
  \S：\s之外的所有字符
  \b：词边界，如：开头、结尾、标点、空格等
  \B：非词边界
  ```

+ 次数控制：

  ```
  *：前面的字符可以是任意次
  +：前面的字符至少出现一次
  ?：至多一次，0次或1次
  {m}���匹配固定的m次
  {m,}：至少m次
  {m,n}：m到n次
  ```

  > 正则的匹配默认是贪婪的
  >
  > 贪婪：最大限度的匹配，正则的匹配默认是贪婪的
  >
  > 非贪婪：只要满足匹配条件，能少匹配就少匹配，通常使用'?'取消贪婪

  ```python
  import re
  
  # c = re.compile(r'a.*?c')
  c = re.compile(r'a.+?c')
  
  s = c.search('abcjsdhfkdkc')
  
  if s:
      print('ok')
      print(s.group())
  >>> ok
  abc
  ```

+ 边界限定

  ```markdown
  ^：以指定内容开头
  $：以指定内容结尾
  ```

+ 分组匹配

  ```markdown
  |：表示或，具有最低的优先级
  ()：用于表示一个整体，可以确定优先级
  ```

  ```python
  import re
  c = re.compile(r'(\d+)([a-z]+)(\d+)')
  s = c.search('sda123ksdak456sdk')
  if s:
      print('ok')
      print(s.group())   //所有匹配的字符(即匹配正则表达式整体结果)
      print(s.group(0))  //与group()相同
      print(s.group(1))  //列出第一个括号匹配的字符
      print(s.group(2))  //列出第二个括号匹配部分
      print(s.group(3))  //列出第三个括号匹配部分
      print(s.groups())  //返回所有括号匹配的字符，以tuple格式
  ```

  ```python
  import re
  
  # 正则中的\1:表示前面第一个小阔号匹配的结果
  # c = re.compile(r'<([a-z]+)><([a-z]+)>\w*</\2></\1>')
  # c = re.compile(r'<(?P<hello>[a-z]+)><(?P<world>[a-z]+)>\w*</\2></\1>')
  # 可以给指定的分组起个名字
  c = re.compile(r'<(?P<hello>[a-z]+)><(?P<world>[a-z]+)>\w*</(?P=world)></(?P=hello)>')
  
  s = c.search('xxx<div><a>百度一下</a></div>yyy')
  
  if s:
      print('ok')
      print(s)
      print(s.group())
  ```

+ 转义字符

  ```markdown
  在匹配所有正则中有特殊含义的字符时，都需要转义。
  正则字符串需要被处理两次，python中处理，正则解析时处理一次。
  通常在写正则字符串时，前面都加一个'r'，表示原始字符，让所有的字符失去意义。
  在匹配有如：'\'的字符时，前面再添加一个'\'就可以了，如果没有添加'r'，通常要写好几个。
  ```

### 2.10.3. 正则高阶

+ 匹配模式

  正则可以对匹配的模式做出整体的修饰处理，如忽略大小写等。

  ```python
  import re
  
  # 忽略大小写
  # c = re.compile(r'hello', re.I)
  
  # 多行匹配
  # c = re.compile(r'^hello', re.M)
  
  # 作为单行处理  或  让 . 匹配 '\n'
  c = re.compile(r'<div>.*?</div>', re.S)
  string = ''''<div>\n
  hello\n</div>'''
  s = c.search(string)
  if s:
      print('ok')
      print(s.group())
  ```

+ 字符串切割`split`

  某些情况下，无法通过字符串函数进行切割，可以使用正则的方式处理，如：按照数字切割。可使用`split`切割，返回一个列表

  ```python
  import re
  
  c = re.compile(r'\d')
  string = '正则1其实也不难2但是学完发现自己写不出来3是这样吧'
  ret = c.split(string, maxsplit=2)
  print(ret)
  print(type(ret))
  >>> ['正则', '其实也不难', '但是学完发现自己写不出来3是这样吧']
  <class 'list'>
  ```

+ 字符串替换`sub`

  简单的替换可以自己处理，要是按���正则规律进行替换就要使用专用的函数`sub`处理。

  ```python
  import re
  
  c = re.compile(r'\d')
  string = 'sa1erfewr2fsdfs3dfsd'
  ret = c.sub('***', string)
  print(ret)
  ```

## 2.11. 进程

### 2.11.1. 进程简介

- 进程（任务）：
- 在计算机中，其实进程就是一个任务。
- 在操作系统中，进程是程序执行和资源分配的基本单元。
- 单核CPU实现多任务
  - 只是将CPU的时间快速的切换和分配到不同的任务上。
  - 主频足够高，切换足够快，人的肉眼无法分辨而已。
- 多核CPU实现多任务
  - 如果任务的数量不超过CPU的核心数，完全可以实现一个核心只做一个任务。
  - 在操作系统中几乎是不可能的，任务量往往远远大于核心数。
  - 同样采用轮训的方式，轮流执行不同的任务，只是做任务的'人'有多个而已。

`Unix/Linux`操作系统提供了一个`fork()`系统调用，它非常特殊。普通的函数调用，调用一次，返回一次，但是`fork()`调用一次，返回两次，因为操作系统自动把当前进程（称为父进程）复制了一份（称为子进程），然后，分别在父进程和子进程内返回。

子进程永远返回0，而父进程返回子进程的ID。这样做的理由是，一个父进程可以fork出很多子进程，所以，父进程要记下每个子进程的ID，而子进程只需要调用`getppid()`就可以拿到父进程的ID。

```python
import os

print(f'Process {os.getpid()} start...')
# Only works on Unix/Linux/Mac:
pid = os.fork()
print(pid)
if pid == 0:
    print(f'I am child process ({os.getpid()}) and my parent is {os.getppid()})')
else:
    print(f'I ({os.getpid()}) just created a child process {pid}')

>>> Process (876) start...
I (876) just created a child process (877).
I am child process (877) and my parent is 876.
```

由于Windows没有fork调用，上面的代码在Windows上无法运行。有了fork调用，一个进程在接到新任务时就可以复制出一个子进程来处理新任务，常见的`Apache`服务器就是由父进程监听端口，每当有新的http请求时，就fork出子进程来处理新的http请求。

### 2.11.2. 进程的并发与并行

+ **并发**：并发是指在资源有限的情况下，两者交替轮流使用资源，比如一段路(单核CPU资源)同时只能过一个人，A走一段后，让给B，B用完继续给A，交替使用，目的是提高效率。

+ **并行**：并行是指两者同时执行，比如赛跑，两个人都在不停的往前跑（资源够用，比如三个线程，四核的CPU）；

+ **区别**：并发是从宏观上，在一个时间段上可以看出是同时执行的，比如一个服务器同时处理多个session。并行是从微观上，也就是在一个精确的时间片刻，有不同的程序在执行，这就要求必须有多个处理器。

### 2.11.3. 进程管理

```python
from multiprocessing import Process
import os

def run(name):
    print(f'Run child process {name} ({os.getpid()})')

if __name__ == "__main__":
    print(f'Parent process {os.getpid()}')
    # 创建进程，指定任务函数，target就是指定任务的函数，name代表进程名称， args和kwargs表示传递给子进程任务函数的参数
    p = Process(target=run, args=('test',))
    print('Child process will start...')
    p.start()
    p.join()
    print('Child process end...')
```

+ `os.getpid()`：获取当前的进程id

+ `os.getppid()`：获取主进程id

+ `Process([group [, target [, name [, args [, kwargs]]]]])`：由该类实例化得到的对象，表示一个子进程中的任务（尚未启动），需要使用关键字的方式来指定参数，args指定的为传给target函数的位置参数，是一个元组形式，必须有逗号
  
  -group参数未使用，值始终为None
  -target表示调用对象，即子进程要执行的任务
  -name为子进程的名称
  -args表示调用对象的位置参数元组，args=(1, 2, 'egon',)
  -kwargs表示调用对象的字典，kwargs={'name': 'egon', 'age': 18}

+ `p.daemone`：默认值为`False`，如果设为`True`，代表p为后台运行的守护进程，当p的父进程终止时，p也随之终止，并且设定为True后，p不能创建自己的新进程，必须在`p.start()`之前设置

+ `p.name`：进程的名称

+ `p.pid`：进程pid

+ `p.exitcode`：进程在运行时为None、如果为–N，表示被信号N结束(了解即可)

+ `p.authkey`：进程的身份验证键,默认是由`os.urandom()`随机生成的32字符的字符串。这个键的用途是为涉及网络连接的底层进程间通信提供安全性，这类连接只有在具有相同的身份验证键时才能成功（了解即可）

+ `p.start()`：启动进程，并调用该子进程中的`p.run()`

+ `p.run()`：进程启动时运行的方法，正是它去调用`target`指定的函数，我们自定义类的类中一定要实现该方法

+ `p.terminate()`：强制终止进程p，不会进行任何清理操作，如果p创建了子进程，该子进程就成了僵尸进程，使用该方法需要特别小心这种情况。如果p还保存了一个锁那么也将不会被释放，进而导致死锁

+ `p.is_alive()`：如果p仍然运行，返回True

+ `p.join[timeout])`：主线程等待p终止（强调：是主线程处于等的状态，而p是处于运行的状态）。`timeout`是可选的超时时间，需要强调的是，`p.join`只能`join`住`start`开启的进程，而不能`join`住`run`开启的进程

### 2.11.4. 进程锁

当多个进程操作同一资源时，可能会造成混乱，甚至错误（如写文件），通常采用加锁的方式进行解决

```python
from multiprocessing import Process, Lock
import os
import time

def run(label, lock):
    # 获取锁
    lock.acquire()
    time.sleep(1)
    # 中间的任务，不肯能同时多个进程任务执行
    print(label, os.getpid())
    # 释放锁
    lock.release()

if __name__ == '__main__':
    print('主进程：', os.getpid())
    # 创建进程锁
    lock = Lock()
    # 创建多个子进程
    # 用于存储所有的进程
    recode = []
    for i in range(5):
        p = Process(target=run, args=(f'子进程{i}', lock))
        p.start()
        recode.append(p)
    # 等待进程结束
    for p in recode:
        p.join()
# 运行结果如下：
>>> 主进程： 22224
子进程0 22288
子进程1 22296
子进程2 22312
子进程3 22328
子进程4 22344
```

### 2.11.5. 自定义进程

采用继承`Process`类开启进程的方式

```python
from multiprocessing import Process, Lock
import os
import time

class MyProcess(Process):

    def __init__(self, name, num=1):
        super().__init__()
        self.name = name
        self.num = num
    
    def run(self):
        for i in range(self.num):
            print(f'子进程({i})运行中...')
            time.sleep(1)
        
if __name__ == "__main__":
    p = MyProcess('test1')
    print(f'主进程{p.name}开始启动...')
    p.start()
    p.join()
```

### 2.11.6. 进程池

创建少量的进程可以通过创建`Process`对象完成，如果需要大量的进程和管理时就比较费劲。这时，可以通过进程池加以解决，而且可以通过参数控制进程池中进程的并发数，提高CPU利用率（创建进程池-->添加进程-->关闭进程池-->等待进程池结束-->设置回调）

```python
import multiprocessing
import time, random
import os


def callback(num):
    print(num)

def task(num):
    print(f'Run task {num} ({os.getpid()})...')
    start = time.time()
    time.sleep(random.random() * 3)
    end = time.time()
    print(f'Task {num} runs {(end-start):,.2f} seconds.')
    return num

if __name__ == "__main__":
    # 获取cpu核心数
    print('cpu核数：', multiprocessing.cpu_count())
    print(f'Parent process {os.getpid()}')
    # 创建进程池，一般进程池中的进程数不超过cpu核心数
    pool = multiprocessing.Pool(4)
    # 循环创建进程并添加到进程池中
    for i in range(5):
        # 参数：
        # func：任务函数
        # args：任务函数的参数
        # callback：回调函数，进程结束时调用，参数是进程函数的返回值
        pool.apply_async(func=task, args=(i,), callback=callback)
        
    # 如果换用map_async()可以这样来写
    # pool.map_async(task, [i for i in range(5)])
    print('Waiting for all subporcess done...')
    # 关闭进程池，关闭后就不能添加进程了
    pool.close()
    # 等待进程结束
    pool.join()
    print('All subprocess done.')
# 运行结果如下：
>>> cpu核数： 2
Parent process 22840
Waiting for all subporcess done...
Run task 0 (22888)...
Run task 1 (22880)...
Run task 2 (22904)...
Run task 3 (22920)...
Task 2 runs 0.48 seconds.
Run task 4 (22904)...
2
Task 0 runs 0.80 seconds.
0
Task 3 runs 0.71 seconds.
3
Task 1 runs 1.50 seconds.
1
Task 4 runs 1.86 seconds.
4
All subprocess done.
```

+ `Pool([numprocess[, initializer[, initargs]]])`：创建进程池，`numprocess`为要创建的进程数，默认使用`multiprocessing.cpu_count()`的CPU核心数；`initializer`是每个工作进程启动时要执行的可调用对象，默认为`None`；`initargs`是要传给`initializer`的参数组。

+ `pool.apply(func[, args[, kwargs]])`同步执行(阻塞式)：在**一个池工作进程中**执行`func(*args,**kwargs)`,然后返回结果，**同步运行，阻塞，直到本次任务执行完毕后返回结果**。此操作并不会在所有池工作进程中并执行`func`函数。如果要通过不同参数并发地执行`fun`c函数，必须从不同线程调用`pool.apply()`函数或者使用`pool.apply_async()`。

+ `pool.map(func, iterable[, chunksize=None])`：和`pool.apply()`类似，只不过需要接收一个可迭代的参数对象。

+ `pool.apply_async(func[, args[, kwargs[, callback=None[, error_callback=None]]]])`异步执行(非阻塞)：在**一个池工作进程中**执行`func(*args,**kwargs)`，然后返回结果。此方法的结果是`AsyncResult`类的实例，callback是可调用对象，接收输入参数。当func的结果变为可用时，将理解传给callback。callback禁止执行任何阻塞操作，否则将接收其他异步操作中的结果。

+ `pool.map_async(func, iterable[, chunksize=None[, callback=None[, error_callback=None]]]])`：和`pool.apply_async()`类似，只不过需要接收一个可迭代的参数对象。

### 2.11.7. 数据共享

`Process`之间肯定是需要通信的，操作系统提供了很多机制来实现进程间的通信。`Python`的`multiprocessing`模块包装了底层的机制，提供了`Queue`、`Pipes`等多种方式来交换数据。但要注意的是，**全局变量不能共享**。

```python
import multiprocessing
import time, random
import os


num = 250
lt = ['hello']

def run():
    global num, lt
    print('子进程开始。。。')
    num += 10
    lt.append('world')
    print('子进程结束：', num, lt)

if __name__ == "__main__":
    print('主进程开始》》》', num, lt)
    p = multiprocessing.Process(target=run)
    p.start()
    p.join()
    print('主进程结束：', num, lt)

# 运行结果如下：
>>> 主进程开始》》》 250 ['hello']
子进程开始。。。
子进程结束： 260 ['hello', 'world']
主进程结束： 250 ['hello']
```

+ 管道(Pipe)：创建管道时，得到两个连接；默认`dublex`为`True`，表示全双工，两边都可以收发；若`dublex`为`False`，表示半双工，`p_a`只能收，`p_b`只能发。

    - 全双工通信：
    ```python
    import multiprocessing

    def run(p_a):
        # 子进程接收主进程发的数据
        recv = p_a.recv()
        print('子进程收到：', recv)
        print('子进程发送：', ['a', 'b', 'c', 'd'])
        # 子进程给主进程发数据
        p_a.send(['a', 'b', 'c', 'd'])

    if __name__ == "__main__":
        # 创建管道, 默认为全双工
        p_a, p_b = multiprocessing.Pipe()
        p = multiprocessing.Process(target=run, args=(p_a,))
        p.start()
        print('主进程发送：', [1, 2, 3, 4, 5])
        # 主进程向子进程发数据
        p_b.send([1, 2, 3, 4, 5])
        p.join()
        # 主进程接收子进程的数据
        recv = p_b.recv()
        print('主进程收到：', recv)
        print('主进程结束')

    # 运行结果如下：
    >>> 主进程发送： [1, 2, 3, 4, 5]
    子进程收到： [1, 2, 3, 4, 5]
    子进程发送： ['a', 'b', 'c', 'd']
    主进程收到： ['a', 'b', 'c', 'd']
    主进程结束
    ```
    - 半双工通信：`dublex`为`False`，表示半双工，`p_a`只能收，`p_b`只能发

    ```python
   import multiprocessing

    def run(p_a):
        # 子进程接收主进程发的数据
        recv = p_a.recv()
        print('子进程收到(p_a)：', recv)

    if __name__ == "__main__":
        # 创建管道, 默认为全双工
        p_a, p_b = multiprocessing.Pipe(duplex=False)
        p = multiprocessing.Process(target=run, args=(p_a,))
        p.start()
        print('主进程发送(p_b)：', [1, 2, 3, 4, 5])
        # 主进程向子进程发数据
        p_b.send([1, 2, 3, 4, 5])
        p.join()
        # 主进程接收子进程的数据
        print('主进程结束')
    # 运行结果如下：
    >>> 主进程发送(p_b)： [1, 2, 3, 4, 5]
    子进程收到(p_a)： [1, 2, 3, 4, 5]
    主进程结束
    ```

+ 队列(Queue)

`Queue`本身就是一个消息队列程序，常用的方法有：

- `Queue.qsize()`：返回当前消息队列的消息数量。
- `Queue.empty()`：如果队列为空，返回`True` 否则返回`False`。
- `Queue.full()`：如果队列满了，返回`True`，否则`False`。
- `Queue.get()`：获取队列中的一条消息，然后将其从队列中移除。队列为空时，获取的时候也会阻塞。
- `Queue.put('xxx')`：把内容存放进消息队列, 默认为`True`数据会阻塞，设为`False`时，如果队列已满会报错。
- `Queue.close()`：关闭队列
- `Queue.get_nowait()`相当于`Queue.get(False)`。
- `Queue.put_nowait()`相当于`Queue.put(False)`。

```python
import multiprocessing
import os
import time

def put_data(queue):
    # 拼接数据
    data = str(os.getpid()) + ' ' + str(time.time())
    print('压入数据：', data)
    queue.put(data)

def get_data(queue):
    data = queue.get()
    print('读取数据：', data)

if __name__ == "__main__":
    # 创建队列
    q = multiprocessing.Queue(3)

    # 创建5个进程用于写数据
    record1 = []
    for i in range(5):
        p = multiprocessing.Process(target=put_data, args=(q,))
        p.start()
        record1.append(p)
    
    # 创建5个进程用于读数据
    record2 = []
    for i in range(5):
        p = multiprocessing.Process(target=get_data, args=(q,))
        p.start()
        record2.append(p)

    for p in record1:
        p.join()

    for p in record2:
        p.join()
# 运行结果如下
>>> 压入数据： 6220 1573552927.6151476
压入数据： 5900 1573552927.7400696
压入数据： 19276 1573552927.8130243
压入数据： 17492 1573552927.9059665
压入数据： 16408 1573552927.9929125
读取数据： 6220 1573552927.6151476
读取数据： 5900 1573552927.7400696
读取数据： 19276 1573552927.8130243
读取数据： 17492 1573552927.9059665
读取数据： 16408 1573552927.9929125
```

如果采用进程池创建进程，使用队列进行通讯，可以这样：

```python

def put_data(queue):
    # 拼接数据
    data = str(os.getpid()) + ' ' + str(time.time())
    print('压入数据：', data)
    queue.put(data)

def get_data(queue):
    data = queue.get()
    print('读取数据：', data)

if __name__ == "__main__":
    # 创建队列
    q = multiprocessing.Queue(3)

    # 创建5个进程用于写数据
    pool1 = multiprocessing.Pool(4)
    pool1.map_async(put_data, [i for i in range(5)])
    pool1.close()
    pool1.join()
    # 创建5个进程用于读数据
    pool2 = multiprocessing.Pool(4)
    pool2.map_async(put_data, [i for i in range(5)])
    pool2.close()
    pool2.join()
# 运行结果如下：
>>> 压入数据： 16136 1573552887.7448432
压入数据： 16136 1573552887.7468312
压入数据： 16136 1573552887.74783
压入数据： 16136 1573552887.7488291
压入数据： 16136 1573552887.7718146
压入数据： 17880 1573552888.1625717
压入数据： 17880 1573552888.1655722
压入数据： 17880 1573552888.1665695
压入数据： 17880 1573552888.1795611
压入数据： 19020 1573552888.1855621
```

### 2.11.8. 共享内存

`Python`中提供了强大的`Manager`类，专门用于实现多进程之间的数据共享；`Mangaer`类支持的类型非常多，如：`Value`, `Array`, `List`, `Dict`, `Queue`, `Lock`等；`Manager`提供的数据不安全，需要通过`Lock`作处理。

```python
import multiprocessing
from ctypes import c_char_p

def run(v, s, a, l, d):
    print('子进程：', v.value)
    v.value += 10
    print('子进程：', s.value)
    s.value = b'world'
    print('子进程：', a[0])
    a[0] = 5
    l.append('subprocess')
    d['name'] = 'xiaoming'

if __name__ == "__main__":
    # 共享内存，可以共享不同类型的数据
    server = multiprocessing.Manager()

    # 整数i, 小数f
    v = server.Value('i', 250)
    # 字符串
    s = server.Value(c_char_p, b'hello')
    # 数组，相当于列表
    a = server.Array('i', range(5))
    # 列表
    l = server.list()
    # 字典
    d = server.dict()

    p = multiprocessing.Process(target=run, args=(v, s, a, l, d))

    p.start()
    p.join()
    print('主进程：', v.value)
    print('主进程：', s.value)
    print('主进程：', a[0])
    print('主进程：', l)
    print('主进程：', d)
# 运行结果如下：
>>> 子进程： 250
子进程： b'hello'
子进程： 0
主进程： 260
主进程： b'world'
主进程： 5
主进程： ['subprocess']
主进程： {'name': 'xiaoming'}
```

### 2.11.9. 多进程应用举例

使用多进程实现拷贝文件夹，注意直接使用`copy()`效率比较低

```python
import multiprocessing
import os


def run(src, dst):
    src_fp = open(src, 'r')
    dst_fp = open(dst, 'w')
    content = src_fp.read(1024)
    while content:
        dst_fp.write(content)
        content = src_fp.read(1024)
    src_fp.close()
    dst_fp.close()
    print(src, '拷贝到', dst, '已完成')


def copy(src, dst=None):
    if not dst:
        dst = f'{src}_副本'
    if not os.path.exists(src):
        print('源文件不存在！')
        return None
    if os.path.abspath(src) == os.path.abspath(dst):
        print('源文件与目标文件路径相同，无法进行拷贝！')
        return None
    if not os.path.exists(dst):
        os.makedirs(dst)
    record = []
    src_dirs = os.listdir(src)
    for file in src_dirs:
        src_path = os.path.join(src, file)
        dst_path = os.path.join(dst, file)
        if os.path.isfile(src_path):
            p = multiprocessing.Process(target=run, args=(src_path, dst_path))
            p.start()
            record.append(p)
        else:
            copy(src_path, dst_path)
    return record


if __name__ == "__main__":
    src = 'test'
    dst = ''
    record = copy(src, dst)
    if not record:
        print('拷贝异常...')
    else:
        for p in record:
            p.join()
        print('拷贝结束...')
```

## 2.12. 线程

### 2.12.1. 线程简介

+ 在一个进程中，若想做多个子任务，我们把每个子任务称为线程

+ 线程可以理解为轻量级的进程

+ 进程之间的数据是独立，而一个进程下的线程数据是共享的

+ **线程**是CPU分配时间的最小单位，进程和线程的调度都是操作系统的事

+ 一个进程默认都有一个线程，我们称为主线程

### 2.12.2. 线程模块

`Python`的标准库提供了两个模块：`_thread`和`threading`，`_thread`是**低级模块**，`threading`是**高级模块**，对`_thread`进行了封装。绝大多数情况下，我们只需要使用`threading`这个高级模块。

+ 低级模块(`_thread`)：非常简陋，不建议使用

```python
import _thread
import time

def loop():
    print('子线程开始')
  	print('子线程结束')
    
if __name__ == '__main__':  
    print('主线程开始')
    # 创建线程
    _thread.start_new_thread(loop, ())
    # 主线程结束，子线程立即结束，通过演示测试
    time.sleep(3)
    print('主线程结束')

```

+ 高级模块(`threading`)

```python
import threading
import time

def run(num):
    c = threading.current_thread()
    print('子线程开始：', c.name)
    time.sleep(3)
    print(num)
    print(threading.active_count())
    print('子线程结束：', c.name)

if __name__ == "__main__":
    # 获取主线程
    t = threading.main_thread()
    print('主线程开始：', t.name)
    # 获取当前线程
    c = threading.current_thread()
    print('当前线程：', c.name)
    
    # 创建子线程
    sub = threading.Thread(target=run, args=(250,), name='subthread')

    # 启动子线程
    sub.start()

    # 活跃线程个数
    print(threading.active_count())
    # 线程列表
    print(threading.enumerate())

    time.sleep(1)
    # 判断线程是否活着
    print(sub.is_alive())
    # 等待子线程
    sub.join()
    print(sub.is_alive())
    print('主线程结束：', t.name)
```

- `threading.main_thread()`: 返回主线程对象。可以通过`name`属性获取主线程名称，默认`MainThread`
- `threading.current_thread()`：返回当前线程对象，可以通过`name`属性获取当前线程，默认`Thread-N`
- `threading.active_count()`：返回当前存活的线程个数
- `threading.enumrate()`：以列表形式返回当前所有存活的`Thread`对象
- `threading.Thread(group=None, target=None, name=None, args=(), kwargs={}, *, daemon=None)`：构造线程对象
    - `group`：应该为`None`，为了日后扩展`ThreadGroup`类实现而保留
    - `target`：用于任务函数`run()`调用的可调用对象，默认为`None`，表示不需要调用任何方法
    - `name`：线程名称，默认情况下，由`Thread-N`格式构成一个唯一的名称，其中N是小的十进制数。
    - `args`：用于调用目标函数的参数元组，默认为`()`
    - `kwargs`：是用于调用目标函数的关键字参数字典，默认为`{}`
    - `daemon`：默认为`None`，线程将继承当前线程的守护模式属性；不是`None`，线程将被显式的设置为守护模式，不管该线程是否是守护模式
- `sub.start()`：开始线程活动
- `sub.run()`：代表线程活动的方法。也可以在子类型里重载这个方法，标准的`run()`方法对作为`target`参数传递给该对象构造器的可调用对象（如果存在）发起调用，并附带从`args`和`kwargs`参数分别获取的位置和关键字参数。
- `sub.join(timeount=None)`：等待，直到线程结束。这会阻塞调用这个方法的线程，直到被调用`join()`的线程终结。当`timeout`不为`None`时，因为`join()`总是返回`None`，所以你一定要在`join()`后调用`is_alive()`才能判断是否发生超时。
- `sub.is_active()`：判断线程是否存活着
- `os.exit()`：用于退出当前线程
- `os._exit()`：用于退出当前进程中的主线程

### 2.12.3. 数据共享

全局变量是可以共享的。

```python
import threading
import time

num = 250

def thread_one():
    global num
    num += 10

def thread_two():
    global num
    num -= 10

if __name__ == "__main__":
    print('主线程开始：', num)
    t1 = threading.Thread(target=thread_one)
    t1.start()
    t1.join()
    print('主线程：', num)
    t2 = threading.Thread(target=thread_two)
    t2.start()
    t2.join()
    print('主线程结束：', num)
# 运行结果如下：
>>> 主线程开始： 250
主线程： 260
主线程结束： 250
```

> 线程之间共享进程的所有数据

### 2.12.4. 线程锁

多线程和多进程最大的不同在于，多进程中，同一个变量，各自有一份拷贝存在于每个进程中，互不影响，而多线程中，所有变量都由所有线程共享，所以，任何一个变量都可以被任何一个线程修改，因此，线程之间共享数据最大的危险在于多个线程同时改一个变量，把内容给改乱了。

```python
import threading
import time

# 账户余额
balance = 250

def operate(num):
    global balance
    for i in range(1000000):
        balance += num
        balance -=num

if __name__ == "__main__":
    print('账户初始余额为：', balance)
    while True:
        t1 = threading.Thread(target=operate, args=(10,))
        t2 = threading.Thread(target=operate, args=(10,))
        t1.start()
        t2.start()
        t1.join()
        t2.join()
        if balance != 250:
            break
    print('账户最终余额为：', balance)
# 运行结果如下：
>>> 账户初始余额为： 250
账户最终余额为： 240
```

在上面的例子中，两个线程同时一存一取，最终导致余额不对，所以我们必须要保证一个线程在修改`balance`的时候，其他的线程一定不能改。所以，这时候就需要**线程锁**来做这件事情，当某个线程获取锁之后，除非锁被释放才可以继续执行其他线程，保证同意时刻最多只有一个线程持有该所，这样才不会造成冲突。

+ `threading.Lock()`：创建线程锁

```python
import threading
import time

# 账户余额
balance = 250

def operate(num, lock):
    global balance
    for i in range(1000000):
        # lock.acquire()
        # try:
        #     balance += num
        #     balance -=num
        # finally:
        #     lock.release()
        # 可以直接采用with实现锁的创建和释放
        with lock:
            balance += num
            balance -=num

if __name__ == "__main__":
    print('账户初始余额为：', balance)
    # 创建线程锁对象
    lock = threading.Lock()
    t1 = threading.Thread(target=operate, args=(10, lock))
    t2 = threading.Thread(target=operate, args=(10, lock))
    t1.start()
    t2.start()
    t1.join()
    t2.join()
    print('账户最终余额为：', balance)
# 运行结果
>>> 账户初始余额为： 250
账户最终余额为： 250
```

### 2.12.5. 自定义线程

自定义线程，需要继承自`Thread`类，还需要重写`run()`方法，开启线程时会自动调用`run()`方法

```python
import threading
import time

class MyThread(threading.Thread):

    def __init__(self, time, name):
        super().__init__()
        self.time = time
        self.name = name
    
    def run(self):
        print(f'Sub thread {self.name} start >>>')
        time.sleep(self.time)
        print(f'Sub thread {self.name} end <<<')

if __name__ == "__main__":
    print('Main thread start...')
    record = []
    for i in range(5):
        p = MyThread(2, i)
        p.start()
        record.append(p)
    for p in record:
        p.join()
    print('Main thread end...')

# 运行结果
>>> Main thread start...
Sub thread 0 start >>>
Sub thread 1 start >>>
Sub thread 2 start >>>
Sub thread 3 start >>>
Sub thread 4 start >>>
Sub thread 2 end <<<
Sub thread 3 end <<<
Sub thread 0 end <<<
Sub thread 1 end <<<
Sub thread 4 end <<<
Main thread end...
```

### 2.12.6. 定时线程

在`threading`模块中，有一个`Timer`类，继承自`Thread`类，可以延迟执行线程任务。

+ `threading.Timer(interval, function[, args, kwargs])`：设置一定时间后执行任务，`interval`表示设置的时间(`s`)，`function`表示要执行的任务，`args`与`kwargs`表示传入的参数

+ `timer.start()`：开启定时任务

+ `timer.end()`：取消定时任务

```python
import threading
import time

def run(name):
    print(f'Sub thread {name} start time：{time.ctime()}')
    time.sleep(1)
    print(f'Sub thread {name} end time：{time.ctime()}')

if __name__ == "__main__":
    print('Main thread start...')
    record = []
    for i in range(3):
        sub = threading.Timer(3, run, args=(i,))
        sub.start()
        record.append(sub)
    for sub in record:
        sub.join()
    print(f'Main thread end time：{time.ctime()}')
    print('Main thread end...')
# 运行结果如下：
>>> Main thread start...
Sub thread 0 start time：Tue Nov 19 09:53:58 2019
Sub thread 1 start time：Tue Nov 19 09:53:58 2019
Sub thread 2 start time：Tue Nov 19 09:53:58 2019
Sub thread 0 end time：Tue Nov 19 09:53:59 2019
Sub thread 1 end time：Tue Nov 19 09:53:59 2019
Sub thread 2 end time：Tue Nov 19 09:53:59 2019
Main thread end time：Tue Nov 19 09:53:59 2019
Main thread end...
```

### 2.12.7. 信号传递(`Event`)

在`threading`模块中，有一个`Event`类，可以用来控制线程的执行。

```python
import threading
import time

def run(num):
    for i in range(num):
        # 等待条件成立，会阻塞
        e.wait()
        print(f'第{i+1}步...')
        # 清除条件
        e.clear()

if __name__ == "__main__":
    print('Main thread start...')
    e = threading.Event()
    sub = threading.Thread(target=run, args=(3,))
    sub.start()
    for i in range(3):
        time.sleep(1)
        # 设置后，wait处将不在阻塞
        e.set()
        print('走你', end=' ')
```

### 2.12.8. 多核CPU(Python无法利用多线程实现多核任务)

如果你用于一个多核CPU，你肯定回想，多核应该可以同时执行多个线程，可以写一个死循环，在N核CPU上执行N个死循环线程，结果会发生什么？

```python
import threading, multiprocessing

def loop():
    x = 0
    while True:
        x = x ^ 1

if __name__ == "__main__":
    for i in range(multiprocessing.cpu_count()):
        t = threading.Thread(target=loop)
        t.start()
```

启动上面的程序，双核的CPU上可以监控CPU利用率仅有97%，也就是仅使用了一核。但是用`C`、`C++`或`Java`来改写相同的死循环，直接可以把全部核心跑满，4核就跑到400%，8核就跑到800%，为什么Python不行呢？

> 因为`Python`的线程虽然是真正的线程，但解释器执行时，会存在一个全局解释器锁(`GIL`锁)，任何`Python`线程执行前，必须先获得`GIL`锁，然后每执行100条字节码，解释器就会自动释放`GIL`锁，让别的线程有机会执行，这个`GIL`锁实际上把所有线程的执行代码都给加了锁，所以，多线程在`Python`中只能交替执行，即使100个线程跑在100核CPU上，也只能用到1个核。

> `GIL`是`Python`解释器设计的历史遗留问题，通常我们用的解释器是官方实现的`CPython`，要真正利用多核，除非重写一个不带`GIL`的解释器。

> 所以，在`Python`中，可以使用多线程，但不要指望能有效利用多核。如果一定要通过多线程利用多核，那只能通过`C`扩展来实现，不过这样就失去了`Python`简单易用的特点。

> 不过，也不用过于担心，`Python`虽然不能利用多线程实现多核任务，但可以通过多进程实现多核任务。多个`Python`进程有各自独立的`GIL`锁，互不影响。

### 2.12.9. 进程 vs 线程

+ **进程**
    - 进程是操作系统资源分配的最小单位
    - 进程拥有独立的地址空间，每启动一次进程，系统就会为它分配地址空间
    - 多进程程序更健壮
    - 多进程模式最大的优点就是稳定性高，因为一个子进程崩溃了，不会影响主进程和其他子进程。

    - 多进程模式的缺点是创建进程的代价大，在`Unix/Linux`系统下，用`fork`调用还行，在`Windows`下创建进程开销巨大。另外，操作系统能同时运行的进程数也是有限的，在内存和`CPU`的限制下，如果有几千个进程同时运行，操作系统连调度都会成问题。

+ **线程**
    - 程序执行(调度)的最小单位
    - 线程是共享进程中的数据，使用相同的地址空间，CPU切换一个线程的花费远远小于进程
    - 轻量级的进程，进程之间的数据是独立的，而一个进程下的数据是可以共享的，同一进程下的线程共享全局变量、静态变量等数据，而进程之间的通信需要以通信的方式（IPC)进行。不过如何处理好同步与互斥是编写多线程程序的难点。
    - 线程模式致命的缺点就是任何一个线程挂掉都可能直接造成整个进程崩溃，因为所有线程共享进程的内存。

## 2.13. 异步`IO`

### 2.13.1. 计算密集型与`IO`密集型

+ 计算密集型：要进行大量的计算，消耗CPU资源，比如计算圆周率、对视频进行高清解码等等，全靠CPU的运算能力。这种计算密集型任务虽然也可以用多任务完成，但是任务越多，花在任务切换的时间就越多，CPU执行任务的效率就越低，所以，要最高效地利用CPU，计算密集型任务同时进行的数量应当等于CPU的核心数。计算密集型任务由于主要消耗CPU资源，因此，代码运行效率至关重要。Python这样的脚本语言运行效率很低，完全不适合计算密集型任务。对于计算密集型任务，最好用C语言编写。

+ `IO`密集型：涉及到网络、磁盘`IO`的任务都是`IO`密集型任务，这类任务的特点是CPU消耗很少，任务的大部分时间都在等待`IO`操作完成（因为`IO`的速度远远低于CPU和内存的速度）。对于`IO`密集型任务，任务越多，CPU效率越高，但也有一个限度。常见的大部分任务都是`IO`密集型任务，比如`Web`应用。`IO`密集型任务执行期间，99%的时间都花在`IO`上，花在`CPU`上的时间很少，因此，用运行速度极快的`C`语言替换用`Python`这样运行速度极低的脚本语言，完全无法提升运行效率。对于IO密集型任务，最合适的语言就是开发效率最高（代码量最少）的语言，脚本语言是首选，`C`语言最差。

多线程和多进程的模型虽然解决了并发问题，但是系统不能无上限地增加线程。由于系统切换线程的开销也很大，所以，一旦线程数量过多，CPU的时间就花在线程切换上了，真正运行代码的时间就少了，结果导致性能严重下降。

由于我们要解决的问题是CPU高速执行能力和`IO`设备的龟速严重不匹配，多线程和多进程只是解决这一问题的一种方法。

另一种解决`IO`问题的方法是异步`IO`。当代码需要执行一个耗时的`IO`操作时，它只发出`IO`指令，并不等待`IO`结果，然后就去执行其他代码了。一段时间后，当`IO`返回结果时，再通知CPU进行处理。

### 2.13.2. 协程

协程(Corontine)，又称微线程、纤程。

子程序，或者称为函数，在所有语言中都是层级调用，比如A调用B，B在执行过程中又调用了C，C执行完毕返回，B执行完毕返回，最后是A执行完毕。所以子程序调用是通过栈实现的，一个线程就是执行一个子程序。

子程序调用总是一个入口，一次返回，调用顺序是明确的。而协程的调用和子程序不同。

协程看上去也是子程序，但执行过程中，在子程序内部可中断，然后转而执行别的子程序，在适当的时候再返回来接着执行。

注意，在一个子程序中中断，去执行其他子程序，不是函数调用，有点类似CPU的中断。比如子程序A、B：

```python
def A():
    print('1')
    print('2')
    print('3')

def B():
    print('x')
    print('y')
    print('z')
```

假设由协程执行，在执行A的过程中，可以随时中断，去执行B，B也可能在执行过程中中断再去执行A，结果如下。可以看出，在A中是没有调用B的，所以协程的调用比函数调用理解起来要难一些。

```python
1
2
x
y
3
z
```

+ 看起来A、B的执行有点像多线程，但协程的特点在于是一个线程执行，那和多线程比，协程有何优势？

> **协程执行效率极高**。因为子程序切换不是线程切换，而是由程序自身控制，因此，没有线程切换的开销，和多线程比，线程数量越多，协程的性能优势就越明显。

> **不需要多线程的锁机制**，因为只有一个线程，也不存在同时写变量冲突，在协程中控制共享资源不加锁，只需要判断状态就好了，所以执行效率比多线程高很多。

+ 因为协程是一个线程执行，那怎么利用多核CPU呢？

> 最简单的方法是**多进程+协程**，既充分利用多核，又充分发挥协程的高效率，可获得极高的性能

+ `Python`对协程的支持如何通过`generator`实现的？

> 在`generato`r中，我们不但可以通过`for`循环来迭代，还可以不断调用`next()`函数获取由`yield`语句返回的下一个值。但是`Python`的`yield`不但可以返回一个值，它还可以接收调用者发出的参数。

传统的生产者-消费者模型是一个线程写消息，一个线程取消息，通过锁机制控制队列核等待，但一不小心就可能死锁。如果改用协程，生产者生产消息后，直接通过`yeild`跳转到消费者开始执行，待消费者执行完毕后，切换生产者继续生产，效率极高。

```python
# 消费者
def consumer():
    r = ''
    while True:
        n = yield r  # 此处的yield接收调用者发出的参数n，并把处理后的结果r返回
        if not n:
            return 
        print(f'[CONSUMER] Consumering {n}...')
        r = '200 OK'

# 生产者
def produce(c):
    c.send(None) # 启动生成器consumer
    n = 0
    while n < 5:
        n += 1
        print(f'[PRODUCER] Producing {n}...')
        r = c.send(n)  # 切换至consumer执行
        print(f'[PRODUCER] Consumer return {r}')
    c.close()

c = consumer()
produce(c)
# 运行结果如下：
>>> [PRODUCER] Producing 1...
[CONSUMER] Consumering 1...
[PRODUCER] Consumer return 200 OK
[PRODUCER] Producing 2...
[CONSUMER] Consumering 2...
[PRODUCER] Consumer return 200 OK
[PRODUCER] Producing 3...
[CONSUMER] Consumering 3...
[PRODUCER] Consumer return 200 OK
[PRODUCER] Producing 4...
[CONSUMER] Consumering 4...
[PRODUCER] Consumer return 200 OK
[PRODUCER] Producing 5...
[CONSUMER] Consumering 5...
[PRODUCER] Consumer return 200 OK
```

> 运行分析：注意到`consumer`函数是一个`generator`，把一个`consumer`传入`produce`后：
>> (1)首先调用`c.send(None)`启动生成器；<br/>
>> (2)然后，一旦生产了东西，通过`c.send(n)`切换到`consumer`执行；<br/>
>> (3)`consumer`通过`yield`拿到消息，处理，又通过`yield`把结果传回；<br/>
>> (4)`produce`拿到`consumer`处理的结果，继续生产下一条消息；<br/>
>> (5)`produce`决定不生产了，通过`c.close()`关闭`consumer`，整个过程结束。<br/>

> 整个流程无锁，由一个线程执行，`produce`和`consumer`协作完成任务，所以称为“协程”，而非线程的抢占式多任务。

### 2.13.3. `asyncio`

`asynio`是`Python`3.4版本引入的标准库，直接内置了对异步`IO`的支持。它的编程模型就是一个消息循环。我们从`asyncio`模块中直接获取一个`EventLoop`的引用，然后把需要执行的协程扔到`EventLoop`中执行，就实现了异步`IO`。

+ `asyncio`提供了完善的异步IO支持；

+ 异步操作需要在`coroutine`中通过`yield from`完成；

+ 多个`coroutine`可以封装成一组`Task`然后并发执行。

```python
import asyncio

# @asyncio.coroutine把一个generator标记为coroutine类型，然后，我们就把这个coroutine扔到EventLoop中执行。
@asyncio.coroutine
def hello():
    print('hello world!')
    # 异步调用asynico.sleep(1)，也是一个coroutine, 所以线程不会等待asynico.sleep()，而是直接中断并执行下一个消息循环。当asyncio.sleep()返回时，线程就可以从yield from拿到返回值（此处是None），然后接着执行下一行语句。asyncio.sleep(1)看成是一个耗时1秒的IO操作，在此期间，主线程并未等待，而是去执行EventLoop中其他可以执行的coroutine了，因此可以实现并发执行。
    r = yield from asyncio.sleep(10)
    print('hello world again!')

# 获取EventLoop
loop = asyncio.get_event_loop()
# 执行coroutine
loop.run_until_complete(hello())
loop.close()
>>> hello world!
hello world again!
```

使用`task`封装两个`coroutine`:

```python
import asyncio
import threading

@asyncio.coroutine
def hello():
    print(f'hello world! ({threading.current_thread()})')
    yield from asyncio.sleep(1)
    print(f'hello world agagin! ({threading.current_thread()})')

loop = asyncio.get_event_loop()
tasks = [hello(), hello()]
loop.run_until_complete(asyncio.wait(tasks))
loop.close()
# 运行结果如下：
>>> hello world! (<_MainThread(MainThread, started 4020)>)
hello world! (<_MainThread(MainThread, started 4020)>)
hello world agagin! (<_MainThread(MainThread, started 4020)>)
hello world agagin! (<_MainThread(MainThread, started 4020)>)
# 由打印的当前线程名称可以看出，两个coroutine是由同一个线程并发执行的。
```

案例：用`asyncio`的异步网络连接`sina`、`souhu`和163的网站首页

```python
import asyncio

@asyncio.coroutine
def wget(host):
    print(f'wget {host}...')
    # 创建TCP客户端并连接服务器，或者说创建一个TCP连接对象
    # open_connection接收两个参数：主机和端口号
    # connect是协程，这步仅是创建协程对象，立即返回，不阻塞
    connect = asyncio.open_connection(host, 80)
    # 连接创建成功后，asyncio.open_connection方法的返回值就是读写对象
    # 读写对象分别为StreamReader和StreamWriter实例
    # 它们也是协程对象，底层调用socket模块的send和recv方法实现读写
    reader, writer = yield from connect
    # header 是发送给服务器的消息，意为获取页面的 header 信息
    # 这个格式是固定的，见下图
    header = f'GET / HTTP/1.0\r\nHost: {host}\r\n\r\n'
    # 给服务器发消息，注意消息是二进制的
    writer.write(header.encode('utf-8'))
    # 这是一个与底层IO输入缓冲区交互的流量控制方法
    # 当缓冲区达到上限时，drain()阻塞，待到缓冲区回落到下限时，写操作恢复
    # 当不需要等待时，drain()会立即返回，例如上面的消息内容较少，不会阻塞
    # 这就是一个控制消息的数据量的控制阀
    yield from writer.drain()
    # 给服务器发送消息后，就等着读取服务器返回来的消息
    while True:
        # 读取数据是阻塞操作，释放CPU
        # reader相当于一个水盆，服务器发来的数据是水流
        # readline表示读取一行，以\n作为换行符
        # 如果在出现\n之前，数据流中出现EO（End Of File文件结束符）也会返回
        # 相当于出现\n或EOF时，拧上水龙头，line就是这盆水
        line = yield from reader.readline()
        # 数据接收完毕，会返回空字符串\r\n，退出while循环，结束数据接收
        if line.decode('utf-8') == '\r\n':
            break
        # 接收的数据是二进制数据，转换为 UTF-8 格式并打印
        # rstrip 方法删掉字符串的结尾处的空白字符，也就是 \n
        print(f'{host} header > {line.decode("utf-8").rstrip()}')
    writer.close()   # 关闭数据流，可以省略

loop = asyncio.get_event_loop()
tasks = [wget(host) for host in ['www.sina.com.cn', 'www.sohu.com', 'www.163.com']]
loop.run_until_complete(asyncio.wait(tasks))
loop.close()
# 运行结果如下(3个连接由一个线程通过coroutine并完成)：
>>> wget www.163.com...
wget www.sohu.com...
wget www.sina.com.cn...
www.sohu.com header > HTTP/1.1 200 OK
www.sohu.com header > Content-Type: text/html;charset=UTF-8
www.sohu.com header > Connection: close
www.sohu.com header > Server: nginx
www.sohu.com header > Date: Thu, 14 Nov 2019 03:07:07 GMT
www.sohu.com header > Cache-Control: max-age=60
www.sohu.com header > X-From-Sohu: X-SRC-Cached
www.sohu.com header > Content-Encoding: gzip
www.sohu.com header > FSS-Cache: HIT from 11114832.13605210.19052918
www.sohu.com header > FSS-Proxy: Powered by 9410870.10197312.17348930
www.163.com header > HTTP/1.1 200 OK
www.163.com header > Date: Thu, 14 Nov 2019 03:07:56 GMT
www.163.com header > Content-Type: text/html; charset=GBK
www.163.com header > Connection: close
www.163.com header > Expires: Thu, 14 Nov 2019 03:09:17 GMT
www.163.com header > Server: nginx
www.163.com header > Cache-Control: no-cache,no-store,private
www.163.com header > Vary: Accept-Encoding
www.163.com header > X-Ser: BC51_dx-lt-yd-shandong-jinan-5-cache-6, BC51_dx-lt-yd-shandong-jinan-5-cache-6, BC138_dx-zhejiang-zhou-1-cache-3
www.163.com header > cdn-user-ip: 60.176.229.93
www.163.com header > cdn-ip: 115.231.128.142
www.163.com header > X-Cache-Remote: HIT
www.163.com header > cdn-source: baishan
www.sina.com.cn header > HTTP/1.1 302 Moved Temporarily
www.sina.com.cn header > Server: nginx
www.sina.com.cn header > Date: Thu, 14 Nov 2019 03:07:56 GMT
www.sina.com.cn header > Content-Type: text/html
www.sina.com.cn header > Content-Length: 154
www.sina.com.cn header > Connection: close
www.sina.com.cn header > Location: https://www.sina.com.cn/
www.sina.com.cn header > X-Via-CDN: f=edge,s=ctc.nanjing.ha2ts4.63.nb.sinaedge.com,c=60.176.229.93;
www.sina.com.cn header > X-Via-Edge: 15737008765135de5b03c7c5e66ca1bf1580f
```

### 2.13.4. `async`/`await`

为了简化并更好地标识异步`IO`，从`Python`3.5开始引入新的语法`async`和`await`，可以让`corountine`的代码更简洁易读。与`Python`3.4的`asyncio`和`yield from`的区别：

+ 把`@asyncio.coroutine`替换为`async`

+ 把`yield from`替换为`await`。

```python
import asyncio

async def hello():
    print('hello world!')
    r = await asyncio.sleep(10)
    print('hello world again!')

# 获取EventLoop
loop = asyncio.get_event_loop()
# 执行coroutine
loop.run_until_complete(hello())
loop.close()
>>> hello world!
hello world again!
```

### 2.13.5. `aiohttp`

`aiohttp`可以实现单线程并发`IO`操作。如果仅用在客户端，发货的威力不大。如果把`asyncio`用在服务端，例如`Web`服务器，由于`HTTP`连接就是`IO`操作，因此可以用单线程+`coroutine`实现多用户的高并发。

`asyncio`实现了`TCP`、`UDP`、`SSL`等协议，`aiohttp`则是基于`asyncio`实现的`HTTP`框架。

+ 安装`aiohttp`：`pip install aiohttp`

+ 编写`HTTP`服务器，分别处理以下`URL`:

    - `/`-首页返回`b'<h1>Index</h1>'`；
    - `/hello/{name}`-根据`URL`参数返回文本`hello, %s!`。

+ 用`aiohttp`创建服务

```python
import asyncio

from aiohttp import web

async def index(request):
    await asyncio.sleep(0.5)
    return web.Response(body=b'<h1>Index</h1>', content_type='text/html')

async def hello(request):
    await asyncio.sleep(0.5)
    text = f'<h1>hello, {request.match_info["name"]}</h1>'
    return web.Response(body=text.encode('utf-8'), content_type='text/html')

async def init(loop):
    app = web.Application(loop=loop)
    app.router.add_route('GET', '/', index)
    app.router.add_route('GET', '/hello/{name}', hello)
    runner = web.AppRunner(app)
    srv = await loop.create_server(runner, '127.0.0.1', 9000)
    print('Server started at http://127.0.0.1:9000...')
    return srv
```

## 2.14. 网络编程

### 2.14.1. 相关概念

+ `OSI`七层模型：开放系统互连参考模型，包含物理层、数据链路层、网络层、传输层、会话层、表示层和应用层

![`OSI`七层模型](https://github.com/lajos182/python-essay/blob/master/images/OSI.png)

+ `TCP/IP`：在`OSI`七层模型的基础进行简化抽象出来的广泛使用的网络协议簇

+ `TCP协议`(传输控制协议)：

    - 完成`OSI`模型中的第四层传输层指定的功能
    - 有链接的，数据是安全的(有保障)
    - 传输的速度相对较慢，三次握手、四次挥手、数据检查

+ `UDP`(用户数据报协议)：

    - 无连接的，数据是不可靠的
    - 传输速度相对较快

![网络编程相关概念汇总](https://github.com/lajos182/python-essay/blob/master/images/network%20program.png)

+ `http`请求的结构及详细解释可以查看[程序猿必须要了解的HTTP协议，今天总结了一份关于HTTP请求的结构与具体内容](https://blog.csdn.net/sinat_41898105/article/details/80951072)

+ `http`响应的结构及详细解释可以查看[程序猿必须要了解的HTTP协议，总结了一份关于HTTP响应的结构及详细解释](https://blog.csdn.net/sinat_41898105/article/details/80952338)

### 2.14.2. `TCP`编程

`Socket`是网络编程的一个抽象概念。通常我们用一个`Socket`表示打开了一个网络链接，而打开一个`Socket`需要直到目标计算机的`IP`地址和端口号，再指定协议类型即可。

+ `TCP`是建立可靠连接，并且通信双方都可以以流的形式发送数据。

![`TCP`工作原理](https://github.com/lajos182/python-essay/blob/master/images/tcp.png)

+ 客户端：大多数连接都是可靠的`TCP`连接，创建`TCP`连接时，主动发起连接的叫客户端。

+ 服务端：绑定一个端口并监听来自其他客户端的连接。如果某个客户端连接过来了，服务器就与该客户端建立Socket连接，随后的通信就靠这个Socket连接了。

+ `skt = socket.soket(family=AF_INET, type=SOCK_STREAM, proto=0, fileno=None)`: `family`表示协议簇，`socket.AF_INET`表示`IPv4`，`socket.AF_INET6`表示`IPv6`；`type`表示传输协议，`socket.SOCK_STREAM`表示`TCP`, `socket.SOCK_DGRAM`表示`UDP`

+ `skt.connect(address)`：向服务器发出请求，`address`表示(主机/域名, 端口)的一个元组

+ `skt.send()`：发送请求报文，常见的内容`b'GET / HTTP/1.1\r\nHost: www.baodu.com\r\nConnection: close\r\n\r\n'`

+ `skt.recv()`：接收服务器的数据，字节类型，需要`decode`解码

+ `skt.bind()`：绑定主机和端口，接收一个元组类型的数据

+ `skt.listen()`：服务端监听服务

+ `skt.accept()`：服务端等待阻塞，一旦有客户请求数据，便创建新的套接字进行通讯，同时可以获取客户的请求地址

+ `skt.close()`：关闭套接字

> 使用`tcp`模拟客户端连接百度服务器

```python
# tcp-http模拟(tcp传输层, http应用层)
import socket
# 创建套接字
skt = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
# 与服务器建立连接
skt.connect(('www.baodu.com', 80))
# 向服务器发送消息
skt.send(b'GET / HTTP/1.1\r\nHost: www.baodu.com\r\nConnection: close\r\n\r\n')
# 接收服务器的数据
data = []
while True:
    tmp = skt.recv(1024)
    if tmp:
        data.append(tmp)
    else:
        break
headers, content = b''.join(data).decode('utf-8').split('\r\n\r\n', 1)
print(headers)
# 运行结果
>>> HTTP/1.1 200 OK
Server: nginx
Date: Fri, 15 Nov 2019 06:16:49 GMT
Content-Type: text/html
Content-Length: 16831
Last-Modified: Mon, 27 May 2019 05:10:18 GMT
Connection: close
Vary: Accept-Encoding
ETag: "5ceb713a-41bf"
Accept-Ranges: bytes
```

> 使用tcp创建soket服务

```python
import socket
import threading

def tcplink(client_skt, client_addr):
    print(f'接收到来自{client_addr}新的连接')
    while True:
        recv_data = client_skt.recv(1024)
        print('客户端>>>：', recv_data.decode('utf-8'))
        client_skt.send(recv_data)
    client_skt.close()


if __name__ == "__main__":
    # 创建套接字
    skt = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    # 绑定主机和端口
    skt.bind(('192.168.199.178', 8888))
    # 监听服务
    skt.listen()
    # 阻塞，等待客户端的连接，一旦有连接，会创建新的套接字进行通信
    while True:
        client_skt, client_addr = skt.accept()
        # 创建一个新线程处理连接
        t = threading.Thread(target=tcplink, args=(client_skt, client_addr))
        t.start()
        t.join()
    skt.close()
```

> 使用tcp模拟客户端

```python
import socket

# 创建套接字
skt = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
# 建立连接
skt.connect(('192.168.199.178', 8888))
while True:
    data = input('>>>：')
    skt.send(data.encode('utf-8'))
    # 接收服务器返回的消息
    recv_data = skt.recv(1024)
    print('服务器：', recv_data.decode('utf-8'))
skt.close()
```

### 2.14.3. `UDP`编程

+ `UDP`是面向无连接的协议，使用`UDP`协议时，不需要建立连接，只需要知道对方的`IP`地址和端口号，就可以直接发数据包。

![`UDP`工作原理](https://github.com/lajos182/python-essay/blob/master/images/udp.png)

+ `skt.sendto()`：发送`UDP`数据

+ `skt.bind()`：绑定主机和端口

+ `skt.recvfrom()`：接收`UDP`数据

+ `skt.close()`：关闭`Socket`连接


> 采用`UDP`模拟飞秋发送消息

```python
import socket

# 创建UDP套接字，与TCP基本一样，使用协议: socket.SOCKET_DGRAM
skt = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)

# 版本号:数据包序列号:用户名:主机名:命令:消息内容[:附加数据]
data = '99:12345:lajos:windows:32:您好，欢迎进入飞秋'

for i in range(1, 255):
    ip = '192.168.12.' + str(i)
    addr = (ip, 2425)
    skt.sendto(data.encode('gbk'), addr)

skt.close()
```

> `UDP`协议创建服务端

```python
import socket

# 创建UDP套接字
skt = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
# 绑定IP和端口
skt.bind(('192.168.12.165', 8888))
while True:
    # 阻塞，等待接口客户端的数据
    recv_data, client_addr = skt.recvfrom(1024)
    # 打印客户端发来的数据
    print(client_addr, recv_data.decode('utf-8'))
    # 给客户端发送消息
    skt.sendto(recv_data, client_addr)
skt.close()
```

> `UDP`协议创建客户端

```python
import socket

# 创建UDP套接字
skt = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
while True:
    # 从终端获取输入
    data = input('>>>：')
    # 发送获取的内容
    skt.sendto(data.encode('utf-8'), ('192.168.12.165', 8888))
    # 获取服务端的数据
    recv_data, server_addr = skt.recvfrom(1024)
    print('服务器：', server_addr, recv_data.decode('utf-8'))
# 绑定IP和端口
skt.close()
```

# 3. 第三部分  Python与数据库

+ 数据库简介：

    - 用途：用于存储生活的几乎一切数据
    - 概念：数据库服务器、数据库、数据表、一行数据(一条)、一列数据(字段)
    - 分类：关系型数据库(`MySql`, `Oracle`, `SQL Server`)、非关系型数据库(`Redis`, `MongoDB`)
    - `SQL`：`Structured Query Language`，结构化查询语言
    - `SQL`分类：数据定义语言(`DDL`)、数据操作语言(`DML`)、数据查询语言(`DQL`)、数据控制语言(`DCL`)、数据事务语言(`DTL`)

## 3.1. `MySQL`

### 3.1.1. `MySQL`(`Ubuntu`)的安装

+ 安装：`sudo apt-get install mysql-server`(若出现问题，应该删除自己添加的系统服务)

+ 安全配置：`sudo  mysql_secure_installation`

+ 连接测试：`mysql -h 主机 -u 用户名(默认root) -p`

+ 其他：端口3306；提出`\h`或`help`；所有命令都`;`结尾

### 3.1.2. 数据库定义语言(`DDL`)

![ 数据库定义语言(`DDL`)](https://github.com/lajos182/python-essay/blob/master/images/DDL.png)

+ 数据类型：

    - 整型(`_int`)：
        - `tinyint`：有符号(-128, 127)，无符号(0, 255)，一个字节；
        - `smallint`：有符号(-32768,  32767)，无符号(0, 65535)，两个字节；
        - `mediumint`：3个字节，范围(-8388608~8388607)；
        - `int`：4个字节，范围(-2147483648~2147483647)；
        - `bigint`：8个字节，范围(+-9.22*10的18次方)；
        - 注意：`tinyint`(4)中的4并不表示存储的长度，只有字段指定`zerofill`是有用，如0002
    - 浮点型(`float`, `double`)：
        - `float(m, d)`：单精度浮点数，4个字节，`m`表示总位数，`d`表示小数位数；
        - `double(m, d)`：双精度浮点数，8个字节，`m`表示总位置，`d`表示小数位数
    - 定点数：`decimal(m, d)`：参数`m`<65是总个数，`d`<30且 `d`<`m`是小数位，以字符串的形式存储浮点数，用于金融领域等要求严格的场景
    - 字符串(`char`, `varchar`, `_text`)：
        - `char(n)`：固定长度，最多255个字符；
        - `varchar(n)`：固定长度，最多65535个长度；
        - `tinytext`：可变长度，最多255个字符；
        - `text`：可变长度，最多65535个字符；
        - `mediumtext`：可变长度，最多2的24次方-1个字符；
        - `longtext`：可变长度，最多2的32次方-1个字符
        - 注意：`char(n)`若存入字符数小于`n`，则以空格补于其后，查询之时再将空格去掉。所以char类型存储的字符串末尾不能有空格，`varchar`不限于此；
        - 注意：`char(n)`固定长度，`char(4)`不管是存入几个字符，都将占用4个字节，`varchar`是存入的实际字符数+1个字节（n<=255）或2个字节(n>255)，所以varchar(4),存入3个字符将占用4个字节；
        - 注意：`char`类型的字符串检索速度要比`varchar`类型的快。
    - 二进制数据(`_Blob`)：
        - `_Blob`和`_text`存储方式不同，`_Text`以文本方式存储，英文存储区分大小写，而`_Blob`是以二进制方式存储，不分大小写；
        - `_Blob`存储的数据只能整体读出；
        - `_Text`可以指定字符集，`_Blob`不用指定字符集
    - 日期时间类型(`date`, `time`, `datetime`, `timestamp`)：
        - `date`：日期，以`YYYY-MM-DD`的格式显示，如'2019-11-19'；
        - `time`：时间，以`HH:MM:SS`的格式显示，如'15:44:36'；
        - `datetime`：日期时间，以`YYYY-MM-DD HH:MM:SS`的格式显示，如'2019-11-19 15:44:36'；
        - `timestamp`：以`YYYY-MM-DD`的格式显示，自动存储记录修改时间，数据会随其他字段修改的时候自动刷新

+ 数据类型的属性：

    - `NULL`：数据列可包含`NULL`值；
    - `NOT NULL`：数据列不包含`NULL`值；
    - `DEFAULT`：默认值；
    - `PRIMARY KEY`：主键；
    - `AUTO_INCREMENT`：自动递增，适用于整数类型；
    - `UNSIGNED`：无符号；
    - `CHARACTER SET name`：指定字符集

+ 数据库引擎：常见的MySQL数据库引擎有`InnoDB`，`MyIsam`，`Memory`，`Mrg_Myisam`，`Blackhole`等。

    - `InnoDB`：事务型存储引擎，提供了对数据库`ACID`事务的支持，并实现了`SQL`标准的四种������级别，具有行级锁定及外键支持，该引擎的设计目标便是处理大容量数据的数据库系统，`MySQL`在运行时`InnoDB`会在内存中建立缓冲池，用于缓存数据及索引；
    - `MyIsam`：MySQL主流引擎之一，不支持事务操作，不支持行锁及外键，效率较低；
    - `Memory(Heap)`：`MEMORY`类型的表访问非常得快，因为它的数据是放在内存中的，并且默认使用`HASH`索引，但是一旦服务关闭，表中的数据就会丢失掉；`HEAP`允许只驻留在内存里的临时表格。驻留在内存里让`HEAP`要比`ISAM`和`MYISAM`都快，但是它所管理的数据是不稳定的，而且如果在关机之前没有进行保存，那么所有的数据都会丢失;
    - `Mrg_MyIsam`：一个相同的可以被当作一个来用的MyISAM表的集合，它将`MyIsam`引擎的多个表聚合起来，但是它的内部没有数据，真正的数据依然是`MyIsam`引擎的表中，但是可以直接进行查询、删除更新等操作；
    - `Blackhole`：任何写入到此引擎的数据均会被丢弃掉，不做实际存储；`Select`语句的内容永远是空，它会丢弃所有的插入的数据，服务器会记录下`Blackhole`表的日志，所以可以用于复制数据到备份数据库。

+ 数据库索引：用于快速找出在某个列中有一特定值的行

    - 普通索引(`index()`)：`MySQL`中基本索引类型，没有什么限制，允许在定义索引的列中插入重复值和空值，纯粹为了查询数据更快一点；
    - 唯一索引(`unique()`)：索引列中的值必须是唯一的，但是允许为空值；
    - 主键索引(`primary key()`)：是一种特殊的唯一索引，不允许有空值；
    - 组合索引：在表中的多个字段组合上创建的索引，只有在查询条件中使用了这些字段的左边字段时，索引才会被使用，使用组合索引时遵循最左前缀集合；
    - 全文索引：只有在`MyISAM`引擎上才能使用，只能在`CHAR`, `VARCHAR`, `TEXT`类型字段上使用全文索引；
    - 空间索引：对空间数据类型的字段建立的索引，`MySQL`中的空间数据类型有四种，`GEOMETRY`、`POINT`、`LINESTRING`、`POLYGON`。在创建空间索引时，使用`SPATIAL`关键字。要求，引擎为`MyISAM`，创建空间索引的列，必须将其声明为`NOT NULL`。

很多选项都可以在创建表时指定，如：

```sql
create table user(
    id int auto_increment,
    name varchar(20),
    primary key(id),
    unique(name)
)engine=innodb default charset=utf8;
```

添加索引：

```sql
alter table user add index(em);				# 给em字段添加普通索引
alter table user add unique(username);		# 给username字段添加唯一索引
alter table user add primary key(id);		# 将id设置为主键索引
alter table user drop index em;				# 删除em字段的普通索引
```

### 3.1.3. 数据库操作语言(`DML`)

![数据库操作语言(`DML`)](https://github.com/lajos182/python-essay/blob/master/images/DML.png)

+ 创建一张`star`表：

```sql
create table star(
    id int auto_increment,
    name varchar(20) not null,
    money float not null,
    province varchar(20) default null,
    age tinyint unsigned not null,
    sex tinyint not null,
    primary key(id)
)engine=innodb default charset=utf8;
```

+ 插入数据：

    - 方式1：不指定字段，按照数据表的数据添加一条数据的全部字段

    ```sql
    insert into star values(1,'黄晓明',200000,'山东',28,0);
    ```

    > 可以同时插入多条数据，每条一个小括号
    - 方式2：指定字段，只需要传递指定字段的值

    ```sql
    insert into star(name,money,age,sex,province) values('小岳岳',4000000, 33, 0, '河南')；
    ```

    > 可以同时插入多条数据，每条一个小括号

+ 查询数据：

```sql
select * from star;
```

+ 删除数据：删除操作一定不要忘了指定条件，否则后果自负。

```sql
delete from star where id = 1;
```

+ 修改数据：修改操作一定不要忘了指定条件，否则后果自负。

```sql
update star set age=22, money=8000000 where id=6;
```

### 3.1.4. 数据库查询语言(`DQL`)

![数据库查询语言(`DQL`)](https://github.com/lajos182/python-essay/blob/master/images/DQL.png)

+ 基础查询：`select * from star;`

+ 指定字段查询：`select id,name,money from star;`

+ 排除重复记录：`select distinct name from star;`(使用`distinct`修饰的字段组合不能重复)

+ 指定条件查询：

```sql
select id,name,money from star where id > 4;
select id,name from star where id between 2 and 5;
select id,name from star where id in(2,4,6);
select id,name from star where name like '小%';
```

+ 结果集排序：`select id,name,money from star order by money desc;` 

    - `order by`：指定排序字段，`asc`表示升序，默认的，`desc`表示降序
    - 也可以多字段排序，先按照前面的字段排序，再按照后面字段排序。`select id,name,money,age from star order by money desc,age asc;`

+ 限制结果集：

```sql
select id,name,money from star limit 3;					# 取3条数据
select id,name,money from star limit 2,3;				# 偏移2条，然后取3条数据
select id,name,money from star limit 3 offset 2;		# 偏移2条，然后取3条数据
```

+ 常用的集合函数

| 函数    | 功能   |
| ----- | ---- |
| count | 统计个数 |
| sum   | 求和   |
| max   | 最大值  |
| min   | 最小值  |
| avg   | 平均值  |
> 1. 使用count时指定任何字段都行
> 2. 使用其他函数时必须要指定字段

```sql
select count(*) from star;
select max(money) as m from star;
```
> `as`可以给字段其别名

+ 分组操作

```sql
select * from star group by sex;					# 分组
select count(*), sex from star group by sex;		# 分组统计
```
+ 结果集过滤：

```sql
select count(*) as c,province from star group by province having c>1;
```
> 搜索所有记录，然后按照省份分组，统计成员大于1的省份

### 3.1.5. 数据控制语言(`DCL`)

![ 数据控制语言(`DCL`)](https://github.com/lajos182/python-essay/blob/master/images/DCL.png)

### 3.1.6. 多表联合查询

+ 隐式内连接：没有出现`join`关键的连接, `select 字段 from 表1, 表2 where 关联条件;`

```sql
select username, name from user, goods where user.gid = goods.gid;
```
> 查看用户买的商品名

+ 显示内连接：会出现`join`关键字，后面的条件使用`on`，`select 字段 from 表1 [inner/cross] join 表2 on user.gid = goods.gid;`

```sql
select username, name from user [inner/cross] join goods on user.gid = goods.gid;
```
> 功能同上

+ 外左连接：以左表为主，`select 字段 from 表1 left [outer] join 表2 on 关联条件;`

```sql
select username, name from user left [outer] join goods on user.gid = goods.gid;
```
> 以左表为主，显示左边所有内容，右表不匹配的选项显示`NULL`

+ 外右连接：以右表为主，`select 字段 from 表1 right [outer] join 表2 on 关联条件;`

```sql
select username, name from user right [outer] join goods on user.gid = goods.gid;
```
> 以右表为主，显示右边所有内容，左表不匹配的选项显示`NULL`

### 3.1.7. 多表联合操作

+ 子(嵌套)查询操作

  - 说明：一条`sql`语句的查询结果作为另一条`sql`语句的条件
  - 示例：`select * from user where gid in (select gid from goods);`

+ 联合更新(同时更新多个表的数据)

  - 示例：`update user u, good g set u.gid=0, g.price=8000 where u.gid = g.gid and u.id=1`

### 3.1.8. 事务处理语言(`DTL`)

+ 事务：`MySQL`使用`INNODB`数据库引擎，用来维持数据库的完整性，常用来管理`insert`、`delete`、`update`

+ 开启事务：禁止自动提交，`set autocommit=0;`

+ 操作回滚：出现异常时使用，`rollback;`

+ 提交操作：没有异常，`commit;`

### 3.1.9. 外键索引(约束)

+ 所谓**外键**就是一个表的主键作为了另一个表的关联字段，然后在添加一点设置就成为了外键，可以简化多个关联表之间的操作，如：删除一个另一个跟着删除

示例：一个表示用户组的表`t_group`，一个用户表`t_user`

```sql
create table t_group(
    id int,
    name varchar(20),
    primary key(id)
);
create table t_user(
    id int,
    name varchar(20),
    groupid int,
    primary key(id),
    foreign key(groupid) references t_group(id) on delete restrict on update restrict
);
```
+ 约束行为：

    - `NO ACTION`或`RESTRICT`：删除或修改时不做任何操作，直接报错
    - `SET NULL`：删除或更新时，都设置为`null`
    - `CASCADE`：删除或更新时，同时删除或更新从表的数据

### 3.1.10. 数据清空(`DELETE`与`TRUNCATE`)

+ `delete from 表名;`：再次插入数据时，自增字段的值接着清空前的数据增加

+ `truncate table 表名;`：删除数据，同时将`AUTO_INCREMENT`的初始值设为1

### 3.1.11. 数据库的备份与恢复

+ 备份：`mysqldump -uroot -p test > test.sql`

+ 恢复：`mysql -uroot -p test < test.sql`

### 3.1.12. `Python`操作`MySql`

`Python`操作`MySQL`有5中方式，`MySQLdb`、`mysqlclient`、`PyMySQL`、`peewee`、`SQLAlchemy`，在`Python`的`Web`框架`Flask`和`Django`中都采用`orm`进行封。

#### 3.1.12.1. `MySQLdb`

`MySQLdb`又叫`MySQL-python`，是`Python`连接`MySQL`最流行的一个驱动，很多框架都也是基于此库进行开发，遗憾的是它只支持`Python2.x`，而且安装的时候有很多前置条件，因为它是基于`C`开发的库，在`Windows`平台安装非常不友好，经常出现失败的情况，现在基本不推荐使用，取代的是它的衍生版本。

```shell
#  前置条件
sudo apt-get install python-dev libmysqlclient-dev  # Ubuntu
sudo yum install python-devel mysql-devel  # Red Hat / CentOS
# 安装
pip install Mysql-python
# Windwos直接通过exe文件安装
```
```python
import Mysqldb

db = Mysqldb.connect(
    host='localhost',  # 主机名
    user='root',  # 用户名
    passwd='pythontab.com',  # 密码
    db='testdb'  # 数据库名称
)
# 获取游标
cur = db.cursor()
# 执行的都是原生的SQL语句
cur.execute('select * from mytable;')
for row in cur.fetchall():
    print(row[0])
db.close()
```

#### 3.1.12.2. `mysqlclient`

由于`MySQL-python(MySQLdb)`年久失修，后来出现了它的`Fork`版本`mysqlclient`，完全兼容`MySQLdb`，同时支持`Python3.x`，是`Django ORM`的依赖工具，如果你想使用原生`SQL`来操作数据库，那么推荐此驱动。安装方式和`MySQLdb`是一样的，`Windows`可以在`https://www.lfd.uci.edu/~gohlke/pythonlibs/#mysqlclient`网站找到对应版本的`whl`包下载安装。

+ 安装方式：`pip install mysqlclient`, 如果安装出现问题，需要安装`Python3.x-dev`、`libmysqlclient-dev`

#### 3.1.12.3. `PyMySQL`

`PyMySQL`是纯`Python`实现的驱动，速度上比不上`MySQLdb`和`mysqlclient`，最大的特点可能就是它的安装方式没那么繁琐，同时也兼容`MySQL-python`

+ 安装方式：`pip install PyMySQL`，为了兼容`mysqldb`，只需要加入`pymysql.install_as_MySQLdb()`

```python
import pymysql

conn = pymysql.connect(host='127.0.0.1', user='root', passwd="pythontab.com", db='testdb')
cur = conn.cursor()
cur.execute("SELECT Host,User FROM user")
for r in cur:
    print(r)
cur.close()
conn.close()
```
#### 3.1.12.4. `peewee`

写原生`SQL`的过程非常繁琐，代码重复，没有面向对象思维，继而诞生了很多封装`wrapper`包和`ORM`框架，`ORM`是`Python`对象与数据库关系表的一种映射关系，有了 `ORM`你不再需要写`SQL`语句。提高了写代码的速度，同时兼容多种数据库系统，如`sqlite`, `mysql`、`postgresql`，付出的代价可能就是性能上的一些损失。如果你对 `Django`自带的`ORM`熟悉的话，那么`peewee`的学习成本几乎为零。它是`Python`中是最流行的 ORM 框架。

+ 安装：`pip install peewee`

    - `MySQL`数据库连接：`db = MySQLDatabase(database='test', host='localhost', port=3306, user='root', passwd='jiang')`
    - `Sqlite`数据库连接：`db = SqliteDatabase(database=dbpath)`, `dbpath = os.path.join(os.path.dirname(os.path.abspath(__file__)), 'test.db'`
    - 创建数据表：`模型类名.create_table()`
    - 插入数据：
        - 一般的`create`插入数据：类名.create(username='lajos')
        - 事务插入:
        ```python
        data = [
            {
                "username": "lajos",
                "age": 14
            },
            ...
        ]
        with db.atomic():
            for i in data:
                User.create(**i)
        ```
        - `insert_many()`插入多条数据：
         ```python
        data = [
            {
                "username": "lajos",
                "age": 14
            },
            ...
        ]
        with db.atomic():
            for i in range(0, len(data), 100)
                User.insert_many(data[i: i+100]).excute()
        ```
    - 查询数据：可以使用`get()`和`filter()`，也可以使用`select()`

```python
import datetime
from peewee import *

db = MySQLDatabase(database='test', host='localhost', port=3306, user='root', passwd='jiang')
db.connect()

class BaseModel(Model):

    class Meta:
        database = db

class User(BaseModel):
    username = CharField(unique=True)

class Tweet(BaseModel):
    user = ForeignKeyField(User, related_name='tweets')
    message = TextField()
    created_date = DateTimeField(default=datetime.datetime.now())
    is_published = BooleanField(default=True)

def create_table(table):
    # 如果不存在表就创建
    if not table.table_exists():
        table.create_table()

def drop_table(table):
    if table.table_exists():
        table.drop_table()


if __name__ == '__main__':
    # 创建表
    create_table(User)
    create_table(Tweet)
    # 插入数据
    data = [{
        'user_id': 1,
        'message': 'hello world'
    }]
    user = User.create(username='lajos')
    Tweet.create(user=user, message='lajos is a handsome man')
    with db.atomic():
        for i in data:
            Tweet.create(**i)
    # 插入大量数据时可以采用，速度快
    with db.atomic():
        for i in range(0, len(data), 100):
            Tweet.insert_many(data[i: i+100]).execute()
    # 查询数据
    user = User.get(username='lajos')
    User.filter()
```
#### 3.1.12.5. `SQLAlchemy`

如果想找一种既支持原生`SQL`，又支持`ORM`的工具，那么`SQLAlchemy`是最好的选择，它非常接近`Java`中的`Hibernate`框架。安装使用`pip install sqlalchemy`

+ 原生`SQL`使用：

```python

import time
import threading
import sqlalchemy
from sqlalchemy import create_engine
from sqlalchemy.engine.base import Engine

conn_pool=create_engine( #创建sqlalchemy引擎
     "mysql+pymysql://webproject:web@192.168.1.18:3306/web?charset=utf8",  #数据库类型+数据库驱动://用户名:密码@主机:端口/数据库
     max_overflow=2, #超过连接池大小之后，允许最大扩展连接数，如果不指定默认为5；
     pool_size=5,   #连接池大小
     pool_timeout=30,#连接池如果没有连接了，最长等待时间
     pool_recycle=-1,#多久之后对连接池中连接进行一次回收

)



#多线程操作线程池
def task(arg):
    conn = conn_pool.raw_connection()
    cursor = conn.cursor()
    cursor.execute(
        #"select * from cmdb_worker_order"
        "select sleep(2)"
    )
    result = cursor.fetchall()
    cursor.close()
    conn.close()

if __name__ == '__main__'：
    for i in range(20):
        t = threading.Thread(target=task, args=(i,)) #5个线程 执行2秒 然后5个线程在去执行2秒
        t.start()
```
+ `ORM`使用

使用`ORM`方式创建数据表

```python
import datetime
from sqlalchemy import create_engine
from sqlalchemy.ext.declarative import declarative_base
from sqlalchemy import Column, Integer, String, Text, ForeignKey, DateTime, UniqueConstraint, Index
from sqlalchemy.orm import relationship

Base = declarative_base()

class Users(Base):
    __tablename__ = 'users'                #表名称
    id = Column(Integer, primary_key=True) # primary_key=True设置主键
    name = Column(String(32), index=True, nullable=False) #index=True创建索引， nullable=False不为空。
    age = Column(Integer, default=18)        #数字字段
    email = Column(String(32), unique=True)  #设置唯一索引
    ctime = Column(DateTime, default=datetime.datetime.now) #设置默认值为当前时间（注意千万不要datetime.datetime.now()）
    extra = Column(Text, nullable=True)         #文本内容字段
    __table_args__ = (
        # UniqueConstraint('id', 'name', name='uix_id_name'), #设置联合唯一索引
        # Index('ix_id_name', 'name', 'extra'),                #设置联合索引
    )

class Hosts(Base):
    __tablename__ = 'hosts'

    id = Column(Integer, primary_key=True)
    name = Column(String(32), index=True)
    ctime = Column(DateTime, default=datetime.datetime.now)

# ##################### 一对多示例 #########################
class Hobby(Base):
    __tablename__ = 'hobby'
    id = Column(Integer, primary_key=True)
    caption = Column(String(50), default='篮球')

class Person(Base):
    __tablename__ = 'person'
    nid = Column(Integer, primary_key=True)
    name = Column(String(32), index=True, nullable=True)
    hobby_id = Column(Integer, ForeignKey("hobby.id"))
    # 与生成表结构无关，仅用于查询方便
    hobby = relationship("Hobby", backref='pers')

# ##################### 多对多示例 #########################

class Server2Group(Base):
    __tablename__ = 'server2group'
    id = Column(Integer, primary_key=True, autoincrement=True)
    server_id = Column(Integer, ForeignKey('server.id'))
    group_id = Column(Integer, ForeignKey('group.id'))

class Group(Base):
    __tablename__ = 'group'
    id = Column(Integer, primary_key=True)
    name = Column(String(64), unique=True, nullable=False)
    # 与生成表结构无关，仅用于查询方便
    servers = relationship('Server', secondary='server2group', backref='groups')

class Server(Base):
    __tablename__ = 'server'
    id = Column(Integer, primary_key=True, autoincrement=True)
    hostname = Column(String(64), unique=True, nullable=False)

def init_db():
    """
    根据类创建数据库表
    :return:
    """
    engine = create_engine(
        "mysql+pymysql://webproject:web@192.168.1.18:3306/web?charset=utf8",
        max_overflow=0,  # 超过连接池大小外最多创建的连接
        pool_size=5,  # 连接池大小
        pool_timeout=30,  # 池中没有线程最多等待的时间，否则报错
        pool_recycle=-1  # 多久之后对线程池中的线程进行一次连接的回收（重置）
    )

    Base.metadata.create_all(engine)


def drop_db(): #根据类 删除数据库表
    engine = create_engine(
        "mysql+pymysql://webproject:web@192.168.1.18:3306/web?charset=utf8",
        max_overflow=0,   # 超过连接池大小外最多创建的连接
        pool_size=5,      # 连接池大小
        pool_timeout=30,  # 池中没有线程最多等待的时间，否则报错
        pool_recycle=-1   # 多久之后对线程池中的线程进行一次连接的回收（重置）
    )

    Base.metadata.drop_all(engine) #这行代码很关键哦！！ 读取继承了Base类的所有表在数据库中进行删除表

if __name__ == '__main__':
    init_db()                      #执行创建
```

使用`ORM`方式操作数据库

```python
from SqlALchemy.models import Users
from sqlalchemy.orm import sessionmaker
from sqlalchemy import create_engine

engine = create_engine( "mysql+pymysql://webproject:web@192.168.1.18:3306/web?charset=utf8")
Session = sessionmaker(bind=engine)

# 每次执行数据库操作时，都需要创建一个会话
session = Session()

# ############# 执行ORM操作 #############

# 增加一条数据
obj1 = Users(username="张根"， age=18, email="1320168@qq.com", extra="handsome") #创建Users对象=1行数据
session.add(obj1)          #添加到表中

# 批量添加多条
session.add_all([
    Users(name="lajos", age=21, email="lajos@163.com", extra="merchant"),
    Users(name="刘峻轩", age=20, email="ljunxuan@163.com", extra="scientist")
])

# 删除操作
session.query(Users).filter(users.id==5).delete()

# 修改操作
session.query(Users).filter(Users.id==4).update({'name':'Martin'})
session.query(Users).filter(Users.id==4).update({Users.name: Users.name + "666"}, synchronize_session=False)#在原来的基础上做字符串
session.query(Users).filter(Users.id==18).update({Users.id: Users.id - 12},synchronize_session="evaluate")#在原来的基础上做数字+,-操作

# 查询
r0=session.query(Users).all()                             #查询user表中全部数据；
r1=session.query(Users).filter(Users.id > 2)              #查询user表中，id>2的记录；
r2=session.query(Users.age).all()                         #查询User表中的 age列； ##[(18,), (19,)]
r3=session.query(Users.age.label('cname')).all()          #使用别名查询

r4=session.query(Users).filter(Users.name=='Martin').all()      #查询姓名==Martin的用户
r5=session.query(Users).filter_by(name='Martin',age=19).all()   #filter_by方式查询
r6=session.query(Users).filter_by(name='Martin',age=19).first() #获取第 单个对象 print(r6.name)
r7=session.query(Users).filter(text("id<:value and name=:name")).params(value=18, name='Martin').order_by(Users.id).all() #查询 id>18 name=Martin的Users 根据 id排序，params支持传参数；
r8 = session.query(Users).from_statement(text("SELECT * FROM users where name=:name")).params(name='ed').all()#from_statement,申请使用原生sql

#条件查询
ret0 = session.query(Users).filter(Users.id.between(0,7), Users.name == 'Martin').all()  #between: 查询 user id在0--7之间，用户名为Martin 的数据;
ret1= session.query(Users).filter(Users.id.in_([1,6])).all()  #查询user_id in [1,6] 的数据
ret2 = session.query(Users).filter(~Users.id.in_([1,3,4])).all()  #查询user_id  not in [1,6] 的数据
ret = session.query(Users).filter(Users.id.in_(session.query(Users.id).filter_by(name='Martin'))).all()
#1.session.query(Users.id).filter_by(name='Martin') 查询name=Martin'的id
#2.在user表中 按1的结果 查询


# 多查询条件 逻辑运算、嵌套查询
from sqlalchemy import and_, or_
ret0 = session.query(Users).filter(and_(Users.id > 3, Users.name == 'eric')).all()
ret1 = session.query(Users).filter(or_(Users.id < 2, Users.name == 'eric')).all()
ret2 = session.query(Users).filter(
    or_(
        Users.id < 2,
        and_(Users.name == 'eric', Users.id > 3),
        Users.extra != ""
    )).all()

# 字符串、模糊匹配查询
ret0 = session.query(Users).filter(Users.name.like('M%')).first().name
ret1 = session.query(Users).filter(~Users.name.like('%r%')).first().name
print(ret0,ret1)

# 限制分页
ret = session.query(Users)[0:2]
print(ret)

# 排序
ret0 = session.query(Users).order_by(Users.id.desc()).all()                   #根据id,由大到小排序(desc).
ret1 = session.query(Users).order_by(Users.id.asc(),Users.age.desc()).all()   #根据id,由小到大排序(asc)，如id相等,由大到小排序(desc).
print([i.id for i in ret0])
print([i.id for i in ret1])

# group_by分组查询和having二次筛选
from sqlalchemy.sql import func

ret0 = session.query(Users).group_by(Users.age).all() #根据name字段进行分组

ret1 = session.query(     #使用name字段进行分组，求每组中 最大id 、最小id 、id 之和
    func.max(Users.id),
    func.sum(Users.id),
    func.min(Users.id)
).group_by(Users.name).all()


ret2 = session.query(
    func.max(Users.id),
    func.sum(Users.id),                          #对分组之后的数据进行 having筛选，
    func.min(Users.id)
).group_by(Users.name).having(func.min(Users.id) >2).all()
'''
having的作用：
例如：查询公司中 部门人数大于3人的部门，先按照部门分组，然后求人数，然后再having 大于3的；

'''

# 连表查询
ret = session.query(models.Users).join(models.Hobby, models.Users.id == models.Hobby.id,isouter=True).filter(models.Users.id >1)
#2个没有外键关系的表 做连表查询
print(ret)

ret = session.query(models.Person).join(models.Hobby).all()              #inin_join
print(ret)
ret = session.query(models.Person).join(models.Hobby,isouter=True).all() #left_join 调换位置 更换为 right_join
print(ret)

''''
left join：以左表为准，显示符合搜索条件的记录；

aID　　　　　aNum　　　　　bID　　　　　bName
　　　　  a20050115　　　 NULL　　　　　NULL


right join：以右表为准，显示符合搜索条件的记录；

aID　　　　　aNum　　　　　bID　　　　　bName
NULL　　　　 NULL　　　　　 8　　　　2006032408


inin_join：并不以谁为基础,它只显示符合条件
aID　　　　　aNum　　　　　bID　　　　　bName


'''

# 连表方式1：指定字段获取
persons=session.query(models.Person.name,models.Hobby.caption.label('hobby_caption')).join(models.Hobby)
for row in  persons:
    print(row.name,row.hobby_caption,)

# 连表方式2：获取所有字段
persons = session.query(models.Person, models.Hobby).join(models.Hobby)
for row in persons:
    #print(row)=2个对象
    print(row[0].name,row[1].caption)

# 连表方式3：relationship 连表查询
persons = session.query(models.Person).all()
for row in persons:
    print(row.name,row.hobby.caption)

'''
 hobby = relationship("Hobby", backref='pers')
 Hobby：正向查询
 backref：反向查询

ps:查询喜欢姑娘的所有人
hobby_obj=session.query(models.Hobby).filter(models.Hobby.id==2).first()
print(hobby_obj.pers)
'''

################################relationship增加######################
# 1.relationship正向增加
person_obj=models.Person(name='Tony',hobby=models.Hobby(caption='any'))


# 2.relationship 反向增加
hobby_obj=models.Hobby(caption='人妖')
hobby_obj.pers=[
        models.Person(name='李渊'),
        models.Person(name='西门庆'),
    ]
session.add(person_obj,hobby_obj)

基于relationship 做1对多操作


#############################多对多添加#################################

#添加方式1：同时添加男、女对象，直接添加相亲表；前提是 知道新添加男、女对象的ID；
session.add_all([
    models.Boy(name='张无忌'),
    models.Boy(name='宋青书'),
    models.Girl(name='周芷若'),
    models.Girl(name='赵敏'),
])
session.commit()

s2g =models.G2B(girl_id=1,boy_id=1)
session.add(s2g)
session.commit()

#添加方式2：通过女生对象 添加 相亲记录表
girl_obj = models.Girl(name='灭绝师太')                                     #创建1位女性朋友 灭绝
girl_obj.boys = [models.Boy(name='张三丰'),models.Boy(name='方正大师')]    #然后灭绝和 张三丰、方正大师分别相了1次亲
session.add(girl_obj)
session.commit()

##添加方式3：通过男生对象 添加 相亲记录
boy_obj = session.query(models.Boy).filter(models.Boy.name=='尹志平').first()  #创建1位男性朋友 尹志平
boy_obj.girls = [models.Girl(name='小龙女'),models.Girl(name='黄蓉')]         #然后尹志平 和小龙女、黄蓉分别 相了一次亲
session.add(boy_obj)
session.commit()

##################################多对多查询###################################

#boys = relationship('Boy', secondary='g2b', backref='girls')
#1.基于 relationship 正向查询
mie_jue = session.query(models.Girl).filter(models.Girl.name=='灭绝师太').first()
print( [i.name for i in mie_jue.boys]) #['方正大师', '张三丰']

#2.基于 relationship 反向查询
yi_zhi_ping = session.query(models.Boy).filter(models.Boy.name=='尹志平').first()
print( [i.name for i in yi_zhi_ping.girls]) #['小龙女', '黄蓉']


# 提交事务，上面的每次操作都要执行
session.commit()
# 关闭session
session.close()
```
> `filter`与`filter_by`的区别：
> `filter`传入的参数要用这样的格式：类名.列明，判断要用`==`表示，`session.query(Users).filter(Users.name =='Martin').filter(Users.age == 19).all()`;
> `filter_by`使用的语法和`Python`更接近，`session.query(Users).filter(name='Martin', age=19).all()`

#### 3.1.12.6. `Flask-SQLAlchemy`

+ `SQLAlchemy`是一个关系型数据库框架，它提供了高层的`ORM`和底层的原生数据库的操作，让开发者不用直接和`SQL`语句打交道，而是通过`Python`对象来操作数据库，在舍弃一些性能开销的同时，换来的是开发效率的较大提升。一句话：就是对数据库的抽象！

+ `Flask-SQLAlchemy`是一个简化了`SQLAlchemy`操作的`flask`扩展，是`SQLAlchemy`的具体实现，封装了对数据库的基本操作。举例：如果说动物园是`SQLAlchemy`，那`Flask-SQLAlchemy`只是其中的一只。

## 3.2. `Redis`

`Redis`是一个开源的使用`ANSI C语言`编写、支持网络、可基于内存亦可持久化的日志型、`Key-Value`数据库。它是一种**非关系型数据库**，经常用过缓存，拥有丰富的数据类型：字符串、哈希、列表、集合和有序集合。

### 3.2.1. `Redis`的安装与连接测试

+ 直接安装：`sudo apt-get install redis-server`，该安装只是`Linux`的稳定版本，如果想安装`Redis`官方稳定版本需要采用源码安装

+ 源码安装：
    - 官网`redis.io`下载稳定的最新版本，比如`redis-5.0.7.tar.gz`
    - 安装`tcl`：`sudo apt-get install tcl`
    - 解压下载的安装包，将解压后的文件放至指定的安装目录，`sudo mv redis-5.0.7 /usr/local/redis  cd /usr/local/redis`
    - 编译安装：`sudo make`——>`sudo make test`——>`sudo make install`
    - 测试：`/usr/local/redis/src/redis-server`——>`/usr/local/redis/src/redis-cli`——>`set name lajos`——>`get name`
    - 创建相关目录：`sudo makdir /etc/redis`(配置文件路径)——>`sudo mkdir /var/lib/redis`(redis数据库存储路径)
    - 安装服务：`cd /usr/local/redis/utils`——>`sudo ./install_server.sh`
    - 重启服务：`ps ajx | grep redis`——>`sudo kill -9 对应的进程号`
    - 测试：`redis-server`——>`redis-cli`
    - 配置文件：`cd /etc/redis`——>`sudo vim /etc/redis/6379.conf`——>可以修改`bind`、`daemonize`、`requirepass`——>然后重启服务
    - 直接开启客户机：`redis-cli`
+ 连接测试
    - 检查服务是否启动：`ps aux(ajx, -ef) | grep redis`
    - 连接：`redis-cli -h 主机 -p 端口 -a 密码`
    - 退出：`quit`
+ 密码管理：默认没有密码，若设置密码，需要通过`auth`认证
    - 单次有效：
        - 获取密码：`config get requirepass`
        - 设置密码：`config set requirepass 123456`
        - 密码认证：`auth 123456`
    - 永久有效：修改配置文件`/etc/redis/redis.conf`
        - 将`requirepass xxxxx`行修改设置的密码
        - 重新启动`redis`服务
### 3.2.2. `Redis`命令

+ 常用

```markdown
ping：测试连接情况，回复PONG表示OK
quit：退出连接
auth：密码认证
select：选择库，总共有16个，序号0~15，默认是第0个
info：查看服务器信息
command：查看支持的命令
flushdb：清空当前库
flushall：清空所有库
save：前台进行持久化存储
bgsave：后台进行持久化存储
exists：判断指定键是否存在
del：删除键
```
+ 字符串(`string`)

```markdown
set：设置
get：获取
getset：获取之后再设置
mset：设置多个
mget：获取多个
incr：加1
decr：减1
incrby：加指定的值
decrby：减指定的值
append：追加内容
```
+ 哈希(`hash`)

```markdown
hset：设置单个属性
hget：获取单个属性
hmset：设置多个属性
hmget：获取多个属性
hgetall：获取所有属性
hdel：删除键值对
hexists：判断指定键的指定字段是否存在
hkeys：获取指定键的所有属性名
hvals：获取指定键的所有属性值
hlen：获取指定键的属性个数
```
+ 列表(`list`)

```markdown
lpush：从左边(头部)插入数据
lpop：从左边(头部)删除数据
lrange：获取指定区间范围内的数据，0 -1表示所有
lindex：根据索引获取元素
llen：获取列表长度(元素个数)
rpush：从右边(尾部)插入数据
rpop：从右边(尾部)删除数据
lrem：移除指定个数的指定元素
```
+ 集合(`set`)

```markdown
sadd：添加元素
scard：统计元素个数
sdiff：求差集
sinter：求交集
smembers：获取指定集合的所有成员
sismember：判断是否在集合中
smove：移动元素
spop：随机的删除一个元素
srandmember：随机获取指定个数的元素
srem：移除元素
sunion：求并集
```
+ 有序集合(`sorted set`)

```markdown
zadd：添加元素
zcard：统计个数
zcount：指定分数区间内的元素数量
zrange：返回指定索引范围内的元素
zrangebyscore：返回指定分数区间的元素
zrank：返回指定成员的索引值
zrem：移除元素
zscore：获取指定元素的排序指标(分数)
```
### 3.2.3. `Python`操作`Redis`

`redis`扩展库中有两个类，`Redis`和`StrictRedis`，`StrictRedis`实现了官方的命令，`Redis`是它的子类，兼容老版本。扩展库没有实现`select`方法，可以通过连接时指定使用的库。

+ 安装扩展：`pip install redis`

#### 3.2.3.1. 简单连接

+ `redis.Redis(host='localhost', port=6379, db=0, password=None, socket_timeout=None, socket_connect_timeout=None,socket_keepalive=None, socket_keepalive_options=None, connection_pool=None, unix_socket_path=None,encoding='utf-8', encoding_errors='strict', charset=None, errors=None, decode_responses=False, retry_on_timeout=False, ssl=False, ssl_keyfile=None, ssl_certfile=None, ssl_cert_reqs='required', ssl_ca_certs=None, max_connections=None, single_connection_client=False, health_check_interval=0)`：`db`表示选定的数据库，`decode_response`表示解码返回

```python
import redis
# 创建连接对象，所有的命令在代码中都是Redis对象的方法
r = redis.Redis(host='localhost', port=6379, db=0, password=None, decode_response=True)
r.set('name', 'lajos')
print(r.get('name))
```
#### 3.2.3.2. 连接池

多个`redis`对象使用同一个连接池进行连接，避免了多次连接、断开等操作的系统开销。默认，每个Redis实例都会维护一个自己的连接池。可以直接建立一个连接池，然后作为参数Redis，这样就可以实现多个Redis实例共享一个连接池。

```python
import redis

# 创建连接池
pool = redis.ConnectionPool(host='localhost', port=6379, db=0, decode_responses=True)

# 创建Redis对象
r = redis.Redis(connection_pool=pool)
r.set('name', 'lajos')
print(r.get('name'))
```

#### 3.2.3.3. 详细操作命令

[`redis`详细操作命令](https://www.cnblogs.com/melonjiang/p/5342505.html)

#### 3.2.3.4. 管道(`pipeline`)

+ 可以记录多个操作，然后一次将操作发送至数据库，避免了多次连接、断开等操作的系统开效

+ 多个操作可以依次进行保存，然后发送，也可以进行连贯操作

```python
import redis

# 创建连接池
pool = redis.ConnectionPool(host='localhost', port=6379, db=0, decode_responses=True)
# 创建Redis对象
r = redis.Redis(connection_pool=pool)
# 创建管道, 默认支持事务(transaction=True)
pipe = r.pipeline()
# 记录命令
pipe.set('name', 'lajos')
pipe.set('age', 20)
pipe.set('message', 'lajos is a handsome man')
dic = {'a': 'aaa', 'b': 'bbb'}
pipe.hmset('myhash', dic)
# 执行操作
pipe.execute()
print(r.get('message'))
print(r.hget('myhash', 'b'))
```
#### 3.2.3.5. 发布和订阅

`Redis`发布订阅(`pub/sub`)是一种消息通信模式：发送者(`pub`)发送消息，订阅者(`sub`)接收消息。

```python
import redis

class RedisHelper(object):

    def __init__(self, channel=None):
        self.__connection = redis.Redis(host='127.0.0.1', port=6379, decode_responses=True)
        self.channel = 'lajos'
    # 定义发布方法
    def publish(self, msg):
        self.__connection.publish(self.channel, msg)
        return True
    # 定义订阅方法
    def subscribe(self):
        pub = self.__connection.pubsub()
        pub.subscribe(self.channel)
        pub.parse_response()
        return pub
```
+ 发送者

```python
from pythonRedis import RedisHelper

pub = RedisHelper()
while True:
    msg = input('发布者：')
    pub.publish(msg)
# 运行结果
>>> 发布者：hello
发布者：world
发布者：
```

+ 订阅者

```python
from pythonRedis import RedisHelper

sub = RedisHelper()
redis_sub = sub.subscribe()

while True:
    msg = redis_sub.parse_response()
    print(msg)
# 运行结果
>>> ['message', 'lajos', 'hello']
['message', 'lajos', 'world']

```
## 3.3. `MongoDB`

### 3.3.1. `MongoDB`简介

+ MongoDB是一个基于分布式文件存储 的数据库。由`C++`语言编写。旨在为WEB应用提供可扩展的高性能数据存储解决方案。它是一个介于关系数据库和非关系数据库之间的产品，是非关系数据库当中功能最丰富，最像关系数据库的。更多的介绍可查看，[菜鸟教程(https://www.runoob.com/mongodb/mongodb-intro.html](https://www.runoob.com/mongodb/mongodb-intro.html)

+ `MongoDB`的安装(`linux`)

    - 直接安装：`sudo apt-get install mongodb`，此安装可能无法安装最新稳定版本
    - 自定义安装：
        - 按转包下载：到`MongoDB`官方网站[https://www.mongodb.com/download-center/community](https://www.mongodb.com/download-center/community)下载对应版本的安装包，例如，下载`mongodb-linux-x86_64-ubuntu 16.04-4.2.1.tgz`，对应的官网链接为`https://fastdl.mongodb.org/linux/mongodb-linux-x86_64-ubuntu1604-4.2.1.tgz`
        ![`MongoDB`的下载](https://github.com/lajos182/python-essay/blob/master/images/mongodb_download.png)
        - 使用`curl`命令下载：`curl -O https://fastdl.mongodb.org/linux/mongodb-linux-x86_64-ubuntu1604-4.2.1.tgz`
        - 解压：`tar -xzvf mongodb-linux-x86_64-ubuntu1604-4.2.1.tgz`
        - 将解压包拷贝至指定没目录：`sudo mv mongodb-linux-x86_64-ubuntu1604-4.2.1 /usr/local/mongodb`
        - 添加至系统环境变量：`sudo vim /etc/profile`——>在最后一行添加`export PATH=/usr/local/mongodb/bin:$PATH`——>`source /etc/profile`
        - 添加相关配置文件：`sudo vim /etc/mongod.conf`
        ```shell
        verbose=true
  		port=27017
  		logpath=/var/log/mongodb/logs/mongodb.log
  		logappend=true
  		dbpath=/var/lib/mongodb/db
   		directoryperdb=true
  		auth=false
  		fork=true
  		quiet=true
        ```
        - 创建数据库存储、日志文件：`sudo mkdir /var/log/mongodb/logs/ -p`——>`sudo touch /var/log/mongodb/logs/mongodb.log`——>`sudo mkdir /var/lib/mongodb/db –p`
        - 注册开机启动：`sudo vim /ect/init.d/mongodb`
        ```shell
        #!/bin/sh
        ### BEGIN INIT INFO
        # Provides: mongodb
        # Required-Start:
        # Required-Stop:
        # Default-Start: 2 3 4 5
        # Default-Stop: 0 1 6
        # Short-Description: mongodb
        # Description: mongo db server
        ### END INIT INFO
        . /lib/lsb/init-functions
        PROGRAM=/usr/local/mongodb/bin/mongod
        MONGOPID=`ps -ef | grep 'mongod' | grep -v grep | awk '{print $2}'`
        test -x $PROGRAM || exit 0
        case "$1" in
        start)
        ulimit -n 3000
        log_begin_msg "Starting MongoDB server"
        $PROGRAM -f /etc/mongod.conf
        log_end_msg 0
        ;;
        stop)
        log_begin_msg "Stopping MongoDB server"
        if [ ! -z "$MONGOPID" ]; then
        kill -15 $MONGOPID
        fi
        log_end_msg 0
        ;;
        status)
        ;;
        *)
        log_success_msg "Usage: /etc/init.d/mongodb {start|stop|status}"
        exit 1
        esac
        exit 0
        ```
        `sudo chmod +x /etc/init.d/mongodb`
        - 注册开机脚本：`sudo update-rc.d mongodb defaults`(注意：移除使用`sudo update-rc.d –f mongodb remove`)
        - 启动服务：`sudo service mongodb start`
        - 客户端连接：`mongo`(若无法连接，可查看环境变量，或者重新开启会话)
    - 官方安装：
        - 导入`MongoDB`公共`GPG`密钥：`wget -qO - https://www.mongodb.org/static/pgp/server-4.2.asc | sudo apt-key add -`(注意是大写`O`)，如果收到指示`gnupg`未安装的错误，则输入命令`sudo apt-get install gnupg`，安装成功后重新输入`GPG`密钥
        - 创建`MongoDB`相关文件：选择合适的`MongoDB`版本，例如`Ubuntu16.04`，需要执行命令`echo "deb [ arch=amd64 ] https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/4.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.2.list`
        - 重新加载本地软件包数据库：`sudo apt-get update`
        - 安装`MongoDB`：可以选择安装最新版本(`sudo apt-get install -y mongodb-org`)，也可指定版本安装(`sudo apt-get install -y mongodb-org=4.2.1 mongodb-org-server=4.2.1 mongodb-org-shell=4.2.1 mongodb-org-mongos=4.2.1 mongodb-org-tools=4.2.1`)。
        - 配置文件：`/ect/mongod.conf`
        - 启动服务：`sudo service mongod start`
+ `MongoDB`与`MySQL`比较

| MySQL    | MongoDB          |
| -------- | ---------------- |
| database | db(数据库)       |
| table    | collection(集合) |
| 一条数据 | document(文档)   |

### 3.3.2. `MongoDB`基本操作

+ `db`操作
    - 查看所有数据库：`show dbs`
    - 查看当前数据库：`db`或者`db.getName()`
    - 创建或切换数据库：`use python`
    - 若使用的数据库不存在则创建然后切换，存在直接切换
    - 新建的数据库没有数据时，`show dbs`显示不出来
    - 删除当前使用的数据库：`db.dropDatabase()`
    - 退出：`exit`或`quit()`
    - 查看帮助：`help`
+ `collection`操作
    - 查看当前数据库的所有集合：`show collections`
    - 创建集合：
        - 单纯创建：`db.createCollection('star')`，创建一个空集合
        - 按需创建：`db.stu.insert({name:'lufei', age:22})`，直接使用不存在的集合，并插入数据
    - 删除当前数据库指定的集合：`db.stu.drop()`
+ `document`操作
    - 增加文档：
        - `insert`
            - 插入一条：`db.star.insert({name:'linjunjie', age:32, treasure:200, isDelete:0})`
            - 插入多条：
            ```mongodb
            db.star.insert([
            {name:'zhoujielun', age:41, treasure:500, isDelete:0}, 
            {name: 'baijingting', age:26, treasure:80, isDelete:0}
            ])
            ```
        - `save`
        ```moogodb
        # 不指定_id字段，功能等价于insert
        db.star.save({name:'xiaozhan',age:31,treasure:90,isDelete:1})
        # 指定_id字段，相当于更新操作
        db.star.save({_id:ObjectId("5dd63af30246a3087b2054ce"), name:"xiaozhan", age: 31, treasure: 90, isDelete: 0 })
        ```
    - 更新文档：
        - `save`：保存文档时，需要指定`_id`字段
        - `update`：`db.集合.update(query, update, {upsert: <boolean>, multi: <boolean>})`
        ```mongodb
        db.star.update({name: 'zhoujielun'}, {$set: {age: 40}})
        db.star.update({isDelete: 0}, {$inc: {age: 3}})
        db.star.update({isDelete: 0}, {$set: {isDelete: 1}}, {multi: true})
        db.star.update({name: 'zhoujie'}, {$set: {age: 40}}, {upsert: true})
        ```
        > `query`：表示查询条件<br>
        > `update`：表示跟新设置<br>
        > `$set`：表示设置<br>
        > `$inc`：表示增加<br>
        > `upsert`：更新的查询结果不存在，是否作为新数据插入<br>
        > `multi`：符合条件的数据是否全部更新，`true`表示全部更新，`false`只更新一条，默认为`false`
    - 删除文档：`remove`：`db.集合.remove(query, {justOne: <boolean>})`，默认为`false`
    ```mongodb
    # 默认删除所有匹配到的文档
    db.star.remove({name: 'zhoujie'})
    # 只删除一条匹配到的文档
    db.star.remobe({age: 26}, {justOne: true})
    ```
    - 查询文档：`db.star.find()`
        - 格式：`db.集合.find(query, {key1: 0, key2: 0})`
        ```mongodb
        db.star.find({name: 'xiaozhan'})
        db.star.find({name: 'xiaozhan'}, {name: 1, age: 1})
        ```
        > `query`表示查询条件；<br>
        > 第二个参数值为1表示要显示的字段，为0表示不显示的字段；<br>
        > 选择字段时或排序字段只能选择一种情况，要么都选择，要么都排除
        - `pretty()`：格式化显示文档以字典的形式，`db.star.find().pretty()`
        - `findOne()`：查询一条文档，`db.star.findOne()`
        - `count()`：统计查询文档的个数

### 3.3.3. `MongoDB`进阶操作

+ 查询条件操作符
    - 大于：`$gt`，格式是`db.集合.find({<key>: {$gt: <value>}})`，如`db.star.find({age: {$gt: 35}})`
    - 大于等于：`$gte`
    - 小于：`$lt`
    - 小于等于：`$lte`
    - 等于：不写符合就是等于
    - 多个条件：`db.star.find({age: {$gt: 31, $lt: 40}})`
    - 正则：格式是`db.集合.find({<key>: /正则表达式/})`，如`db.star.find({name: /an$/})`
+ 条件合并`and/or`
    - `and`：表示并且，格式：`db.集合.find({条件1，条件2})`，如，`db.star.find({isDelete: 0, age: {$gt: 35}})`
    - `or`：表示或者，格式：`db.集合.find({$or: [{条件1}，{条件2}])`，如，`db.star.find({$or: [{age: {$gt: 35}}, {age: {$lt: 31}}]})`
+ 限制结果集
    - 限制：`limit`，如，`db.star.find().limit(2)`
    - 跳过：`skip`，如，`db.star.find().skip(1).limit(1)`
+ 结果集排序
    - 格式：`db.集合.find().sort({<key>: 1/-1})`，1表示升序，-1表示降序
    - 示例：`db.star.find().sort({age: 1})`

### 3.3.4. 权限认证

+ `mongod.conf`配置文件：

  ```shell
  #  mmapv1:
  #  wiredTiger:
  
  # where to write logging data.
  systemLog:
    destination: file
    logAppend: true
    path: /var/log/mongodb/mongod.log
    quiet: true
    # timeStampFormat: iso8601-utc 
  
  # nework interfaces
  net:
   port: 27017
   bindIp：127.0.0.1
   
  # how the process runs
  processManagement:
    timeZoneInfo：/usr/share/zoneinfo
    
  security:
    authorization: enabled
    
  #operationsProfiling:
  
  #replication
  
  #sharding
  
  ## Enterprise-Only Options:
  
  #auditLog
  
  #snmp
  ```

  > - **`systemLog`**：
  >   - `systemLog.verbosity`：`integer`，日志文件输入的级别，越大级别越低
  >   - `systemLog.quiet`：`boolean`，该模式下会限制输出信息，数据库命令输出，副本集活动，连接接受事件，连接关闭事件。
  >   - `systemLog.traceAllExceptions`：`string`，打印`verbose`信息来调试，用来记录额外的异常日志
  >   - `systemLog.syslogFacility`：`string`，默认为`user`，指定`syslog`日志信息的设备级别。需要指定`--syslog`来使用这个选项
  >   - `systemLog.path`：`string`，发送所有的诊断日志，默认重启后会覆盖
  >   - `systemLog.logAppend`：`boolean`，是否启用追加日志
  >   - `systemLog.destination`：`string`，指定一个文件或`syslog`，如果指定为文件，必须同时指定`systemLog.path`
  >   - `systemLog.timeStampFormat`：`string`，默认为`iso8601-local`
  > - **`processManagement`**：
  >   - `processManagement.pidFilePath`：`string`，指定进程的`ID`，与`--fork`配合使用，不指定则不会创建
  >   - `processManagement.fork`：`boolean`，默认为`false`，`true`表示守护进程在后台运行
  >   - `processManagement.timeZoneInfo`：`string`，如，`/usr/share/zoneinfo`，时区
  > - `net`：
  >   - `net.port`：`interger`，默认`27017`，`mongodb`实例监听的端口号
  >   - `net.bindIp`：`string`，2.6版本默认为`127.0.0.1 `，指定`mongodb`实例绑定的`ip`，为了绑定多个`ip`，可以使用逗号分隔
  >   - `net.maxIncomingConnections`：`integer`， 默认为1000000，`mongodb`实例接受的最多连接数，如果高于操作系统接受的最大线程数，设置无效
  >   - `net.wireObjectCheck`：`boolean`，默认为`true `，检查文档的有效性。会稍微影响性能
  >   - `net.http.enabled`：`boolean`，默认为`false`， 打开`http`端口，会导致更多的不安全因素
  >   - `net.unixDomainSocket.enabled`：`boolean`，默认为`false`， 停止`UNIX domain socket`监听。 `mongodb`实例会一直监听`UNIX socket`，除非`net.unixDomainSocket.enabled`设置为`true`，`bindIp`没有设置，`bindIp`没有默认指定为`127.0.0.1`
  >   - `net.unixDomainSocket.pathPrefix`：`string`，默认为`/tmp unix Socket`所在的路径
  >   - `net.ipv6`：`boolean`，默认为`false`，打开`IPV6`功能，默认为关闭的
  >   - `net.http.JSONPEnabled`：`boolean`，默认为`false`，运行`json`访问`http`端口，打开会导致更多的不安全因素
  >   - `net.http.RESTInterfaceEnabled`：`boolean`，默认为`false`， 即使`http`接口选项关闭，打开也会暴露`http`接口，会导致更多的不安全因素。
  > - **`security`**：
  >   - `security.keyFile`：`string`， 指定分片集或副本集成员之间身份验证的`key`文件存储位置
  >   - `security.clusterAuthMode`：`string`， 集群认证中利用到这个模式，如果使用`x.509`安全机制，可以在这里指定
  >   - `keyFile,sendKeyFile,sendX509,x509`：默认的`mongodb`发行版是不支持`ssl`的，可以使用专业版的或重新自行编译`mongodb`
  >   - `security.authorization`：`string`，默认为`disabled` ，`enabled`表示打开访问数据库和进行操作的用户角色认证
  > - **`operationProfiling`**：
  >   - `operationProfiling.slowOpThresholdMs`：`integer`，默认100 指定慢查询时间，单位毫秒，如果打开功能，则向`system.profile`集合写入数据
  >   - `operationProfiling.mode`：`integer`，默认0，改变分析日志输出级别。 0，1，2,分别对应关闭，仅打开慢查询，记录所有操作
  > - **`storage`**：
  >   - `storage.dbPath`：`string `，指定数据文件的路径
  >   - `storage.directoryPerDB`：`boolean`，默认关闭。指定存储每个数据库文件到单独的数据目录。如果在一个已存在的系统使用该选项，需要事先把存在的数据文件移动到目录。
  >   - `storage.indexBuildRetry`：`boolean`，,默认为`true` 。指定数据库在索引建立过程中停止，重启后是否重新建立索引。
  >   - `storage.preallocDataFiles`：`boolean`，默认`true`， 是否预先分片好数据文件。
  >   - `storage.nsSize`：`integer`,默认16 指定命名空间的大小，即`.ns`后缀的文件。最大为2047MB,16M文件可以提供大约24000个命名空间。
  >   - `storage.quota.enforced`：`boolean`,默认`false` 限制每个数据库的数据文件数目。可以通过`maxFilesPerDB`调整数目。
  >   - `storage.quota.maxFilesPerDB`：`integer`,默认为8 限制每个数据库的数据文件数目。
  >   - `storage.smallFiles`：`boolean`,默认为`false` 限制`mongodb`数据文件大小为512MB，减小`journal`文件从1G到128M,适用于有很多数量小的数据文件。
  >   - `storage.syncPeriodSecs`：`number`,默认60。`mongodb`文件刷新频率，尽量不要在生产环境下修改。
  >   - `storage.repairPath`：`string`，默认为指定`dbpath`下的`_tmp`目录。 指定包含数据文件的根目录，进行`--repair`操作。
  >   - `storage.journal.enabled`：`boolean`,默认`64bit`为`true`，`32bit`为`false `记录操作日志，防止数据丢失。
  >   - `storage.journal.debugFlags`：`integer` 提供数据库在非正常关闭下的功能测试。
  >   - `storage.journal.commitIntervalMs`：`number`，默认为100或30，`journal`操作的最大间隔时间。可以是2-300`ms`之间的值，低的值有助于持久化，但是会增加磁盘的额外负担。 如果`journal`和数据文件在同一磁盘上，默认为100`ms`。如果在不同的磁盘上为30`ms`。 如果强制`mongod`提交日志文件，可以指定`journal`: `true`，指定后，时间变为原来的三分之一。
  > - **`replication`**：
  >   - `replication.oplogSizeMB`：`integer`,默认为磁盘的5% 指定`oplog`的最大尺寸。对于已经建立过`oplog.rs`的数据库，指定无效。
  >   - `replication.replSetName`：`string` 指定副本集的名称。
  >   - `replication.secondaryIndexPrefetch`：`string`，默认为all 指定副本集成员在接受`oplog`之前是否加载索引到内存。默认会加载所有的索引到内存。` none`，不加载；`all`，加载所有；`_id_only`，仅加载`_id`。
  > - **`sharding`**：
  >   - `sharding.clusterRole`：`string`，指定分片集的`mongodb`角色。 `configsvr`,配置服务器，端口27019;`shardsvr`,分片实例，端口27018。
  >   - `sharding.archiveMovedChunks`：`integer `在块移动过程中，该选项强制mongodb实例保存所有移动的文档到moveChunk目录。
  > - **`auditLog`**：
  >   - `auditLog.destination`：`string`, `syslog`,以`json`格式保存身份验证到`syslog`，`windows`下不可用，`serverity`级别为`info`，`facility`级别为`user`。`console`以`json`格式输出信息到标准输出。 `file`以`json`格式输出信息到文件。
  >   - `auditLog.forma`t：`string` 指定输出文件的格式` JSON`,输出`json`格式文件;`BSON`,输出`bson`二进制格式文件。
  >   - `auditLog.path`：如果`--auditDestination`的值为`file`，则该选项指定文件路径。
  >   - `auditLog.filter`：`document`, 指定过滤系统身份验证的格式为:
  > - **`snmp`**：
  >   - `snmp.subagent`：`boolean` 运行`SNMP`为一个子代理。
  >   - `snmp.master`：`boolean `运行`SNMP`为一个主进程。

- 在`admin`数据库中创建认证用户：`mongo`—>`use admin`—>`db.createUser({user: 'lajos', pwd: '123456', 'roles': [{role: 'root', 'db': 'admin'}]})`—>`show users`或`db.system.users.find()`
  - `role`：指定用户的角色，可选的角色有以下几种
    - 数据库用户角色：`read`、`readWrite`
    - 数据库管理角色：`dbAdmin`、`dbOwner`、`userAdmin`
    - 集群管理角色：`clusterAdmin`、`clusterManager`、`clusterMonitor`、`hostManager`
    - 备份恢复角色：`backup`、`restore`
    - 所有数据库角色：`readAnyDatabase`、`readWriteAnyDatabase`、`userAdminAnyDatabase`、`dbAdminAnyDatabase`
    - 超级用户角色：`root`
    - 内部角色：`__system`
    > (1)`Read`：允许用户读取指定数据库<br>
    > (2)`readWrite`：允许用户读写指定数据库<br>
    > (3)`dbAdmin`：允许用户在指定数据库中执行管理函数，如索引创建、删除，查看统计或访问`system.profile`<br>
    > (4)`userAdmin`：允许用户向`system.users`集合写入，可以找指定数据库里创建、删除和管理用户<br>
    > (5)`clusterAdmin`：只在`admin`数据库中可用，赋予用户所有分片和复制集相关函数的管理权限<br>
    > (6)`readAnyDatabase`：只在`admin`数据库中可用，赋予用户所有数据库的读权限<br>
    > (7)`readWriteAnyDatabase`：只在`admin`数据库中可用，赋予用户所有数据库的读写权限<br>
    > (8)`userAdminAnyDatabase`：只在`admin`数据库中可用，赋予用户所有数据库的`userAdmin`权限<br>
    > (9)`dbAdminAnyDatabase`：只在`admin`数据库中可用，赋予用户所有数据库的`dbAdmin`权限<br>
    > (10)`root`：只在`admin`数据库中可用。超级账号，超级权限
- 修改配置文件做认证：`vim /etc/mongod.conf`—>将`security`中的`authorization`改为`enabled`
- 重启`mongod`服务：`sudo service mongod restart`
- 认证：`mongo`—>`use admin`—>`db.auth('lajos', '123456')`

### 3.3.5. `Python`操作`MongoDB`

+ 安装扩展库：`pip install pymongo`

+ 创建连接及相关操作:

```python
import pymogo
# 创建连接
connect = pymongo.MongoClient(host='localhost', port=27017)
# 选择数据库, test是数据库名称
# 如果mongodb设置账户和密码校验，先要进行校验
admin = connect.admin
admin.authentication(username='lajos', password='123456')

db = connnect.test
# 查看当前数据库的所有集合
print(db.collection_names())
# 查询文档, 得到的结果是一个生成器，需要遍历才可以获取结果
ret = db.star.find()
print([i for i in ret])
# 增加文档，得到的返回值是对应的_id
ret1 = db.star.insert({'name': 'lajos', age: 18})
ret2 = db.star.insert_one(({'name': 'lajos', age: 18})
ret3 = db.star.insert([
    {'name': 'wjk', age: 20},
    {'name': 'yyqx', age: 21},
])
ret4 = db.star.insert_many([
    {'name': 'wjk', age: 20},
    {'name': 'yyqx', age: 21},
])
# 根据_id查询，需要注意要将id值转化为bson类型
from bson.objectid import ObjectId
ret = db.star.find({'_id': ObjectId('5dd6518225d1748cf88d0d3b')})
print([i for i in ret])
```

# 4. 第四部分  Linux相关知识

## 4.1. `Linux`系统简介

+ 操作系统严格意义上来讲就是一个内核，是一套管理软硬件资源的软件组件。我们平时所说的操作系统其实是发行版，包括：内核 + 桌面环境 + 常用软件，常见的内核有windows、Linux

+ 常见的操作系统：
    - 桌面版：windows系列、Ubuntu(桌面)、MacOS
    - 服务器：windows server、Linux系列、Unix系列
    - 移动端：Android、iOS、Symbian、windows phone、Ali OS
+ 32位和64位的区别：简单理解：就相当于4车道与8车道，本质上是寻址空间的区别。
    - 32位：理论值4*2^10*2^10*2^10，即4G，大概可用内存为3.25G
    - 64位：理论值2^64，现在主流的主板一般最大支持128G
+ `Linux`是一套免费使用和自由传播的类`Unix`操作系统，是一个基于`POSIX`和`UNIX`的多用户、多任务、支持多线程和多`CPU`的操作系统。它能运行主要的`UNIX`工具软件、应用程序和网络协议。它支持32位和64位硬件。`Linux`继承了`Unix`以网络为核心的设计思想，是一个性能稳定的多用户网络操作系统。

+ `Linux`发行版就是在内核的基础上，添加特定桌面环境和常用软件，省去了自己组装的麻烦。常见的桌面版有`ubuntu(desktop)`、`Ubuntu kylin`、`deepin`，服务器有`debian`、`redhat`、`Ubuntu(server)`、`centos`
![Linux发行版](https://github.com/lajos182/python-essay/blob/master/images/linux.png)

+ `Linux`启动过程：`Linux`系统的启动过程可以分为5个阶段
    - 内核的引导：计算机打开电源后，首先是`BIOS`开机自检，按照`BIOS`中设置的启动设备（通常是硬盘）来启动。操作系统接管硬件以后，首先读入`/boot`目录下的内核文件。
    - 运行`init`：`init`进程是系统所有进程的起点，`init`程序首先是需要读取配置文件`/etc/inittab`，里面记录系统的运行级别，`Linux`系统级别有7个：
        - 0：关机模式
        - 1：单用户模式，`root`权限
        - 2 ~ 5：多用户模式(桌面)
        - 6：重启
    - 系统初始化：执行对应级别目录下的脚本，如级别5，对应`/etc/rc5.d`目录；解析用户自定义的启动脚本，如，`/etc/rc.local`
    - 建立终端：`rc`执行完毕后，返回`init`，`init`会打开6个终端，以便用户登录系统
    - 用户登录系统：命令行登录、`ssh`登录、图形界面登录

## 4.2. `Linux`目录结构及`vim`

+ 文件系统：操作管理存储设备或分区上的文件的方法和数据结构，也就是存储设备上组织文件的方式。操作系统中**负责管理和存储文件信息**的软件机构叫文件管理系统，简称为文件系统。常见的文件系统有：
    - `fat16(MS-DOS 6.X)`，分区最大2G
    - `fat32(windows 95)`，单个文件最大4G，性能较弱，容易产生碎片
    - `ntfs(window nt)`，提升了fat32文件系统的稳定性
    - `ext4(Linux)`，扩展型日志文件系统
    - `hfs[+] (Mac)`，苹果设备的文件系统
    - `exfat(win/mac)`，可以支持4G以上的单个文件，适合于闪存
+ 根目录结构：

    | 目录          | 说明                                       |
    | ----------- | ---------------------------------------- |
    | /           | 根目录                                      |
    | /bin        | 大多数的操作命令                                 |
    | /boot       | 系统启动相关文件                                 |
    | /cdrom      | 挂在光盘                                     |
    | /dev        | 设备文件(linux下有一切设备皆文件之称)                   |
    | /etc        | 配置文件目录(经常使用)                             |
    | /home       | 所有普通用户的家目录，一个用户对应该目录下的一个文件夹              |
    | /lib        | 库文件                                      |
    | /lib64      | 64位库文件                                   |
    | /lost+found | 系统出现异常时保存信息以便恢复，平时是空的                    |
    | /media      | 自动识别设备的挂载点                               |
    | /mnt        | mount，专门用于挂载的目录                          |
    | /opt        | option，用于安装可选软件                          |
    | /proc       | 虚拟的文件系统，可以映射硬件信息                         |
    | /root       | 超级用户(root)的家目录                           |
    | /run        | 存放系统运行时的文件，如：进程文件                        |
    | /sbin       | 超级用户使用的命令存放目录                            |
    | /snap       | Ubuntu自己搞的一个包管理系统                        |
    | /srv        | service，存储本机提供的数据或服务                     |
    | /sys        | 类似于proc，可以映射内核信息                         |
    | /tmp        | 保存随时可能销毁��临时文件                            |
    | /usr        | 之前的功能同home，现在是unix system resource，用户安装软件的目录 |
    | /var        | 系统产生的不会自动销毁的文件，如：日志文件                    |
    > 隐藏文件：以'.'开头的文件就是隐藏文件<br>
    > '.'：表示当前目录<br>
    > '..'：表示上一级目录<br>
    > '~'：表示当前用户的家目录<br>
+ `VIM`编辑器：`vi`发展出来的一个文本编辑器，被誉为"终端编辑器之神"，可以直接使用`sudo apt-get install vim`进行安装，有三种工作模式：
    - 正常模式(命令模式)：使用vim打开的默认模式

        | 命令/操作           | 说明             |
        | --------------- | -------------- |
        | vim filename    | 打开/新建一个文件      |
        | ESC             | 切换到正常模式        |
        | ZZ（shift + zz）  | 保存退出……         |
        | !v              | 打开最后使用vim打开的文件 |
        | 光标定位            |                |
        | vim filename +n | 打开文件，将光标定位到第n行 |
        | vim filename +  | 打开文件，将光标定位到尾行  |
        | gg              | 定位到首行          |
        | G               | 定位到尾行          |
        | ngg             | 定位到第n行         |
        | ^/0             | 定位到行首          |
        | $               | 定位到行尾          |
        | k               | ↑              |
        | j               | ↓              |
        | h               | ←              |
        | l               | →              |
        | ctrl + f        | 下翻一页           |
        | ctrl + b        | 上翻一页           |
        | ctrl + d        | 下翻半页           |
        | ctrl + u        | 上翻半页           |
        | 内容处理            |                |
        | x               | 向右删除一个字符       |
        | nx              | 向右删除n个字符，n表示个数 |
        | X               | 向左删除一个字符       |
        | nX              | 向左删除n个字符，n表示个数 |
        | dd              | 删除光标所在行        |
        | ndd             | 删除光标开始的n行      |
        |                 | 粘贴剪切板中的内容      |
        | yy              | 复制光标所在行        |
        | nyy             | 复制光标开始的n行      |
        | u               | 撤销             |
        | ctrl + r        | 反撤销            |

  - 插入模式(输入模式)：可以完成文件内容的输入编辑等，输入一下字符可以进入该模式：

    | 命令   | 说明               |
    | ---- | ---------------- |
    | i    | 在光标位置插入          |
    | I    | 在第一个非空字符插入       |
    | a    | 在光标的下一个字符输入      |
    | A    | 在行尾插入            |
    | o    | 在光标所在的行下面插入空行    |
    | O    | 在光标所在的行上面插入空行    |
    | s    | 删除光标所在字符，并进入输入模式 |
    | S    | 删除光标所在行，并进入输入模式  |

  - 单行模式(编辑模式)：可以完成文件的整体编辑保存等操作，输入':'即可进入

    | 命令                | 说明                          |
    | ----------------- | --------------------------- |
    | :w                | 保存                          |
    | :q                | 退出                          |
    | :wq               | 保存退出                        |
    | :x                | 保存退出                        |
    | :w!               | 强制保存                        |
    | :q!               | 强制退出，不保存修改                  |
    | :e!               | 放弃修改，恢复到修改之前的状态             |
    | :w newfile        | 文件另存为                       |
    |                   |                             |
    | :set nu[mber]     | 显示行号                        |
    | :set nonu[mber]   | 隐藏行号                        |
    | :set tabstop=4    | 设置一个tab缩进4个字符               |
    | :set mouse=a      | 启用鼠标的点击功能                   |
    |                   |                             |
    | [:]/内容            | 查找指定内容，n下翻，N上翻              |
    | [:]?内容            | 查找指定内容，N下翻，n上翻              |
    | :%s/原内容/新内容/[g]   | 所有行内容替换，g表示全局(默认只能替换一行中第一处) |
    | :m,ns/原内容/新内容/[g] | m到n行内容替换，g用法同上              |
    | 光标定位              |                             |
    | :n                | 将光标定位到第n行，n表示行号             |

    > 若非正常关闭了`vim`，可能会产生临时的交换文件，再次打开时会出现特定的界面，可以根据提示进行内容的恢复以及交换文件的删除，也可以手动将交换文件删除，下次就`OK`了。交换文件时隐藏的(`ls -a`)<br>
    > vim配置文件：打开文件后的配置是临时的，关闭后就失效了
        > - 在用户家目录创建一个文件`.vimrc`
        > - 将`vim`相关的配置写在文件中
        > - 若文件没有生效，需要重新加载一次`source ~/.vimrc`
+ `help`的使用：查看命令的帮助文档，如`ls --help`。

+ `man`的使用：是`manul`的缩写，是一个命令，可以查询系统中标准的帮助文档

    | 命令             | 说明                 |
    | -------------- | ------------------ |
    | man name       | 查看指定内容(命令/函数)的帮助文档 |
    | q              | 退出查询               |
    | ↓ 或 enter      | 向下翻一行              |
    | ↑              | 向上翻一行              |
    | pageup         | 向上翻一页              |
    | pagedown 或 空格键 | 向下翻一页              |
    | ?内容            | 在帮助文档进行查找指定内容      |

## 4.3. 文件操作

`Linux`系统是一种典型的多用户系统，不同的用户处于不同的地位，拥有不同的权限。为了保护系统的安全性，`Linux`系统对不同的用户访问同一文件（包括目录文件）的权限做了不同的规定。

### 4.3.1. 常识命令
- `ls`：查看指定目录的内容，不指定目录是查看当前工作目录

    | 选项 | 说明                        |
    | ---- | --------------------------- |
    | -a   | 显示所有文件，包括隐藏文件    |
    | -l   | 列表显示，详细信息           |
    | -h   | 人性化的显示大小，如：K/M/G  |
    > 例如，`ls -l`显示的结果如下，格式为：类型及权限  引用数  用户  用户组  大小  月  日  年/时间  名称 
    ```shell
    [root@www /]# ls -l
    total 64
    dr-xr-xr-x   2 root root 4096 Dec 14  2012 bin
    dr-xr-xr-x   4 root root 4096 Apr 19  2012 boot
    ……
    ```
- 文件类型：`ls -l`显示结果中的第一部分的第一列

    | 符号   | 类型     |
    | ---- | ------ |
    | -    | 普通文件   |
    | d    | 目录文件   |
    | l    | 链接文件   |
    | c    | 字符设备文件 |
    | b    | 块设备文件  |
    | s    | 套接字文件  |
    | p    | 管道文件   |

- `cd`：切换工作目录

    | 符号 | 说明                   |
    | ---- | ---------------------- |
    | .    | 当前目录               |
    | ..   | 上一级目录             |
    | ~    | 当前用户的家目录       |
    | -    | 表示上次切换之前的目录 |
    | /    | 表示根目录             |
    > (1)使用cd时，不指定目标地址，会切换到家目录
    > (2)凡是以/开头的目录都是绝对目录
    > (3)凡是以.或..开头的目录都是相当目录
- `pwd`：查看当前工作目录
- `alias`：给命令起别名，如`l`、`la`、`ll`等
### 4.3.2. 查看文件

| 命令 | 说明                                                         |
| ---- | ------------------------------------------------------------ |
| cat  | 从上到下，显示文件全部内容                                   |
| tac  | 从下到上，显示文件全部内容                                   |
| head | 查看开头指定行数的内容，不指定时默认10行，如：head -20 filename |
| tail | 查看文件末尾指定行数的内容，不指定时默认10行，如：tail -5 filename |
| nl   | 功能与cat相同，但是多显示了行号                              |
| wc   | 统计显示，内容：行数 单词数 字符数 文件名                    |
| more | 一点一点查看内容                                             |
| less | 一点一点查看内容                                             |
> `more/less`使用说明：
    > - 显示一屏就停止
    > - `q`退出查看
    > - `enter`下翻一行
    > - 空格下翻一屏
    > - `more`查看完毕会自动退出，`less`不会
    > - `less`可以使用上下按钮上下翻看，`more`不可以
    > - 经常集合管道使用：`ls /etc | more`
### 4.3.3. 文件及目录

| 命令  | 说明                                     |
| ----- | ---------------------------------------- |
| touch | 新建文件，可以是多个                     |
| rm    | 删除文件或目录(删除目录时要传递'-r'选项) |
| cp    | 拷贝文件或目录(拷贝目录是要传递'-r'选项) |
| mv    | 移动文件或目录                           |
| mkdir | 创建目录，可以是多个                     |
| rmdir | 删除空目录                               |

> 选项说明
    > - `-r`：删除或拷贝目录时需要添加，表示递归操作
    > - `-f`：表示强制操作，没有提示信息
    > - `*`：表示模糊匹配，如：`rm *.py`，表示删除所有的`py`文件
    > - `-p`：创建目录时若需要创建中间目录，可以添加此选项
### 4.3.4. 用户及用户组

+ 相关命令

    | 命令       | 说明                                       |
    | -------- | ---------------------------------------- |
    | whoami   | 查看当前登录的用户名                               |
    | useradd  | 新建用户，-d指定家目录，-m不存在，-s指定shell             |
    | userdel  | 删除用户，-r会删除用户家目录                          |
    | passwd   | 设置指定用户的密码，没有指定用户时设置时当前用户的密码              |
    | su -     | 切换用户，一定要加上'-'，否则只会切换家目录，但是环境没有切换，不指定用户时默认切换到root用户(记得先给root用户设置密码) |
    | sudo     | 以指定用户(root)身份执行命令                        |
    | visudo   | 专门用于编辑/etc/sudoers文件的命令，需要将指定用户添加进去才可以使用sudo命令，如：test ALL=(ALL:ALL) ALL；使用sudo update-alternatives --config editor可以修改系统默认编辑器(nano) |
    | groupadd | 新建用户组                                    |
    | groupdel | 删除用户组                                    |
    | gpasswd  | 向指定组添加/删除指定的用户，如：gpasswd -a/-d  user group |
    | groups   | 查看指定用户的组信息                               |
    | chsh     | 修改指定用户的shell解析器，如：sudo chsh test -s /usr/sbin/nologin (禁止登陆) |
    | chown    | 修改文件所属用户[及用户组]，如： sudo chown test[:test] 1.py，递归操作需要加'-R'选项 |
    | chgrp    | 修改文件所属用户组，如：sudo chgrp test 1.py         |

+ 涉及文件
    - /etc/passwd：系统中的用户信息
    - /etc/group：系统中的用户组信息
    - /etc/shadow：系统中的用户密码信息

+ 相关名词
    - uid：用户唯一标识
    - gid：用户组唯一标识
## 4.4. 文件权限
`Linux`系统是一种典型的多用户系统，不同的用户处于不同的地位，拥有不同的权限。为了保护系统的安全性，`Linux`系统对不同的用户访问同一文件（包括目录文件）的权限做了不同的规定。在`linux`下，所有的文件都涉及权限，分为**所有者**、**所属组**、**其他**三组，所有文件的权限可分为**可读(r)**、**可写(w)**、**可执行(x)**，`-`表示没有改权限。

在`Linux`下使用命令`ls -l`可以显示一个文件的属性及其文件所属的用户和组，如：
```shell
[root@www /]# ls -l
total 64
dr-xr-xr-x   2 root root 4096 Dec 14  2012 bin
dr-xr-xr-x   4 root root 4096 Apr 19  2012 boot
……
```
![Linux文件权限](https://github.com/lajos182/python-essay/blob/master/images/document_permission.png)

+ `chgrp`：更改文件属组，`chgrp [-R] 属组名 文件名`，`-R`表示递归更改文件属组，就是在更改某个目录文件的属组时，如果加上这个参数，那么该目录下的所有文件的属组都会更改。

+ `chown`：更改文件属主，也可以同时更改文件属组，`chown [-R] 属主名 文件名`或`chown [-R] 属主名:属组名 文件名`，例如：`sudo chmod root:root install.log`

+ `chmod`：修改文件9个属性，`chmod [-R] [身份] [操作] [权限] 文件`，`-R`表示进行递归(`recursive`)的持续变更，亦即连同次目录下的所有文件都会变更。该设置可通过**数字**或**符号**来进行设置。

    | 命令       | 选项             |操作              | 权限          | 文件或目录 |
    | ---------- | ---------------- | --------------- | ------------- | ------------- |
    | chmod      | u(所有者)                | +(加入)  | r(可读)   |       |
    |            | g(所属组)               | -(去掉)   | w(可写)   |        |
    |            | o(其他)               | =(设置)     | x(可执行)  |         |
    |            | a(去除权限但不改变其他已存在的权限使用)  |          |         |       |
    > - 例如：给其他用户添加可写的权限，`sudo chmod o+x test.py`
    > - 本质：使用一组(3位)八进制的数据来表示权限，如，0755，展开如下，可以简化`sudo chmod 0755 test.py`
    ```markdown
    转化为二进制：0755 =>   111    101  101
    对应三组身份          所有者  所属组 其他
    每一组的权限：都包括可读、可写、可执行
    实例解析：所有者可读可写可执行，所属组可读可执行，其他可读可执行
    ```
+ `umask`：用来限定新建文件的默认权限，权限与该值相反，`umask [value]`，查看或设置掩码

## 4.5. 文件搜索

+ `find`：用于任意文件的搜索，格式`find [目录] 条件选项`
```markdown
-name：指定名字    sudo find / -name passwd
-maxdepth：指定最大层级深度		sudo find / -maxdepth 2 -name passwd
-type：指定类型（d/l/s/p/c/b）
-size：指定大小，单位：k/m/g，+表示大于，-表示小于，如：find -size +5k，查找大于5k的文件
-mtime/-atime/-ctime：指定修改/访问/创建时间，单位是天，+表示几天前，-表示几天内
-mmin/-amin/-cmin：功能同上，单位是分
-user：指定用户
-group：指定用户组
```
+ `whereis`：显示命令的详细信息，如`whereis ls`，结果如下：
```markdown
ls: /bin/ls /usr/share/man/man1/ls.1.gz
命令名  命令位置  帮助文档
```
+ `grep`：正则表达式搜索(文件内容)，`-i`表示忽略大小写，`-n`显示行号
```shell
# 查找/etc/passwd文件中包含/bin/bash的行，并显示行号
ubuntu@VM-0-6-ubuntu:~$ grep -n /bin/bash /etc/passwd
1:root:x:0:0:root:/root:/bin/bash
30:ubuntu:x:500:500:ubuntu,,,:/home/ubuntu:/bin/bash
# 在2.py中查找包含abc的行，不考虑大小写
ubuntu@VM-0-6-ubuntu:~$ grep -i abc 2.py
# 查看/bin下以'm'开头的命令
ubuntu@VM-0-6-ubuntu:~$ ls /bin | grep '^m'	
```
+ `ln`：链接文件，创建一个文件或目录的链接，格式为`ln [-s] 原文件 新文件`，`ls -l`结果中的第一列第一个为`l`就表示链接文件

+ 软链接和硬链接的区别：
    - 硬链接：使用`ln`时不加`-s`选项创建的链接，相当于一个文件多起了一个名字而已，极少用到
        - 不能给目录创建
        - 不能跨文件系统
    - 软链接：使用`ln`是添加`-s`选项创建的链接，相当于`windows`中的快捷方式，比较常用
        - 可以给目录创建
        - 可以跨文件系统
## 4.6. 系统服务
### 4.6.1. 压缩与解压
+ `zip/unzip`：文件后缀为`.zip`
    ```shell
    # 压缩
    zip 123.zip *.txt
    # 解压
    unzip 123.zip
    ```
+ `gzip/gunzip`：文件后缀为`.gz`
    ```shell
    # 压缩，会生成1.txt.gz压缩文件
    gzip 1.txt
    # 解压
    gunzip 1.txt.gz
    gzip -d 1.txt.gz
    ```
+ `bzip2/bunzip2`：文件后缀为`.bz2`
    ```shell
    # 压缩，会生成1.txt.bz2压缩文件
    bzip2 1.txt			
    # 解压，添加'-k'选项可以保留压缩包
    bunzip2 1.txt.bz2	
    bzip2 -d 1.txt.bz2
    ```
+ `tar`：打包解包工具，后缀为`.tar`
  	- `-c`：创建新文件
  	- `-x`：解包
  	- `-t`：查看(不解包)
  	    > 说明：以上三个选项不能同时使用
  	- `-f`：指定操作文件
  	- `-v`：显示相信信息
  	- `-z`：调用`gzip/gunzip`进行压缩解压
  	- `-j`：调用`bzip2/bunzip2`进行压缩解压
  	- `-C`：指定解压位置
  	- `--exclude`：排除指定文件
    - 示例：
        ```shell
        tar -cvf 12.tar 1.txt 2.txt			# 将1.txt，2.txt打包成12.tar
        tar -tf 12.tar						# 查看包内容
        tar -xvf 12.tar						# 解包12.tar文件
        tar -zcvf 12.tar.gz	12.tar			# 调用gzip进行压缩
        tar -jcvf 12.tar.bz2 12.tar			# 调用bzip2进行压缩
        tar -zcvf 12.tar.gz *.txt --exclude 3.txt	# 打包压缩除3.txt以外的所有txt文件
        tar -zxvf 12.tar.gz				# 解压
        tar -jxvf 12.tar.bz2			# 解压
        ```
        > 提示：`.tar.gz`可简写为`.tgz`；`.tar.bz2`可简写为`.tbz2`或`.tbz`
### 4.6.2. 网络服务

+ `ping`：检查网络连通性，`-c`选项指定发送测试包的次数

+ `ifconfig`：查看或设置网卡信息

+ `ifup`：启动网卡

+ `ifdown`：关闭网卡

+ `service networking start|stop|restart`：控制

### 4.6.3. 服务监测

+ `netstat`
    - 作用：查看网络端口占用情况
    - 使用：`netstat -tunpl`
+ `free`
    - 作用：查看内存使用情况
    - 使用：`free -h`，`-h`人性化查看大小
+ `w`
  - 作用：查看当前正在做的事情
+ `top`
  - 说明：`w`的详细信息，3`S`会刷新一次，`q`退出查看
  - 结果：
    ```
    第一行：与`w`相同
    第二行：任务信息
    第三行：`CPU`使用
    第四行：内存使用
    第五行：交换分区
    其他行：系统进程信息
    ```
### 4.6.4. 进程管理

+ `ps`
  - 作用：查看进行信息
  - 使用：
    - `ps -ef`
    - `ps aux`
    - 说明：经常在查询进程号的时候结合`grep`进行过滤
+ `kill`
    - 作用：杀死进程
    - 示例：`kill -9 PID`
    - 说明：强制杀死指定进程

### 4.6.5. 防火墙(`ufw`)

+ 说明：简单版本的防火墙，底层依赖于`iptables`

+ 安装：`sudo apt-get install ufw`

+ 查看状态：`sudo ufw status`

+ 开启/关闭：`sudo ufw enable|disable`

+ 默认允许/禁止：`sudo ufw default allow|deny`

+ 允许/禁止：`sudo ufw allow|deny port/服务`，如：`sudo ufw allow 5900`

+ 删除规则：`sudo ufw delete allow 5900`

### 4.6.6. 远程连接(`ssh:22`)

+ 说明：默认`ubuntu`是没有自带的`ssh`服务，需要手动安装

+ 安装：`sudo apt-get install openssh-server`

+ 控制：`sudo service ssh start|stop|restart`

+ 连接：`putty` | `xshell` 工具，类`unix`也可以是终端：`ssh user@host`

+ 设置`root`用户远程连接：修改`/etc/ssh/sshd_config`文件

  ```ini
  # PermitRootLogin prohibit-password
  PermitRootLogin yes
  ```
  > 修改完配置文件，需要重启服务：`sudo service ssh restart`

### 4.6.7. 软件安装

+ `apt-get`安装：无需考虑复杂的软件依赖关系
  - `install`：安装
  - `remove`：卸载
  - `update`：取回更新软件包的类表信息
  - `upgrade`：进行一次更新
+ `dpkg`安装：文件后缀为`.deb`，可能需要进行依赖包的安装
  - `-i`：安装
  - `-r`：卸载
  - `-l`：查看软件包信息
  - `-L`：查看软件安装目录
  - 示例：安装`wps`
    ```shell
    # 1.安装wps
    sudo dpkg -i wps-office_10.1.0.5672~a21_amd64.deb
    # 2.安装字体库
    unzip wps_symbol_fonts.zip
    # 将字体库移动到/usr/share/fonts目录
    sudo mv *.ttf *.TTF /usr/share/fonts
    ```
+ 源码安装：需要对源文件进行编译
  - 基本步骤：
    - 配置：`configure`
    - 编译：`make`
    - 安装：`make install`
  - 命令执行：
    - `cmd1; cmd2`			# 执行完cmd1后，执行cmd2，无论前面的命令成功与否
      `cmd1 || cmd2`	       # 先执行cmd1，cmd1执行失败才会执行cmd2
    - `cmd1 && cmd2`            # 先执行cmd1，执行成功后才执行cmd2
    - 示例：`make && make install`
  - 示例演示：安装`nginx`
    - 解压软件压缩包：`tar -zxvf nginx-1.13.7.tar.gz `
    - 进入解压的目录：`cd nginx-1.13.7 `
    - 编译前的配置：`./configure --prefix=/usr/local/nginx`
      - `--prefix`：配置安装目录
      - 配置出错多数是因为缺少先关的依赖库或者编译器
      - 如：`sudo apt-get install gcc libpcre3-dev zlib1g-dev`
    - 编译和安装：`make && make install`
      - 如果没有权限常见目录，切换到`root`用户
    - `nginx`介绍
      - `sbin/nginx`：可执行程序，进入`sbin`目录，启动：`./nginx`
      - `html`：默认站点目录
      - 测试：在浏览器中输入`localhost`，看到`welcome to nginx`即表示成功

### 4.6.8. 管道及`xargs`

+ `l`：将前面命令的输出作为后面命令的参数。如：`ls /bin | grep '^m'`

+ `xargs`：有些命令无法接收管道作为参数，可以通过`xargs`解决。如：`find -name 2.txt | xargs rm -rf`

### 4.6.9. 重定向

+ 标准输入(`stdin`)、标准输出(`stdout`)、标准错误(`stderr`)

+ 在`Linux`中，创建任意进程，系统会自动创建上面三个数据流及三个文件，其实就是三个文件

+ 三个文件的描述符分别是：0、1、2，都指向了终端

+ 重定向就是改变原来默认的表现位置

+ 演示：
    ```shell
    # 输出重定向，>会新建文件，若文件已存在会清空；>>会追加到文件末尾，若文件不存在则只创建
    ls > 1.txt
    ls >> 1.txt
    # 错误重定向，2>表示将标准错误重定向
    ls /xxx 2> 1.txt
    # 同时重定向输出和错误，&>将标准输出和错误重定向
    ls /xxx /home &> 1.txxt
    ```
# 5. 第五部分  `shell`编程

## 5.1. `shell`简介

+ 什么是`shell`？
  - 把在终端下可执行的命令保存到一个文件中，这个文件就是`shell`程序，也就做`shell`脚本。

+ `shell`的类型：
  - `ash`、`bash`、`ksh`、`sch`等
  - 查看默认`shell`使用`echo $SHELL`
  - `/etc/shell`文件中存放了当前系统中可用的`shell`
+ `shell`脚本的执行
  - 使用指定`shell`执行指定脚本：`bash hello.sh`，该文件可以没有可执行权限
  - 将`sehll`脚本文件作为可执行程序执行，必须添加可执行权限
    - 添加可执行权限，`sudo chmod +x hello.sh`
    - 在开头指定`shell`：`#!/bin/bash`，其他位置`#`表示注释
    - 执行脚本：
      - 在本目录：`./hello.sh`
      - 不在此目录：`/home/ubuntu/hello.sh`
## 5.2. `shell`变量
+ 定义变量：`name="xiaoming"`
+ 打印变量：`echo $name`或`echo ${name}`
+ 销毁变量：`unset name`
+ 声名常量：`readonly name="xiaoming"`
+ 注意事项：使用`=`，两边不能有空格

## 5.3. 变量类型

+ 本地变量：只适用于当前`shell`的变量
+ 环境变量：适用于整个系统，通常都是全大写的
  - 查看环境变量：`env`
  - 打印指定变量：`echo $PATH`
  - `PATH`：若想要你的脚本在哪里都可以使用，需要脚本庐江添加到`PATH`环境变量中
  - 修改：
    - 一次性：`export PATH=$PATH:/home/ubuntu`
    - 永久性：
      - 系统级别：`/ect/profile`
      - 用户级别：`~/.profile`、`~/.bashrc`、`~/.bash_profile`
      - 重新加载(立即生效)：`source file`或`.filename`

+ 位置变量
  - `$0`：表示脚本名
  - `$1 ~ $9`：表示传递给脚本的参数

+ 特殊变量
  - `$#`：传递给脚本或函数的参数个数
  - `$*`：传递给脚本或函数的所有参数
  - `$?`：上次命令执行情况，0表示正确，其他表示错误
  - `$@`：传递给脚本或函数的所有参数，被双引号`" "`包含时，与 $* 稍有不同
  - `$$`：当前`shell`进程`ID`
    ```shell
    #!/bin/bash
    echo "File Name: $0"
    echo "First Parameter : $1"
    echo "First Parameter : $2"
    echo "Quoted Values: $@"
    echo "Quoted Values: $*"
    echo "Total Number of Parameters : $#"
    # 运行结果如下：
    >>> ./var.sh Zara Ali
    File Name : ./test.sh
    First Parameter : Zara
    Second Parameter : Ali
    Quoted Values: Zara Ali
    Quoted Values: Zara Ali
    Total Number of Parameters : 2
    ```
+ 单双引号的区别
- 双引号：可以是除`$`、`'`、`\`、`"`之外的任意字符
- 单引号：其中的任意字符都不解析，都不会原样输出
    ```shell
    #!/bin/bash
    name="xiaoming"
    echo "hello $namehow are you"
    echo "hello ${name}how are you"
    echo 'hello ${name}how are you'
    # 运行结果
    >>> bash str.sh
    hello are you
    hello xiaominghow are you
    hello ${name}how are you
    ```
- 反引号：会将其中的内容作为命令执行
- 反斜杠：转义特定的字样，如：`&`、`*`、`|`、`?`、`^`、`$`

## 5.4. 字符串操作
+ 计算长度：`${#name}`
+ 提取字符：`${name:2:3}`，从下标为2的字符开始提取三个字符

## 5.5. 数组操作
+ 定义：`a=(1 2 3)`
+ 访问成员：`${a[0]}`
+ 长度：`${#a[@]}`
+ 所有元素：`${a[*]}`，使用`for-in`遍历需要提取元素

## 5.6. `seq`命令
+ 说明：生成连续的整数
+ 示例：`seq 1 10`，生成1~10的连续整数

## 5.7. `expr`命令
+ 说明：运算一个表达式
+ 示例：
    ```shell
    expr 1 + 2
    echo `expr 1 + 2` # 打印结果
    expr 3 \* 5  # 需要转义
    ```
## 5.8. 各种运算
+ `test`命令：成功为真，失败为假，测试结果通过`$?`检查，0表示真，1代表假
    ```shell
    #!/bin/bash
    if test 1 -lt 2
    then 
        echo "OK"
    fi
    # 或者可以使用下面的方式，then和if在一行时要使用;
    if test 1 -lt 2; then 
        echo "OK"
    fi
    ```
+ 数值比较
  - `-lt`：小于
  - `-lte`：小于等于
  - `-gt`：大于
  - `-gte`：大于等于
  - `-eq`：相等
  - `-ne`：不相等
    ```shell
    #!/bin/bash
    # []中前后都需要空格，then和if同行需要写分号;
    if [ 1 -lt 2 ]; then 
        echo "OK"
    fi
    ```

+ 字符串测试：
  - `=`：相等
  - `!=`：不相等
  - `-z`：字符串长度是否为0
  - `-n`：字符串长度是否不为0

+ 文件判断
  - `-f`：普通文件
  - `-d`： 目录文件
  - `-w`：文件存在，且可写
  - `-x`：文件存在，且可执行
  - `-s`：文件存在，且至少有一个字符
  - `-c`：字符设备文件
  - `-b`： 块设备文件

+ 逻辑运算
  - `-a`：逻辑与(`and`)，也可以使用`&&`进行转换
  - `-o`：逻辑或(`or`)，也可以使用`|`转换
  - `!`：逻辑非
    ```shell
    #!/bin/bash
    if [ 1 -lt 2 -a 2 -lt 3 ]; then 
        echo "OK"
    fi
    # 可以转化为&&
    if [ 1 -lt 2 ] && [ 2 -lt 3 ]; then 
        echo "OK"
    fi
    # 逻辑非
    if [ ! 3 -lt 2 ]; then 
        echo "OK"
    fi
    ```
## 5.9. 分支结构

+ `if-else`：
    ```shell
    #!/bin/bash
    if [ 1 gt 2 ]; then
        echo "大于"
    elif [ l lt 2 ]; then
        echo "小于"
    else
        echo "等于"
    fi
    ```
+ `case`：
    ```shell
    #!/bin/bash
    # 从终端获取内容，-p后的字符串是提示字符
    read -p 'press any key: ' ch
    case $ch in
        [a-z])
            echo "alpha"
        ;;
        [0-9])
            echo "numberic"
        ;;	
        *)
            echo "other"
        ;;
    esac
    ```
## 5.10. 循环结构
+ `for-in`
    ```shell
    #!/bin/bash
    # 遍历字符串数组
    for x in a b c
    do
        echo $x
    done
    # 遍历目录
    for x in /etc/*
    do
        echo $x
    done
    # 遍历1~10的整数，反引号表示执行
    for x in `seq 1 10`
    do
        echo $x
    done
    # 计算1+2+3+...+100
    for i in `seq 1 100`
    do
        let j+=$i
    done
    echo $j
    # 遍历数组
    a=(1 6 3)
    for x in ${a[*]}
    do
        echo $x
    done
    ```
+ `for`
    ```shell
    #!/bin/bash
    # 遍历1~10的整数
    for ((i=0;i<=10;i++))
    do
        echo $i
    done
    # 遍历数组
    a=(2 5 6)
    for ((i=0;i<=${#a[@]};i++))
    do
        echo ${a[$i]}
    done
    ```
+ `while`
    ```shell
    #!/bin/bash
    i=1
    sum=0
    # while (($i<=10))
    while [ $i -le 10 ]
    do
        echo $i
        # ((i++))
        # let i++
        # let i+=1
        i=$[$i+1]
        
        ((sum+=$i))
        # let sum+=$i
        # sum=$[$sum+$i]
    done
    echo $sum
    ```
+ `until`：条件与`while`相反
    ```shell
    #!/bin/bash
    i=1
    until [ $i -gt 10 ]
    do
        echo $i
        ((i++))
    done
    ```
+ `break`、`continue`的使用

## 5.11. 函数使用
    ```shell
    demo()
    {
        echo "call demo func"
    }

    demo
    # $1,$2接收传递的实参，$?就代表函数的返回值
    arg()
    {
        echo $1
        echo $2
        echo $#
        echo $*
        return $?
    }
    arg 1 2 
    ```
# 6. 第六部分  Python-Flask框架

# 7. 第七部分  Python-Django框架

# 8. 第八部分  Python-Tornado框架

# 9. 第九部分  Python爬虫基础

# 10. 第十部分  Python-Scrapy与分布式爬虫
