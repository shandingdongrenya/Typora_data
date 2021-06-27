# BIF 内置函数

## help()

```py
help(print)
```

实参为BIF的函数名,由help函数可获得BIF函数得使用方法

## print()

```py
print("string" * 8)
print(5 * 8)
print("string" "string")
```

将括号内的东西打印到屏幕上

可以重复打印,直接输出数据甚至进行运算后的数据,拼接两段字符串

一个print()打印得内容默认占据一行

## input()

```py
A = input("请输入A")
```

- 由用户给A赋值,实参为给用户得提示

## int()

```py
int(A)
a = 5.99
c = int(a)		#c == 5
b = "小甲鱼"	  #报错
```

- 将实参转化为整型数据

## 例程

```py
print("--------------dididididididididi----------------")
temp = input("不妨猜一下小甲鱼现在想的是哪个数字:\n")
guess = int(temp)
if guess == 8:
	print("卧槽, 你是小甲鱼心里的蛔虫吗?")
	print("很,猜中了也没用")
else:
	print("猜错啦,小甲鱼想的是8")
print("游戏结束,不玩啦^_^")
```

- python中加了冒号自动缩进

## float()

将数据类型转化为浮点型

```py
a = 520
b = float(a)			#b == 520.0
a = "520"
b = float(a)			#b == 520.0	
```

## str()

将数据类型转化为字符串类型

```py
a = 5.99
b = str(a)			#b == "5.99"
c = 1.5e4
b = str(c)			#b == "1.5e+4"
```

## type()

询问数据类型

```py
type("520") == <class 'str'>
type(5.2) == <class 'float'>
type(ture) == <class 'bool'>
type(5e15) == <class 'float'>
```

## isinstance()

```py
#判断数据类型是否为想要的数据类型
a = "小甲鱼"
isinstance(a, str) == ture
isinstance(a, int) == false
isinstance(320, int) == ture
isinstance(320, float) == false
isinstance(320.25, float) == ture
```

isinstance(数据, 数据类型),返回是否相匹配,类型匹配返回ture,否则返回0

# 语法



## "+" (字符串的拼接)

```py
str1 = "string1"
str2 = "string2"
str3 = str1 + str2
```

"+"拼接两个字符串

## 反斜杠

### 引号

当字符串中出现引号时,使用转义字符进行修饰

```py
str = "Let's go!" #错误
str = "Let\'s go!"
```

### 反斜杠\

当字符串中出现反斜杠时,使用反斜杠对其进行转义

```py
str = "C:\now"		#\n出现歧义
str = "C:\\now"		
```

## 原始字符串

在字符串前添加一个r表达原始字符串,此时不必担心字符串中出现歧义,程序自动在需要转义得符号添加转义字符反斜杠

- 原始字符串得最后不可以加反斜杠
- 如果非要加,可以分成两个字符串拼接

```py
str = r"C:\now" + "\\"
```

	## 三重引号

给字符串自动添加换行符

```py
str = """哇哎小甲鱼
咕叽咕叽咕氧化剂
咕唧咕唧咕唧
古籍古hi咕叽咕叽
咕叽咕叽咕叽咕"""
```

## 科学计数法e

```py
150000 == 1.5e5
```

## true 与 false

```py
true == 1
false == 0
```

# 算术操作符

## 优先级

幂运算 > 正负号 > 算术操作符 > 比较操作符 > 逻辑运算符

从左到右依次进行

### 4则运算中,先乘除后加减

```py
* == / > + == -
```

## += & -= & *= &  /=

```py
a = a+3 # 等价于 a += 3
a = a-1 # 等价于 a -= 1
a = a*3 # 等价于 a *= 3
a = a/3 # 等价于 a /= 3
```

## /与//

整型//整型 == 整型	地板除法

```py
#6//5 == 1
#6//3 == 2
```

整型/整型 == 浮点型 真实除法

```py
#6/5 == 1.2
#6/3 == 2
```

## 取余%

```py
#5%2 == 1
```

## 幂运算**

```py
# 3 ** 2 == 9
# 3 ** 5 == 3*3*3*3*3
```

幂运算比它左边的优先级高,比右边的优先级低

# 逻辑操作符

## and 且

```py
3 < 4 < 5 	#	等价于 (3<4) and (4<5)
```

## or 或

## not 非

# 关键字

## while循环

```py
while 条件:
	循环体
```

# 模块

## random

```py
import random
```



###  randint()

```py
secrect = random.randint(1,10)
# 1-10之间得随机整型
```



## 

