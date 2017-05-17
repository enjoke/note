# Markdown Syntax

## What's Markdown
>Markdown是一种可以使用普通文本编辑器编写的标记语言，通过简单的标记语法，它可以使普通文本内容具有一定的格式。

## Syntax

### 标题
#### 类 Setext 形式
类Setext 形式是用底线的形式，利用 = （最高阶标题）和 - （第二阶标题）

e.g:
>一级标题
>=========
>二级标题
>---------  

####类 Atx 形式
类 Atx 形式则是在行首插入 1 到 6 个 # ，对应到标题 1 到 6 阶

e.g:
>#一级标题
>##二级标题

###区块引用 Blockquotes
1. 	Markdown 标记区块引用是使用类似 email 中用 > 的引用方式。可以在每一行前加上'>',也可以只在第一行加上'>'
2. 	区块引用可以嵌套（例如：引用内的引用），只要根据层次加上不同数量的'>'
3. 	引用的区块内也可以使用其他的 Markdown 语法，包括标题、列表、代码区块等

###列表
Markdown 支持有序列表和无序列表.

1.	注意列表标记和内容之间要加上一个空格或者tab  
2.	一个列表标记可以包括多行，可对齐可不对齐，包括多个段落时，每个项目下的段落必须缩进4个空格或者一个tab(貌似需要2个tab)  
3.	如果要在列表项目内放进引用，那 > 就需要缩进(貌似不需要吧？)
4.	放代码区块的话，该区块就需要缩进两次，也就是 8 个空格或是 2 个制表符：(好像也不需要？)
5.	在行首出现数字-句点-空白，要避免这样的状况，你可以在句点前面加上反斜杠  
>	1986. What a great season.  
>	1986\. What a great season. /\*这里是加上反斜杠后的\*/
####无序列表
无序列表使用星号、加号或是减号作为列表标记，三者等价

>    
>*	Lorem ipsum dolor sit amet, consectetuer adipiscing elit.  
>	Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,  
>	viverra nec, fringilla in, laoreet vitae, risus.
>    
>		Donec sit amet nisl. Aliquam semper ipsum sit amet velit.  
>		Suspendisse id sem consectetuer libero luctus adipiscing.  
>	 
>+	A list item with a blockquote:
>	> This is a blockquote
>	> inside a list item. 
>-	code block for c:
>		int main(int argc, char **agrv)
>		{
>			printf("Hello world!\n");
>			return 0;
>		}  
>    

####有序列表
有序列表则使用数字接着一个英文句点
数字可以随意设置

>   
>	2. 这是从2开始
>	4. 但我不是3
>	5. 瞎了吧，根本没有用
>	

### 代码区块
空4格或者tab键，markdown 会将该段当代码看待，但是要避免c/c++ 等include头文件时被忽略，应在代码前后加上```，暂不考虑语法高亮  
e.g:

	```
	/*test for code */
	#include <stdio.h>

	int main(int agrc, char **agrv)
	{
		printf("Hello World!\n");
		return 0;
	} 
	```

### 分割线
在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。也可以在星号或是减号中间插入空格。  
> 	***
>	- - - 

### 区段元素
#### 链接
1.	链接文字用'[]'来标记
2.	Markdown 支持两种形式的链接语法： 行内式和参考式两种形式。
3.	链接到同样主机的资源，可以使用相对路径：
4.	参考式：在链接文字的括号后面再接上另一个方括号，而在第二个方括号里面要填入用以辨识链接的标记,这个标记的链接内容可以在文件任意处定义
5.	链接内容定义的形式为：
	[linkname]:\tab<http://127.0.0.1> title(可选)
6.	隐式链接标记功能可以省略指定链接标记，链接标记会视为等同于链接文字，要用隐式链接标记只要在链接文字后面加上一个空的方括号
>	行内式：
>	1.	This is [an example](http://example.com/ "Title") inline link.  
>	2.	[This link](http://example.net/) has no title attribute.  
>	3.	See my [About](/about/) page for details. /\* 相对路径 \*/  
>	4.	[id]:	http://example.com/  "Optional Title Here" 
>	This is [an example] [id] reference-style link.
>	5.	[google]:	http://google.com
>	[google][]

### 强调
使用星号（*）和底线（_）作为标记强调字词的符号，被 * 或 _ 包围的字词会被转成用 &lt;em&gt; 标签包围，用两个 * 或 _ 包起来的话，则会被转成 &lt;strong&gt;
>	*一个星号*
>	**两个星号**

### 代码
可以用一对反引号标记一段行内代码
> 	this is `printf("%s\n", "Hello World!");`.

### 图片
类似于链接，同样有行内式和参考式
语法：
![picname](img.jpg)
`![Alt text](/path/to/img.jpg "Optional title")`


