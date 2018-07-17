# 第三方库安装：

* 1.自动下载安装
```
\>> pip install libname
```

* 2.自主下载安装
```
\>> python setup.py install
```

* 3.资源大全

> [GitHub_Python资源大全](https://github.com/jobbole/awesome-python-cn)

# IDLE快捷键

| Ctrl+] | 缩进代码 |
| ------ | -------- |
| Ctrl+[ | 取消缩进 |
| Alt+3  | 注释代码 |
| Alt+4  | 去除注释 |
| F5     | 运行     |

# 数据类型

* 1、字符串
```
         ‘string’， “string1”，
         '''string2''', """string3"""
         # 四种等效
```
* 2、类型转换

```
        int(23.6)  # 浮点数转整数
        int("23")  # 字符串转整形
        float(23)  # 整形变浮点型
        float('23')  # 字符串转浮点型
        str(23)  # 整形转字符串
        str(23.6)  # 浮点型转字符串
        ord('a')  # 将'a'字符转换成ASCII码
        chr(97)  # 将97字符转换成ASCII码对应的字符

#注;字符串转整形要求字符串内容为整数
```
* 3、列表

```
        list[] #空列表
            []  #空列表
        list = ['a', 1, 2, "aaa"]

```
* 4、元组
```
    # 元组是一种特殊的列表，元组一旦定义就不允许修改
       tuple=('a',1,2,"aaa")
```
* 5、字典

```
     adct={'a':1,'b':2,'c':3}//访问adct['a']

      # 遍历字典：
     for key,value in adct.items():
          #key,value对应for后的定义，可自设任意标识
          print(key,':',value)


    for k in adct.keys():
          print(k)

    for v in adct.values():
          print(v)
```
# 时间调用

* 标准库有：

```
      calendar、datetime、time
```
* 调用：

```
    time.time()
    datetime.datetime.now()# 获取当地时间
    datetime.datetime.utcnow()#获取世界协调时间
```

# Class1 2018/7/17
```
"""
Python内部存在四种基本数据类型：
    整型
    浮点
    字符串（单双引号包含的内容）
    布尔类型（ture or flase）

弱类型变量：根据数据的变化而变化的变量
python中变量是一种弱类型的变量的变量，
没有严格的类型限制，变量的类型完全根据变量中存储的数据的实际类型的变量。

变量的定义语法：
    变量名 = 变量值

变量命名规范：
    1、变量只能有字母、数字、下划线等且数字不能开头
    2、变量名不能是系统预留字段
    3、变量名最好能见名知意
    4、小驼峰结构: className = "ZZ14"
"""
```

```
age = 22
name = 'LEIF LIU'  # name, age = "LEIF LIU", 22
```
```
"""
算术运算符（+,-,*,/,%,//,**）:
// :地板除向下取整
** :幂指数
'+' :除了做算术运算外还可以做字符串拼接（左右必须都是字符串）
"""
num1, num2 = 10.5, 20
print(num1 + num2)
print(num1 // num2)   # 向下取整，直接舍弃小数部分
print(num1 % num2)
print(num1 ** 2)  # 幂指数num1^2

# 字符串拼接
str1, str2 = "Hello ", "Lanou "
print(str1 + str2)
```
```
"""
复合运算符: +=,-=,/=,*=,//=,**=,%=
左右数值先进行算术运算之后赋值给左边的数值
"""
num1 += num2
print(num1)  # 复合运算不能直接打印
```
```
"""
位运算符： &按位与,|按位或，^按位异或，~按位取反，
<<左移（移一位*2），>>右移（移一位/2，正数向下取整，负数数值向上取整）
"""
```
```
"""
进制计算：
十进制转n进制，连续除反取余
n进制转十进制，按位计算求和
"""
num1, num2 = 3, 4
print("\n")
print(num1 & num2)
print(num1 | num2)
print(num1 ^ num2)
print(num1 << 1)
print(num1 >> 1)  # 除以2，整数向下取整
print(-num1 >> 1)  # 除以2，负数向上取整
```
```
"""
位运算符测试题
"""
# 奇数或偶数检测，不用运算符，使用位运算符（&）num & 1
print("是否是偶数：", num1 & 1)

# 计算n是否是2的整数次幂
num = 32
num1 = num - 1
print("是否是2的整数次幂：", num & num1)
```
```
"""
负数的存储（补码）:
    1、求原码
    2、求反码
    3、末尾加1
    4、添加符号位（注意数据类型的字节数）
注意：~n 等价于 -n-1  (~按位取反)
"""
print("~n 等价于 -n-1:(~59)", ~59)
```
```
"""
格式化输入输出：
    input(tip): tip为提示字符串，允许用户输入数据，都会当成字符串处理
    整型输入： int(input("输入整型数"))
    小数输入： float(input("输入小数"))

    print("占位符%f"% flo): 占位符‘%’，%d,%s,%f
    注意：以'%'分隔而不是','
"""

num = input("Please input a num:")  # 输入被当成字符串处理
# print(num + 1)
print(int(num) + 1)  # 强制转换，适用于整型输入（不支持字符和小数）
print("num2=%d" % num2)
```
