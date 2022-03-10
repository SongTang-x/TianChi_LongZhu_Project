# 学习笔记  

Day 1

按位取反操作结论：~n = -(n+1)  

is, is not 对比的是两个变量的内存地址，==, != 对比的是两个变量的值  

比较的两个变量，指向的都是地址不可变的类型（str等），那么is，is not 和 ==，！= 是完全等价的  

对比的两个变量，指向的是地址可变的类型（list，dict，tuple等），则两者是有区别的  

Python 变量名是大小写敏感的  

当把布尔型变量用在数字运算中，用 1 和 0 代表 True 和 False  

type() 不会认为子类是一种父类类型，不考虑继承关系  

isinstance() 会认为子类是一种父类类型，考虑继承关系  

Python中bin一个负数（十进制表示），输出的是它的原码的二进制表示加上个负号

Day2

使用多个except代码块时，必须坚持对其规范排序，要从最具针对性的异常到最通用的异常

一个 except 子句可以同时处理多个异常，这些异常将被放在一个括号里成为一个元组

列表是有序集合，没有固定大小，能够保存任意数量任意类型的 Python 对象

由于list的元素可以是任何对象，因此列表中所保存的是对象的指针。即使保存一个简单的[1,2,3]，也有3个指针和3个整数对象

x = [a] * 4操作中，只是创建4个指向list的引用，所以一旦a改变，x中4个a也会随之改变

Day 3

remove 和 pop 都可以删除元素，前者是指定具体要删除的元素，后者是指定一个索引

如果你要从列表中删除一个元素，且不再以任何方式使用它，就使用del语句；如果你要在删除元素后还能继续使用它，就使用方法pop()

把 step 设为 -1，相当于将列表反向排列,切片的第三位是step

list1 = [[123, 456], [789, 213]]
list2 = list1   深复制
list3 = list1[:]  外列表是浅复制，内列表是深复制

「等号 ==」，只有成员、成员位置都相同时才返回True

reverse = True 降序， reverse = False 升序（默认）

方法里面可以嵌套函数

元组与列表类似，也用整数来对它进行索引 (indexing) 和切片 (slicing)

创建元组可以用小括号 ()，也可以什么都不用，元组中只包含一个元素时，需要在元素后面添加逗号，否则括号会被当作运算符使用

元组有不可更改 (immutable) 的性质，因此不能直接给元组的元素赋值，但是只要元组中的元素可更改 (mutable)，那么我们可以直接更改其元素

元组大小和内容都不可更改，因此只有 count 和 index 两种方法

解压（unpack）一维元组（有几个元素左边括号定义几个变量）
解压二维元组（按照元组里的元组结构来定义变量）
如果你只想要元组其中几个元素，用通配符「*」
如果你根本不在乎 rest 变量，那么就用通配符「*」加上下划线「_」

Day 4

三引号允许一个字符串跨多行，字符串中可以包含换行符、制表符以及其他特殊字符

最后一个元素的位置编号是 -1

swapcase() 将字符串中大写转换为小写，小写转换为大写

endswith(suffix, beg=0, end=len(string)) 检查字符串是否以指定子字符串 suffix 结束，如果是，返回 True，否则返回 False。如果 beg 和 end 指定值，则在指定范围内检查

startswith(substr, beg=0,end=len(string)) 检查字符串是否以指定子字符串 substr 开头，如果是，返回 True，否则返回 False。如果 beg 和 end 指定值，则在指定范围内检查

rfind(str, beg=0,end=len(string)) 类似于 find() 函数，不过是从右边开始查找

partition(sub) 找到子字符串sub，把字符串分为一个三元组(pre_sub,sub,fol_sub)，如果字符串中不包含sub则返回('原字符串','',''),rpartition(sub)类似于partition()方法，不过是从右边开始查找

先maketrans再translate

'{0:.2f}{1}'.format(27.658, 'GB')  # 保留小数点后两位，位置参数要在关键字参数之前

字典以"关键字"为索引，关键字可以是任意不可变类型，通常用字符串或数值

字典是 Python 唯一的一个 映射类型，字符串、元组、列表属于序列类型

用 hash(X)，只要不报错，证明 X 可被哈希，即不可变，反过来不可被哈希，即可变

用 id(X) 函数，对 X 进行某种操作，比较操作前后的 id，如果不一样，则 X 不可变，如果一样，则 X 可变

多次对一个key放入 value，后面的值会把前面的值冲掉

dict.popitem()随机返回并删除字典中的一对键和值

集合的两个特点：无序 (unordered) 和唯一 (unique)

不可以为集合创建索引或执行切片(slice)操作，也没有键(keys)可用来获取集合中元素的值，但是可以判断一个元素是否在集合中

set.remove(item) 用于移除集合中的指定元素。如果元素不存在，则会发生错误，而 discard() 方法不会

set.pop() 用于随机移除一个元素

set.intersection(set1, set2) 、set1 & set2、set.intersection_update(set1, set2)返回两个集合的交集

set.union(set1, set2)、set1 | set2返回两个集合的并集

set.difference(set)、set1 - set2 、set.difference_update(set) 返回集合的差集

set.symmetric_difference(set)、set1 ^ set2 返回集合的异或、set.symmetric_difference_update(set)返回集合的异或

set.issubset(set)、set1 <= set2判断集合是不是被其他集合包含

frozenset([iterable]) 返回一个冻结的集合，冻结后集合不能再添加或删除任何元素



