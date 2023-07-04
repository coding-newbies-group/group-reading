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



f 字符串，有的地方会看到叫f-string，string翻译过来也是字符串。



制表符通常就是按tab键的效果。



" python" 和 "python"是不同的，前面的p前面有一个空格，要对空格敏感，对计算机而言，空也是一种东西，虽然，对人而言，看上去好像空是不存在的。



练习：

```python
# 练习2.3
name = "Eric"
msg = f"Hello {name}, would you like to learn some Python today?"
print(msg)

# 练习2.4
print(name.lower())
print(name.upper())
print(name.capitalize())

# 练习2.5
print('Albert Einstein once said, "A person who never made a mistake never tried anything new."')

# 练习2.6
famous_person = "Albert Einstein"
msg2 = f'{famous_person} once said, "A person who never made a mistake never tried anything new."'
print(msg2)

# 练习2.7
name2 = " Mumu \t Wu \n "
name3 = "Mumu \t Wu"
print(len(name2.strip()))
print(len(name3.strip()))
```

练习2.7，为了验证删除空白的效果，我创建了name3作为对照，len()函数用于获取结果的长度，发现长度是一致的，所以，对于删除空白，name3的内容等价于name2删除空白后的结果。

![](https://raw.githubusercontent.com/vwumumu/images/master/20230704221357.png)



## 2.4 数



## 2.5 注释



## 2.6 Python之禅



# 3 列表简介
