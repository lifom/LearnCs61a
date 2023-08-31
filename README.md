# LearnCs61a
Write some notes and learning
## 学习的版本为:cs61a su20 
link:https://inst.eecs.berkeley.edu/~cs61a/su20/

最近写代码发现,很多时候最基本的语法很不标准,代码规范很差,需要debug很多次才可以实现目标,因此完完整整的更一遍自己学习cs61a时的记录


### Learn week1
#### 2023.8.20 update Lab0 HW1
##### Floating point division (/) 浮点除法 和 Floor division (//) 向下整除法

<div align=center><img src="https://s1.ax1x.com/2023/08/20/pP87MjJ.md.png" width="50%" height="50%"></div>

<div align=center><img src="https://s1.ax1x.com/2023/08/20/pP873H1.md.png" width="50%" height="50%"></div>

<div align=center><img src="https://s1.ax1x.com/2023/08/20/pP871BR.md.png" width="50%" height="50%"></div>

##### python使用技巧

```
Python -i ex.py
```

就进入了交互模式

```
python -m doctest ex.py
```

运行文档测试例如:

<img src="https://picgoimage-1304379529.cos.ap-beijing.myqcloud.com/202308310932869.png" alt="CleanShot 2023-08-22 at 19.43.53@2x" style="zoom: 25%;" />

##### assert 用法

`assert` 的语法如下：

```python
assert <条件表达式>, <错误信息表达式>
```

当 `<条件表达式>` 为假时，`assert` 会引发 `AssertionError` 异常，并将 `<错误信息表达式>` 的值作为异常的错误消息。如果 `<条件表达式>` 为真，则程序继续执行，没有任何影响。

```
def divide(a, b):
    assert b != 0, "除数不能为零"
    return a / b

result = divide(10, 2)
print(result)  # 输出: 5.0

result = divide(10, 0)  # 触发 AssertionError 异常
```

##### 函数定义直接带参数

def func(n,d=10)

##### lambda 函数

```
lambda 参数: 表达式
square = lambda x: x**2
result = square(5)
print(result)  # 输出: 25
```

##### Print and None

一个没有return 的函数 将会返回一个 None

<img src="https://picgoimage-1304379529.cos.ap-beijing.myqcloud.com/202308311022082.png" alt="CleanShot 2023-08-22 at 01.26.16@2x" style="zoom: 25%;" />

None 可以

1.print出来

2.作为一个值绑定到右边的键

3.虽然可以被绑定但不能直接print出来



```
>>>print(print(1,)print(2))
1
2
None None
```

图像化展示:

<img src="https://picgoimage-1304379529.cos.ap-beijing.myqcloud.com/202308311027678.png" alt="CleanShot 2023-08-22 at 01.31.19@2x" style="zoom:25%;" />

##### 纯函数(Pure Function)和非纯函数(None)



<img src="https://picgoimage-1304379529.cos.ap-beijing.myqcloud.com/202308311024737.png" alt="CleanShot 2023-08-22 at 01.28.37@2x" style="zoom:25%;" />

纯函数(pure funciton)  就是只返回一个值的函数 不能有其他副作用(side effetct)

非纯函数(None function) 可能有返回的值 并且包含副作用

##### Boole ! George Boole

False 值并不单单指的是 False 还可以是 0 ,None ...

Ture 的值并不是仅仅指 Ture 还可以是 除了False 的任何值  

```
while 3:
	print()
这个循环就会一直进行
```

##### 函数的设计思想

有且仅有一个job

就像每个插座只对应一种插座类型

<img src="https://picgoimage-1304379529.cos.ap-beijing.myqcloud.com/202308311034682.png" alt="CleanShot 2023-08-23 at 18.17.06@2x" style="zoom:25%;" />

##### Higher Function

一个函数的就过就是返回另一个函数(🪆)

<img src="https://picgoimage-1304379529.cos.ap-beijing.myqcloud.com/202308311038422.png" alt="CleanShot 2023-08-30 at 14.17.45@2x" style="zoom:25%;" />



<img src="https://picgoimage-1304379529.cos.ap-beijing.myqcloud.com/202308311038304.png" alt="CleanShot 2023-08-30 at 14.31.56@2x" style="zoom:25%;" />

```
>>>make_adder(200)(1)
201
step1:
	200作为参数赋值给n 传递进去 maker_adder函数执行
step2:
	1作为参数赋值给k,传递给maker_adder中的adder
```

![CleanShot 2023-08-31 at 10.47.08](https://picgoimage-1304379529.cos.ap-beijing.myqcloud.com/202308311048541.gif)






