## 一、段落与换行
1.段落前后必须是空行,如果没有则会显示在一行中(换行符被转换为空格)

2.或者使用`<br>`标签

## 二、标题
### 1.Setext形式
```
h1
====

h2
----
```
h1
====
h1
----


### 2.atx形式
```
#### H4 ####
##### H5 #####
```
#### H4 ####
###### H5 ######


or just left

```
#### H4
##### H5
```
## 三、引用
### 1.行内引用

```
> 引用内容
```
> 引用内容
### 2.多行引用

```
多行引用
在每行前加'>'
```
> s1

> s2

> s3

### 3.嵌套引用

```
> 也可以在引用中
>> 使用嵌套的作用
```

> s1
>> s2

### 4.可以在引用中使用其他markdown语法

`` > # 这是一个一级标题 ``
> # 这是一级标题

## 四、列表

### 1.无序列表

     * 
     + 
     - 
    三者均可作为列表标记




* 使用 * 做标记
+ 使用 + 做标记
- 使用 - 做标记

### 2.有序列表

    1.有序列表以数字和'.'开始;
    3.数字的序列并不会影响生成的列表
    4.但仍然推荐按照自然序列(1, 2, 3...)编写




1. 有序列表以数字和'.'开始;

3. 数字的序列并不会影响生成的列表序列;

4. 但仍然推荐按照自然顺序(1.2.3...)编写。




### 3.嵌套的列表

    1. 第一层
    + 1-1
    + 1-2    
    2. 无序列表和有序列表可以随意相互嵌套
    3. 2-1
    4. 2-2





1. 第一层
+ 1-1
+ 1-2
2. 无序列表和有序列表可以随意相互嵌套
    1. 2-1
    2. 2-2

### 4.语法和用法

1. 无序列表项的开始是: `对应标记 + 空格`;
2. 有序列表项的开始是: `数字 + '.' + 空格`;
3. 空格至少为一个，多个空格将被解析为一个;
4. 如果仅需要在行前显示数字和`.`:

`05\.可以使用:数字.\来取消显示为列表`

05\.可以使用:数字.\来取消显示为列表

## 五、代码
### 1.多行代码
可以使用缩进来插入代码块

    <html>// Tab 开头
        <title>Markdown</title>
    </html>




代码快前后需要有至少一个空行，且每行代码前需要有至少一个Tab或四个空格

### 2.行内代码
通过``(位于Tab键上面)插入行内代码

`<title>Markdown</title>`

## 6、分割线

1.可以在一行中使用三个或更多的`*`,`-`,`_`来添加分割线(`<hr>`):


    ***
    -------
    ____




***
---
___

2.多个字符之间可以有空格（空白符）,但不能有其他字符

    * * *
    - - -




* * *
- - -

## 超链接


### 1.行内式

1.格式为`[link text](URL)`

`[Baidu](http://www.baidu.com)
`

