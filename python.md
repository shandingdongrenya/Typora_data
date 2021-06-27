# python笔记

## 运算符

### 算数运算符

#### 标准运算符

> + ==+==		==-==		==*==		==/== 
> + 加减乘除
> + ==//== 整除运算

#### 取余运算符

> + ==%==
> + 取余运算

#### 幂运算符

> + ==**==
> + 幂运算

#### 例程

```py
#同正同负取整数部分
print(9//4)	#2
print(9//4)	#2

#一正一负向下取整
print(9//-4)	#-3
print(-9//4)	#-3

#一正一负套公式
#余数 = 被除数 - 除数*商
print(9%-4)	#-3
print(-9%4)	#3
```

### 赋值运算符

> + =====		赋值运算
> + 执行顺序: 从右到左

#### 支持链式赋值

```py
a=b=c=20
```

#### 参数赋值

```py
a+=20 #a=a+20
a-=20 #a=a-20
a*=20 #a=a*20
a/=20 #a=a/20
a//=20 #a=a//20
a%=20 #a=a%20
```

#### 支持系列解包赋值

```py
a,b,c = 20,30,40

#交换两个变量的值
a,b = b,a
```

### 比较运算符

> + 返回布尔类型

#### 比较变量的值

```py
a>b
a<b
a<=b
a>=b
a==b
a!=b
```

#### 比较变量的标识

> a is not b	#标识是否不相等
> a is b #标识是否相等

```py
a=10
b=10
a==b	#值相等
a is b 	#标识相同

lst1=[11,22,33]
lst2=[11,22,33]
lst1 == lst2	#value相等
lst1 is lst2	#id不同
```

### 布尔运算符

> ==and==	且&&
>
> ==or==		或||
>
> ==not==	非!
>
> ==in==		包含
>
> ==not in==	不包含

```py
s = 'hello world'
'w' in s	#true
'k' in s	#false
'w' not in s	#false
'k' not in s	#true
```

### 位运算符

> ==&==	按位且
>
> ==|==	按位或
>
> ==<<==	左移位
>
> ==>>==	右移位

### 运算符的优先级

<img src="D:\tools\Typora\Typora_data\inmages\image-20210627114354124.png" alt="image-20210627114354124" style="zoom: 50%;" />

## 程序结构

### 顺序结构

#### bool()内置函数

> ==空列表==
>
> ==空元组==
>
> ==空字典==
>
> ==空集合==
>
> ==false==
>
> ==数值0==
>
> ==none==
>
> 以上对象的bool值为false

### 选择结构

#### 单分支结构

> 如果.....就

```py
money=1000
s=int(input("请输入取款金额"))
if money>=s:
	money-=s
	print("取款成功,余额为:",money)
```

#### 双分支结构

> 如果...就...
>
> 不然就...

```py
num = int(input("请输入一个整数"))

if num%2 == 0:
	print(num,"是整数")
else
	print(num,"是奇数")
```

#### 多分支结构

> 如果...就...
>
> 其他如果...就...
>
> 其他如果...就...
>
> 其他如果...就...
>
> 其他如果...就...
>
> 否则就...	(可以不写)

```py
score = int(input("输入一个整数"))

if score>=90 and score<=100:
	print('A')
elif score>=80 and score<90:
	print('B')
elif score>=70 and score<80:
	print("C")
elif score>=60 and score<70:
	print("D")
elif score>=0 and score<60:
	print("E")
else:
	print("error")
```

#### 嵌套if

```py
if a>b:
	if a>c:
		print("hh")
	elif a==c:
		print('jj')
	else:
		print("pa")
elif a==b:
	pass
else:
	pass
```

#### 简写

```py
x if x>y else y
```

#### pass占位符

```py
if x==y:
	pass
else:
	pass
```

### 循环结构

#### range()函数

