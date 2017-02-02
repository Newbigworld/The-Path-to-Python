# ***The-Path-to-Python***
==========
**Python 基本数据类型**
________
# ***一、运算符***

## 1、 算术运算符
加减： + 、- ;
乘除： * 、/ ;
乘方：*** ;
求余：% ;
整除：// ;

## 2、 比较运算符
==、!=或<>、>、<、>=、<=
## 3、赋值运算符
=、+=、-=、\*=、/=、%=、\**=、//=
## 4、逻辑运算符
and、or、not
## 5、字符运算符
* 原始字符串操作符（r/R）-用于一些不希望转意字符串起左右的地方

        >>> f= open(r'D:\Python\Hello Kitty.py','w')
        >
        >>> f= open('D:\\Python\\Hello Kitty.py','w')
        >
        >>> f.close()
* Unicode字符串操作符(u/U)-转换成Unicode字符串


## 6、成员运算符
in、not in

# ***二、基本数据类型***
## 1、整型(int)
在32位机器上，整数的位数为32位，取值范围为-2**31～2**31-1，即-2147483648～2147483647
在64位系统上，整数的位数为64位，取值范围为-2**63～2**63-1，即-9223372036854775808～9223372036854775807

## 2、浮点型(Float)

## 3、复数型（complex）

    >>> x = 2.3 + 4.3j
    >>> x.imag
    4.3
    >>> x.real
    2.3
    >>> x.conjugate()
    (2.3-4.3j)


## 4、布尔类型（bool）
True  除0以外的任何值都表示Ture
False 0值表示为False

## 5、字符串(str)
### 1)可以用索引和切片、字符串长度
### 2）字符串功能如下：
        >>> dir(str)
        ['__add__', '__class__', '__contains__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getnewargs__', '__gt__', '__hash__', '__init__', '__iter__', '__le__', '__len__', '__lt__', '__mod__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__rmod__', '__rmul__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', 'capitalize', 'casefold', 'center', 'count', 'encode', 'endswith', 'expandtabs', 'find', 'format', 'format_map', 'index', 'isalnum', 'isalpha', 'isdecimal', 'isdigit', 'isidentifier', 'islower', 'isnumeric', 'isprintable', 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip', 'maketrans', 'partition', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill']

## 6、 元组（tuple）

元组与列表基本一样，区别是列表可以支持增删改查，而元组不支持增删改

- 创建元组

    Name_list = （'He', 'Liu', 'Li', 'Zhang'）

- 基本操作
    - 索引
    - 切片
    - 长度
    - 循环
- 列表基本操作方法
        >>> dir(tuple)
        ['__add__', '__class__', '__contains__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getnewargs__', '__gt__', '__hash__', '__init__', '__iter__', '__le__', '__len__', '__lt__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__rmul__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', 'count', 'index']

## 7、 列表（List）

- 创建列表

        Name_list = ['He', 'Liu', 'Li', 'Zhang']

- 基本操作
    - 索引

            print(Name_list[0])          # 返回He

    - 切片

            print(Name_list[0：2])       # 返回['He', 'Liu']

    - 长度

            len(Name_list)

    - 循环

            for i in Name_list:
                print(i)

- 列表基本操作方法

        >>> dir(list)
        ['__add__', '__class__', '__contains__', '__delattr__', '__delitem__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__gt__', '__hash__', '__iadd__', '__imul__', '__init__', '__iter__', '__le__', '__len__', '__lt__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__rmul__', '__setattr__', '__setitem__', '__sizeof__', '__str__', '__subclasshook__', 'append', 'clear', 'copy', 'count', 'extend', 'index', 'insert', 'pop', 'remove', 'reverse', 'sort']


## 8、 字典（Dict）

- 创建字典

        Person = {'Name': 'Yan Liu', 'Age': 31}

- 基本操作
    - 索引

            print(Person['Name'])          # 返回'Yan Liu'

    - 键、值、键值对
            Person.keys()
            Person.values()
            Person.items()
    - 新增
            >>> Person.update([('Height', 1.8)])
            >>> Person
            {'Name': 'Yan Liu', 'Height': 1.8, 'Age': 31}
    - 删除
            >>> Person
            {'Name': 'Yan Liu', 'Height': 1.8, 'Age': 31}
            >>> Person.pop('Height')
            1.8
            >>> Person
            {'Name': 'Yan Liu', 'Age': 31}
            >>> Person.popitem()
            ('Name', 'Yan Liu')
            >>> Person
            {'Age': 31}
    - 长度
            >>> Person
            {'Age': 31}
            >>> len(Person)
            1

    - 循环

***迭代中常用函数： range()、  enumerate()***
========

        # enumerate()
        li = ['zhao','qian','sun','li']
        for key, value in enumerate(li):
            print(key, value)

        # range()
        li = ['zhao','qian','sun','li']
        for i in range(0,len(li)):
            print(li[i])

- 字典基本操作方法
        >>> dir(dict)
        ['__class__', '__contains__', '__delattr__', '__delitem__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__gt__', '__hash__', '__init__', '__iter__', '__le__', '__len__', '__lt__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__setitem__', '__sizeof__', '__str__', '__subclasshook__', 'clear', 'copy', 'fromkeys', 'get', 'items', 'keys', 'pop', 'popitem', 'setdefault', 'update', 'values']

## 9、集合（set）