[Baidu](http://www.baidu.com)

2.指向本地文件的链接

`[icon.png](./images/icon.png)
`

[icon.png](./images/icon.png)

3.包含'title'(可选)的链接

`[Baidu](http://www.baidu.com/ "Baidu")
`

[Baidu](http://www.baidu.com/ "Baidu")

### 2.参考式

1.首先定义链接

`[Baidu][link]`

[Baidu][link]第二个方阔号内为链接独有的**识别符**，可以是字母、数字、空白或标点符号，不区分大小写。

2.然后定义链接内容
`[link]:http://www.baidu.com/ "Baidu"
`

[link]:http://www.baidu.com/ "Baidu"

3.也可以**省略** *识别符*

    [Baidu][]
    [Baidu]: http://www.baidu.com/ "Baidu"





[Baidu][]

[Baidu]: http://www.baidu.com/ "Baidu"


### 3.自动链接

使用`<>` 包括的URL或邮箱地址会被自动转化为超链接:

    <http://www.baidu.com/>
    <123@email.com>




<http://www.baidu.com/>

<123@email.com>



## 图片

### 1.行内式

    ![text.jpg](./3265208.jpeg title)

![text.jpg](./3265208.jpeg "picture")



方括号中的部分是图片的替代文本，括号中的'title'部分和链接一样，是可选的

### 2.参考式

    ![text][text]
    [text]: ./3265208.jpeg





![text][text]

[text]: ./3265208.jpeg





### 3.制定图片的显示大小

`<img src = "./3265208.jpeg" width = "50" height = "50" />
`

<img src = "./3265208.jpeg" width = "50" height = "50" />

## 强调

1.使用`**`或`__`包括的文本会被转换为`<em></em>`, 通过表现为斜体

这是用来*演示*的 _文本_

2.使用`** **`和`__ __`包括的文本会被转换为`<strong></strong>`,通常表现为加粗:

这是用来**演示**的 __文本__

3.`*`,`_`内侧不能有空白

4.如果文本需要显示`*`或`_`，可以使用转义字符`\`

5.符号标记必须成对*使用*


## 删除线

    这就是~~~删除线~~~

这就是~~~删除线~~~。


## 代码块语法高亮

    ```
    <p>code here</p>
    ```


```
<p>code here</p>
```

### 代码高亮

    ```c++
    #include <iostream>
    using namespace std;
    int main()
    {
        cout << "Hello Markdown";
        return 0;    
    }
    ```





```c++
#include <iostream>
using namespace std;
int main()
{
    cout << "Hello Markdown";
    return 0;    
}
```




第一个\`\`\`后面可以设置不同语言的语法高亮

## 表格

### 1.单元格和表头 

使用`|`来分隔不同的单元格，使用`-`来分隔表头和其他行

    name | age
    -- | --
    LearShare | 12
    Mike | 32
    bob | 22





name | age
-- | --
LearShare | 12
Mike | 32
bob | 22

### 2.对齐

在表头下方的分隔线标记中加入`:`, 即可标记下方单元格内容的对齐方式

+ `+---`代表左对齐
+ `:--:`代表居中对齐
+ `---:`代表右对齐

      | left | center | right |
      | :--- | :---:  | ----: |
      | aaa | bbbb | cccc |
      | a | b | c |





| left | center | right |
| :--- | :---:  | ----: |
| aaa | bbbb | cccc |
| a | b | c |



### 3.插入其他内容

表格中可以插入其他的Markdown中的行内标记:



    | name | age | blog |
    | ---- | --- | ---- |
    | _LearnShare_| 12 | [LearnShare](http://xianbai.me) |
    | __Mike__ | 32 | [Mike](http://mike.me) |





| name | age | blog |
| ---- | --- | ---- |
| _LearnShare_| 12 | [LearnShare](http://xianbai.me) |
| __Mike__ | 32 | [Mike](http://mike.me) |

## Task List

    - [✔]Eat
    - [ ]Code
        + HTMl
        + CSS
        + JavaScript
    - [ ]Eat
    - [ ]Code
        + [ ]HTML
        + [ ]CSS
        + [ ]JavaScript
    - [ ]Sleep


- [✔]Eat
- [ ]Code
    + HTMl
    + CSS
    + JavaScript
- [ ]Eat
- [ ]Code
    + [ ]HTML
    + [ ]CSS
    + [ ]JavaScript
- [ ]Sleep

## 格式转换

### Pandoc

#### 1.导出为HTML

[Installing](https://www.pandoc.org/) Pandoc

打开命令行，进入文档所在目录

执行下面的命令，将Markdown转换为HTML:

`pandoc -o hello.html hello.md`

自定义HTML样式:

`pandoc -o hello.html -c style.css hello.md`




#### 2.导出为PDF

`pandoc -o hello.pdf hello.md`

同样也可通过`-c style.css`来指定样式文件

##### chrome

将Markdown转化为HTML文档后,用`Chrome`
打开它，选择`打印`,然后`更改目标打印机`为`另存为PDF`，再进行一些设置后，即可保存为PDF文档


#### 3.导出为word

`pandoc -o hello.docx hello.md`



**<p style="color: red">建议再下载一个`typora`亲测命令行方式导出文件一坨屎，另外Typora也是一款非常优秀的Markdown编辑器，值得一用。</p>**





