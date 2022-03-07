# -
学习笔记  

按位取反操作结论：~n = -(n+1)  

is, is not 对比的是两个变量的内存地址，==, != 对比的是两个变量的值  

比较的两个变量，指向的都是地址不可变的类型（str等），那么is，is not 和 ==，！= 是完全等价的  

对比的两个变量，指向的是地址可变的类型（list，dict，tuple等），则两者是有区别的  

Python 变量名是大小写敏感的  

当把布尔型变量用在数字运算中，用 1 和 0 代表 True 和 False  

type() 不会认为子类是一种父类类型，不考虑继承关系  

isinstance() 会认为子类是一种父类类型，考虑继承关系  

Python中bin一个负数（十进制表示），输出的是它的原码的二进制表示加上个负号
