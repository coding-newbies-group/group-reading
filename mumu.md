# 1 起步

## 1.1 编程环境简介

安装了3.9或更高版本的Python就可以运行本书的所有代码。

> 有的人电脑已经安装了Python，如何查看安装的Python的版本？
>
> 开始——运行——powershell——python
>
> 可以看到，下图Python版本为3.11.2
>
> ![image-20230703105431876](https://raw.githubusercontent.com/vwumumu/images/master/image-20230703105431876.png)

## 1.2 在各种操作系统中搭建Python编程环境

- 安装Python注意勾选“Add Python 3.11 to PATH”



## 1.3 运行Hello World程序

![image-20230703105918966](https://raw.githubusercontent.com/vwumumu/images/master/image-20230703105918966.png)

编辑完，请注意保存代码。可以选择在VSCode的File菜单中勾选自动保存。

## 1.4 排除安装问题

## 1.5 从终端运行Python程序



> 什么是终端？
>
> 终端我们可以简单理解为命令行工具，即非图形化的，比如Windows的CMD，PowerShell，苹果系统的Terminal，Linux系统的Bash Shell等。



进入PowerShell

```
cd ~\desktop\python_work
python hello_world.py
```

> .\hello_workld.py 和 hello_world.py对此场景没有区别，.\表示当前目录下，也就是python_work目录下。

![image-20230703110222173](https://raw.githubusercontent.com/vwumumu/images/master/image-20230703110222173.png)

# 2 变量和简单的数据类型

## 2.1 运行hello_world.py时发生的情况

## 2.2 变量

注意，比较下面使用引号的区别：

```python
print("Hello World")
```

```python
message = "Hello World"
print(message)
```

如果打印的是文字，文字包含在引号中；

如果打印的是变量所代表的的文字，变量没有包含在引号中。



关于变量名命名规范，实际上，如果是不规范的，VSCode会有红色波浪线的提示（如下截图），如果强行运行，报错如下：

![](https://raw.githubusercontent.com/vwumumu/images/master/20230703163039.png)

## 2.3 字符串

> name = "ada lovelace"
>
> print(name.title())

上面是书中的范例代码，如果不太好理解print(name.title())

可以试着理解下面的代码：

```python
name = "ada lovelace"
name = name.title()
print(name)
```



lower()方法很有用。把数据全部转换成小写保存，用的时候根据需要再转换为首字母大写或全大写。



f 字符串，有的地方会看到叫f-string，string翻译过来也是字符串。非常常用和重要的。



制表符（\t）通常就是按tab键的效果。



" python" 和 "python"是不同的，前面的python的p前面有一个空格，要对空格敏感，对计算机而言，空也是一种东西，虽然，对人而言，看上去好像空是不存在的。



## 练习2.3-2.8

```python
# 练习2.3
name = "Eric"
msg = f"Hello {name}, would you like to learn some Python today?"
print(msg)

# 练习2.4
print("=======================================")
print(name.lower())
print(name.upper())
print(name.capitalize())

# 练习2.5
print("=======================================")
print('Albert Einstein once said, "A person who never made a mistake never tried anything new."')

# 练习2.6
print("=======================================")
famous_person = "Albert Einstein"
msg2 = f'{famous_person} once said, "A person who never made a mistake never tried anything new."'
print(msg2)

# 练习2.7
print("=======================================")
name2 = " Mumu \t Wu \n "
name3 = "Mumu \t Wu"
print(name2.strip())
print(name2.lstrip())
print(name2.rstrip())
print(len(name2.strip()))
print(len(name3.strip()))

# 练习2.8
print("=======================================")
filename = "python_notes.txt"
print(filename.removesuffix(".txt"))
```

练习2.7，为了验证删除空白的效果，我创建了name3作为对照，len()函数用于获取结果的长度，发现长度是一致的，所以，对于删除空白，name3的内容等价于name2删除空白后的结果。

![](https://raw.githubusercontent.com/vwumumu/images/master/20230705082719.png)



## 2.4 数

任意两个数相除，结果总是浮点数，即使这两个数是整数且能整除。



程序中变量是允许再次被赋值的，不能再赋值的变量称为常量，Python中没有内置的常量类型，以全大写字母当做常量。

其他语言，比如JavaScript是有变量常量的：

```js
let a = 1  //用let表明a是一个变量
const b = 2 //用const表明b是一个常量
```



## 2.5 注释

在VSCode中，Ctrl + /可以将光标所在行快速的注释和取消注释。



## 2.6 Python之禅

输入`exit()`可以退出Python终端。

![](https://raw.githubusercontent.com/vwumumu/images/master/20230705143622.png)

## 练习 2.9-2.10

```python
# 练习 2.9

print(4+4)
print(2*4)
print(10-2)
print(64/8)

# 练习 2.10

favourite_number = 3
msg = f"my favourite number is {favourite_number}"  #拼字符串
print(msg)
```



# 3 列表简介

## 3.1 列表是什么

## 练习 3.1-3.3

```py
# 练习 3.1

names = ["张三", "李四", "王五"]
print(names[0])
print(names[1])
print(names[2])

# 练习 3.2

print(f"你好，{names[0]}")
print(f"你好，{names[1]}")
print(f"你好，{names[2]}")

# 练习 3.3

methods = ["开车", "骑车"]

print(f'通常，我都是{methods[0]}上班，偶尔，为了锻炼身体也会{methods[1]}去上班。(我信你个鬼')


## 注意中英文标点符号

# 英文标点：'' "" , .
# 中文标点：‘’ “” ， 。
```

从此刻开始，请注意，中英文标点符号在VSCode中的不同，对于包裹字符串用的引号是英文的。

![](https://raw.githubusercontent.com/vwumumu/images/master/20230706135501.png)

## 3.2 修改、添加和删除元素

列表中某个特定元素的修改，也就是对这个特定索引重新赋值。



对于删除列表中的元素，如果不使用删除后的内容，使用`del`语句，如果还使用删除后的内容，用`pop()`方法。



`remove()`只删除第一个指定的元素，如果要全部删除需要用循环遍历，以后会学到。



## 练习 3.4-3.7

```python
# 练习 3.4
invitees = ["张三", "李四", "王五"]
print(f'{invitees[0]}您好，诚挚地邀请您一起参加晚餐。')
print(f'{invitees[1]}您好，诚挚地邀请您一起参加晚餐。')
print(f'{invitees[2]}您好，诚挚地邀请您一起参加晚餐。')

# 练习 3.5
# 张三不能参加

print(f"{invitees[0]}不能参加晚宴。")
invitees[0] = "赵四"
print(f'{invitees[0]}您好，诚挚地邀请您一起参加晚餐。')
print(f'{invitees[1]}您好，诚挚地邀请您一起参加晚餐。')
print(f'{invitees[2]}您好，诚挚地邀请您一起参加晚餐。')

# 练习 3.6
print("大家好，我找到了一张更大的餐桌，将邀请更多的人参加晚餐。")
invitees.insert(0, "新1")
invitees.insert(2, "新2")
invitees.append("新3")
print(invitees)
print(f'{invitees[0]}您好，诚挚地邀请您一起参加晚餐。')
print(f'{invitees[1]}您好，诚挚地邀请您一起参加晚餐。')
print(f'{invitees[2]}您好，诚挚地邀请您一起参加晚餐。')
print(f'{invitees[3]}您好，诚挚地邀请您一起参加晚餐。')
print(f'{invitees[4]}您好，诚挚地邀请您一起参加晚餐。')
print(f'{invitees[5]}您好，诚挚地邀请您一起参加晚餐。')

# 练习 3.7
print("因为新买的餐桌无法送达，因此这次只能邀请两位朋友参加完餐，十分抱歉。")
target = invitees.pop()
print(f'很抱歉，{target}，没有办法邀请您参加晚宴了。')
target = invitees.pop()
print(f'很抱歉，{target}，没有办法邀请您参加晚宴了。')
target = invitees.pop()
print(f'很抱歉，{target}，没有办法邀请您参加晚宴了。')
target = invitees.pop()
print(f'很抱歉，{target}，没有办法邀请您参加晚宴了。')
print(f'{invitees[0]}，请您参加晚宴。')
print(f'{invitees[1]}，请您参加晚宴。')
del invitees[1]
del invitees[0]
print(invitees)
```

关于使用`del`语句删除的顺序的问题，请大家比较下面的区别：

```python
del invitees[1]
del invitees[0]

del invitees[0]
del invitees[1]

del invitees[0]
del invitees[0]
```



## 3.3 管理列表

向`sort()`方法传递一个参数，第一次使用参数。

```python
cars = ['audi','bmw','subaru','toyota']
cars.sort(reverse=True)
```

`True`在这里可以理解为`reverse`这个参数的开关，`=`也就是设定，设定为`True`，表示该选项打开。



注意比较下面的区别：

```python
cars.sort()
sorted(cars)
```

`cars`是列表，`sort()`是列表这种东西身上的方法，所以使用的方式是`cars.sort()`

`sorted()`是一个函数，具备特定的功能，对cars执行特定的功能，比如`print()`，也可以执行特定的功能。

感受这种区别。



len()其实在我前面的笔记中已经提到过了，也可以用户获取字符的长度，比如`hello`有5个字符：

```python
>>> len("hello")
5
```



## 3.4 使用列表时避免索引错误

未来，学习了if判断，可以判断列表的长度是否为0，避免空列表索引错误。

```python
>>> len([])
0
```



## 练习3.8-3.11

```python
# 练习 3.8
locations = ["Japan","Korea","France","Germany","Canada","Australia"]

print(locations) #打印列表
print(sorted(locations)) #不改变原列表按字母排序
print(locations)
print(sorted(locations,reverse=True)) #不改变原列表按字母反向排序
print(locations)
locations.reverse() #改变原列表逆转列表元素
print(locations)
locations.reverse() #改变原列表再逆转回来
print(locations)
locations.sort() #改变原列表按字母顺序排序
print(locations)
locations.sort(reverse=True) #改变原列表按字母顺序反向排序
print(locations)

# 练习 3.9
#我就直接打印练习3.8的列表长度了
print(len(locations))

# 练习 3.10
list = ["Japan","黄河","北京","德语","北京","bmw"]
print(list)
print(len(list))
list.pop()
print(list)
list.append("hi")
print(list)
list.insert(0,'mumu')
print(list)
list.remove("北京")
print(list)
del list[2]
print(list)
list.sort()
print(list)
list.reverse()
print(list)

# 练习 3.11
print(list[9])
```

sorted()使用reverse参数的参考：

![](https://raw.githubusercontent.com/vwumumu/images/master/20230706185017.png)

# 4 操作列表

## 4.1 遍历整个类别表

## 4.2 避免缩进错误

## 4.3 创建数值列表

## 4.4 使用列表的一部分

## 4.5 元组

## 4.6 设置代码格式



