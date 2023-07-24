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

```powershell
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
name = "ada lovelace" #原始的字符串
name = name.title()  #处理字符串
print(name)  #打印处理后的字符串
```



lower()方法很有用。把数据全部转换成小写保存，用的时候根据需要再转换为首字母大写或全大写。



f 字符串，有的地方会看到叫f-string，string翻译过来也是字符串。非常常用和重要的。



制表符（\t）通常就是按tab键的效果。



" python" 和 "python"是不同的，前面的python的p前面有一个空格，要对空格敏感，对计算机而言，空也是一种东西，虽然，对人而言，看上去好像空是不存在的。



### 练习2.3-2.8

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

在VSCode中，`Ctrl + /`可以将光标所在行快速的注释和取消注释。



## 2.6 Python之禅

输入`exit()`可以退出Python终端。

![](https://raw.githubusercontent.com/vwumumu/images/master/20230705143622.png)

### 练习 2.9-2.10

```python
# 练习 2.9

print(4 + 4)
print(2 * 4)
print(10-2)
print(64/8)

# 练习 2.10

favourite_number = 3
msg = f"my favourite number is {favourite_number}"  #拼字符串
print(msg)
```



# 3 列表简介

## 3.1 列表是什么

### 练习 3.1-3.3

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



### 练习 3.4-3.7

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
cars.sort()  #method
sorted(cars)  #function
```

`cars`是列表，`sort()`是列表这种东西身上的方法，所以使用的方式是`cars.sort()`

`sorted()`是一个函数，具备特定的功能，对`cars`执行特定的功能，比如`print()`，也可以执行特定的功能。

感受这种区别。



len()其实在我前面的笔记中已经提到过了，也可以用于获取字符串的长度，比如`hello`有5个字符：

```python
>>> len("hello")  #length
5
```



## 3.4 使用列表时避免索引错误

未来，学习了if判断，可以判断列表的长度是否为0，避免空列表索引错误。

```python
>>> len([])
0
```



### 练习3.8-3.11

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

`sorted()`使用`reverse`参数的参考：

![](https://raw.githubusercontent.com/vwumumu/images/master/20230706185017.png)

# 4 操作列表

## 4.1 遍历整个别表

## 4.2 避免缩进错误

概括一下：对于for里面的内容，要向右缩进，如果跟for的代码是左边是上下对齐的，就是for之外的代码，或者说是跟for平级的代码。

> 属于for循环的内容的内容，要向右缩进



提示一下：for的第一行结尾需要英文的冒号:

```shell
  File "c:\Users\vwumumu\Desktop\python_work\4.1-4.2.py", line 5
    for pizza in pizzas
                       ^
SyntaxError: expected ':'
```

### 练习4.1-4.2

```python
# 练习 4.1

pizzas = ["Margherita", "Pepperoni", "Hawaiian"]

for pizza in pizzas:
    print(pizza)
    print(f"I like {pizza} pizza.")
print("I really love pizza!")

# 练习 4.2

animals = ["lion", 'tiger', 'cougar']

for animal in animals:
    print(f"{animal} can roar loudly")
print('All these animals can roar loudly.')

```



## 4.3 创建数值列表

range(1,6)的结果是数字1，2，3，4，5，即括号内的范围是**含左不含右**的。



列表推导式，新人不掌握也没关系，但是需要知道，避免看到别人的代码不认识。

### 练习 4.3-4.9

```python
# 练习 4.3
for i in range(1,21):
    print(i)

# 练习 4.4
list = range(1,1_000_001)
# for i in list:
    # print(i)

# 练习 4.5
print(min(list))
print(max(list))
print(sum(list))

# 练习 4.6
odd = range(1,21,2)
for i in odd:
    print(i)

# 练习 4.7
three_times = range(3,31,3)
for i in three_times:
    print(i)

# 练习 4.8
cube = []
list2 = range(1,11)
for i in list2:
    cube.append(i ** 3)
print(cube)

# 练习 4.9
cube = [i ** 3 for i in range(1,11)]
print(cube)
```

```python
cube = []
for i in range(1,11):
	cube.append(i ** 3)
print(cube)
    
# cube = [i ** 3 for i in range(1,11)]
```



## 4.4 使用列表的一部分(切片)

### 练习4.10-4.12

```python
# 练习 4.10

three_times = list(range(3,31,3))
# for i in three_times:
#     print(i)

print(f"The first three items in the list are: {three_times[0:3]}")
print(f"Three items from the middle of the list are: {three_times[4:7]}")
print(f"The last three items in the list are: {three_times[-3:]}")

# 练习 4.11

pizzas = ["Margherita", "Pepperoni", "Hawaiian"]
friend_pizzas = pizzas[:]

friend_pizzas.append("榴莲披萨")
for pizza in pizzas:
    print(f"I like {pizza} pizza.")

for pizza in friend_pizzas:
    print(f"I like {pizza} pizza.")

# 练习 4.12

#同练习4.11
```



## 4.5 元组

不可变的列表称为元组（tuple）。



不能修改元组中的元素，但是可以对元组的变量重新赋值一个新元组，这本质上是赋值，跟元组本身并没有什么关系。



### 练习 4.13

```python
# 练习 4.13

foods = ("苹果", "香蕉", "西瓜", "草莓", "橙子")

for food in foods:
    print(food)

# foods[0] = "榴莲"

foods = ("苹果", "榴莲", "葡萄", "草莓", "橙子")

for food in foods:
    print(food)
```



## 4.6 设置代码格式

通过VSCode实现代码的格式化

1. 如下图，在VSCode中安装Python插件：

   ![](https://raw.githubusercontent.com/vwumumu/images/master/20230712004001.png)

2. 在任意Python代码文件的代码区域右键选择`Format Document With...`

   ![](https://raw.githubusercontent.com/vwumumu/images/master/20230712004127.png)

3. 设置默认的格式化Python代码所使用的插件

   ![](https://raw.githubusercontent.com/vwumumu/images/master/20230712004236.png)

4. 选择Python作为默认：

   ![](https://raw.githubusercontent.com/vwumumu/images/master/20230712004331.png)

5. 之后，在VSCode代码区右键选择`Format Document`或者同时按键盘`Shift + Alt + F`自动格式化Python代码：

   ![](https://raw.githubusercontent.com/vwumumu/images/master/20230712004421.png)

# 5 if语句

## 5.1 一个简单的示例

## 5.2 条件测试

对于新手，可能会比较难判断什么情况下`if`代码块的内容执行。

尤其是涉及到`and`, `or`的情况，因为需要判断的内容可能会比较多和复杂。

一个简化的方式是直接把需要判断的内容print出来看看是`True`还是`False`，如果结果是`True`，就会执行if代码块内的代码。

比如：

```python
age_0 = 22
age_1 = 18

if age_0 >= 21 and age_1 >= 21:
	print("Hi")
    
print(age_0 >=21 and age_1 >=21)
```

把`age_0 >=21 and age_1 >=21`打印出来，结果是`False`，自然`if`不会执行，无法打印`Hi`。



 ### 练习5.1-5.2

```python
# 练习 5.1

print("1" == 1)
print("a" == "A")
print("?" == "？")
print(1 > 2 and 3>2)
print(2 > 1 and 3>2)
print(1 > 2 or 3>2)
print(2 > 1 or 3>2)
print("Mumu" in ["Mumu","Zhang San"])
print("mumu" in ["Mumu".lower(),"Zhang San"])
print("Mumu" not in ["Mumu","Zhang San"])


# 练习 5.2

#同练习5.1
```



## 5.3 if语句

注意，`if elif`，从上向下，当有一个`elif`满足时，后面的条件将不再判断。

如果需要把所有的条件都判断，需要写成一个个独立的`if`。

多体会5.3.6披萨的例子。



### 5.3-5.7

```python
# 练习 5.3
alien_color = "green"
if alien_color == "green":
    print("获得5分")

alien_color2 = "red"
if alien_color2 == "green":
    print("获得5分")


# 练习 5.4
if alien_color == "green":
    print("获得5分")
elif alien_color != "green":
    print("获得10分")

if alien_color2 == "green":
    print("获得5分")
elif alien_color2 != "green":
    print("获得10分")

# 练习 5.5
if alien_color == "green":
    print("获得5分")
elif alien_color == "yellow":
    print("获得10分")
else:
    print("获得15分")

# 练习 5.6

age = 18

if age < 2:
    print("婴儿")
elif age < 4:
    print("幼儿")
elif age < 13:
    print("儿童")
elif age < 18:
    print("少年")
elif age < 65:
    print("中青年人")
else:
    print("老年人")


# 练习 5.7
favorite_fruits= ["apple","orange","banana"]
if "a" in favorite_fruits:
    print("You really like a")
if "b" in favorite_fruits:
    print("You really like a")
if "c" in favorite_fruits:
    print("You really like a")
if "apple" in favorite_fruits:
    print("You really like apple")
if "banana" in favorite_fruits:
    print("You really like banana")
```



## 5.4 使用if语句处理列表

如何验证空列表是False？

```python
>>> a = []
>>> a == False
False
>>> a == True
False
>>> type(a)
<class 'list'>
>>> type(False)
<class 'bool'>
>>> bool(a) == False
True
```

### 练习5.8-5.11

```python
# 练习 5.8
users = ["admin","a","b","c","d"]

for user in users:
    if user == "admin":
        print("admin")
    else:
        print("user")

# 练习 5.9
if users:
    for user in users:
        if user == "admin":
            print("admin")
        else:
            print("user")
else:
    print("We need to find some users!")


# 练习 5.10
current_users = []

for i in users:
    current_users.append(i.lower())

new_users = ["c","d","e","f","g"]


for user in new_users:
    if user in current_users:
        print("The user name has been used. Please using another one.")
    else:
        print("The user name is avaliable.")

# 练习 5.11

list = list(range(1,10))
for i in list:
    if i == 1:
        print("1st")
    elif i == 2:
        print("2nd")
    elif i == 3:
        print("3rd")
    else:
        print(f"{i}th")
```



## 5.5 设置if语句的格式

同4.6

# 6 字典

## 6.1 一个简单的字典

## 6.2 使用字典

### 练习6.1-6.3

```python
# 练习 6.1

person = {"firstname": "mumu", "lastname": "wu", "age": 18, "city": 'beijing'}

print(person["firstname"])
print(person["lastname"])
print(person["age"])
print(person["city"])

# 练习 6.2

db = {"a": 1, "b": 2, "c": 3, "d": 4, "e": 5}

print(f'a like {db["a"]}')
print(f'b like {db["b"]}')
print(f'c like {db["c"]}')
print(f'd like {db["d"]}')
print(f'e like {db["e"]}')


# 练习 6.3

db2 = {"string": "一串文字", "int": "整数",
       "float": "小数", "list": "列表", "tuple": "元组"}

print(f'string: {db2["string"]}')
print(f'int: {db2["int"]}')
print(f'float: {db2["float"]}')
print(f'list: {db2["list"]}')
print(f'tuple: {db2["tuple"]}')
```



## 6.3 遍历字典

python提供很多方法，既可以遍历字典的所有键值对，也可以只遍历键或者值。



.items()是字典的所有元素；

.key()是字典的键；

.value()是字典的值。



### 练习6.4-6.6

```python
# 练习 6.4

db2 = {"string": "一串文字", "int": "整数",
       "float": "小数,浮点数", "list": "列表", "tuple": "元组", "set": "集合", "boolean": "布尔值，Ture和False"}

for k, v in db2.items():
    print(k, ":", v)

# 练习 6.5

rivers = {"尼罗河": "埃塞俄比亚，苏丹，埃及，乌干达，坦桑尼亚，肯尼亚，卢旺达，布隆迪，摩洛哥，刚果和南苏丹",
          "亚马逊和": "巴西，玻利维亚，秘鲁，厄瓜多尔，哥伦比亚，委内瑞拉，圭亚那，苏里南和法属圭亚那", "Danube": "德国，奥地利，斯洛伐克，匈牙利，克罗地亚，塞尔维亚，罗马尼亚，保加利亚，摩尔多瓦和乌克兰"}

for k, v in rivers.items():
    print(f"The {k} runs through {v}.")

print("\n河流的名字：")
for k in rivers.keys():
    print(k)

print("\n国家的名字：")
for v in rivers.values():
    print(v)

# 练习 6.6
favorite_languages = {
    "jen": "python",
    "sarah": "c",
    "edward": "rust",
    "phil": "python",
}

people = ["jen","edward","mumu"]

for p in people:
    if p in favorite_languages.keys():
        print(f"Hi {p.title()}, thanks for take the survey.")
    else:
        print(f"Hi {p.title()}, could you please help to complate the survey?")

```



## 6.4 嵌套

### 练习6.7-6.12

```python
# 练习 6.7

person1 = {"firstname": "mumu", "lastname": "wu", "age": 18, "city": 'beijing'}
person2 = {"firstname": "san", "lastname": "zhang",
           "age": 19, "city": 'shanghai'}
person3 = {"firstname": "si", "lastname": "li", "age": 20, "city": 'guangzhou'}

list = [person1, person2, person3]

for i in list:
    print(i)

# 练习 6.8

pets = {"amao": {"category": "cat", "owner": "zhangsan"},
        "agou": {"category": "dog", "owner": "lisi"}}

for k,v in pets.items():
    print(k,v)


# 练习 6.9
#类似6.8

# 练习 6.10
#类似编程语言的题目：
favorite_languages = {
    "jen": ["python", "rust"],
    "sarah": ["c"]
}

for name, language in favorite_languages.items():

    if(len(language) == 1):
        print(f"{name}'s favorite langue is:")
        for i in language:
            print(i)
    else:
        print(f"{name}'s favorite langue are:")
        for i in language:
            print(i)

# 练习 6.11
#重复练习，跳过

# 练习 6.12
#参考练习6.10，结合了if对遍历内容做判断。
```



# 7 用户输入和while循环

## 7.1 input()函数的工作原理

7.1.1中的示例使用了+=，还记得这是什么吗？

+=就是先+然后再=（赋值），比如下面两行代码是等价的:

```
a += b
a = a + b
```



input()函数得到的结果会转换为字符串，即使输入的是数字。



求模运算符（%），取余数。



### 练习7.1-7.3

```python
# 练习 7.1
car = input("请问您想要租什么车？")
print(f"让我查询一下是否有{car}")

# 练习 7.2
customers = int(input("请问您有几位用餐？"))
if customers > 8:
    print("很抱歉，已经没有空位了。")
else:
    print("可以的，欢迎就餐。")

# 练习 7.3

number = int(input("请输入一个数字"))
if number % 10 == 0:
    print("这个数字是10的整数倍。")
else:
    print("这个数字不是10的整数倍。")

```



## 7.2 while 循环简介

continue是继续的意思，往往容易让人误解，实际上是break+continue，结束本次循环，然后继续后面的循环。

### 练习7.4-7.7

```python
# 练习 7.4

active = True

while active:
    a = input("请输入您需要添加的披萨配料：")
    if a != "quit":
        print(f"将在披萨中添加{a}")
    else:
        active = False

# 练习 7.5

while True:
    age = int(input("请问您的年龄是？"))
    if age < 3:
        print("免费")
    elif age < 12:
        print("10元")
    else:
        print("15元")

# 练习 7.6

while True:
    a = input("请输入您需要添加的披萨配料：")
    if a != "quit":
        print(f"将在披萨中添加{a}")
    else:
        break

# 练习 7.7
while True:
    print("按Ctrl + C,或者关闭窗口结束无限循环。")

```



## 7.3 使用while循环处理列表和字典

for循环是一种遍历列表的有效方式，但不应该在for循环中修改列表，否则将导致Python难以跟踪其中的元素。要在遍历列表的同时修改它，可使用while循环。通过将while循环与列表和字典结合起来使用，可收集、存储并组织大量的输入，供以后查看和使用。

### 练习7.8-7.10

```python
# 练习 7.8

sandwich_orders = ["a", "pastrami", "b", "pastrami", "c", "pastrami"]
finished_sandwiches = []

for i in sandwich_orders:
    print(f"I made your {i}")
    finished_sandwiches.append(i)

print(finished_sandwiches)

# 练习 7.9

print("pastrami have sold out.")
sandwich_orders2 = ["a", "pastrami", "b", "pastrami", "c", "pastrami"]
finished_sandwiches2 = []

while "pastrami" in sandwich_orders2:
    sandwich_orders2.remove("pastrami")

finished_sandwiches2 = sandwich_orders2[:]
print(finished_sandwiches2)

# 练习7.10

while True:
    target = input("If you could visit one place in the world, where would you go?")
    print(target)
```



# 8 函数

## 8.1 定义函数

关于形参实参，如果不好记什么是形参，我们可以记住实参，即调用一个函数时实际要提供的参数。

比如例子：greet_user("mumu")，mumu是实际上要提供给函数greet_user()的，所以mumu在这里是实参（实际的参数），那greet_user(username)的username就是形参。



## 8.2 传递实参

位置实参，也就是说，在提供给函数的参数的顺序，位置，决定了这个参数值是对应到哪个参数的变量。

关键字实参，将参数值指定给某个具体的参数变量。



建议把包含默认值的形参放到函数的后面，这样实参还可以按照位置顺序指定给没有默认值的形参。



### 练习8.1-8.5

```python
# 练习 8.1

def display_message():
    print("function")


display_message()

# 练习 8.2


def favorite_book(title):
    print(f"One of my favorite books is {title}")


favorite_book("Alice in Wonderland.")

# 练习 8.3


def make_shirt(size, text):
    print(f"shirt size is {size}, and text: {text} on it")


make_shirt(1, "hi")
make_shirt(text="hello", size=2)


# 练习 8.4

def make_shirt2(size="Big", text="I love Python"):
    print(f"shirt size is {size}, and text: {text} on it")


make_shirt2()
make_shirt2("Middle")
make_shirt2("Small", "Coding")


# 练习 8.5

def describe_city(city, country):
    print(f"{city} is in {country}")


describe_city("Beijing", "China")

```



## 8.3 返回值

请认真阅读，理解8.3.2，如何让实参变成可选的：指定默认值为空字符串，移到形参列表的末尾，在函数体内对空值进行判断，实现实参可选。



### 练习8.6-8.8

```python
# 练习 8.6

def city_country(city, country):
    return f"{city.title()}, {country.title()}"


print(city_country("beijing", "china"))
print(city_country("shanghai", "china"))
print(city_country("guangzhou", "china"))


# 练习 8.7

def make_album(singer, album, songs=None):
    if songs == None:
        return {singer.title(): {"Album": album.title()}}
    else:
        return {singer.title(): {"Album": album.title(), "Songs": songs}}


print(make_album("zhoujielun", "a"))
print(make_album("zhoujielun", "b"))
print(make_album("zhoujielun", "c", 12))

# 练习 8.8

while True:
    singer = input("请提供歌手名：(输入q退出程序)")
    if singer == "q":
        break
    album = input("请提供专辑名：(输入q退出程序)")
    if album == "q":
        break
    print(make_album(singer, album))

```



## 8.4 传递列表

每个函数都应该只负责一项具体工作。



### 练习8.9-8.11

```python
# 练习 8.9

list = ["a", "b", "c"]


def show_messages(list):
    for i in list:
        print(i)


show_messages(list)

# 练习 8.10

list2 = []

def send_messages(list,list2):
    for i in list:
        list2.append(i)

send_messages(list,list2)

print(list)
print(list2)


# 练习 8.11
send_messages(list[:],list2)  #如果移除用pop()实现，可以保留原list
```



## 8.5 传递任意数量的实参

传递任意数量的参数就是把这些实参作为形参的元素，构成一个元组，然后在函数内部，可以操纵这个元组。



注意8.5.1和8.5.2的不同，一个星号\*是任意实参为元组，两个星号\*是任意实参为字典。



你经常会看到通用形参名*args，收集任意数量的位置实参。

你经常会看到通用形参名**kwargs，收集任意数量的关键字实参。



### 练习8.12-8.14

```

```



## 8.6 将函数存储在模块中
## 8.7 函数编写指南
## 9.1 创建和使用类
## 9.2 使用类和实例
## 9.3 继承
## 9.4 导入类
## 9.5 Python标准库
## 9.6 类的编程风格
## 10.1 读取文件
## 10.2 写入文件
