



## JAVA入门

## 1.JAVA是什么

---

JAVA是一个编程语言

### JAVA学习

#### 1.JAVA可以做些什么呢?

##### 1.1三大平台

JAVASE	JAVAME	JAVAEE

###### 1.2JAVA SE

Java语言的(标准版)，用于桌面的开发，是其他两个版本的基础。

桌面应用开发

用户打开程序，程序会让用户在最短时间内找到他们需要的功能，同时主动带领用户完成工作并得到最好的体验

学习Java的目的为今后从事Java ee做基础

###### 1.3JAVA ME

Java语言(小型版)，用于嵌入式电子设备或小型移动设备

###### 1.4JAVA EE

 Java语言的(企业版)，用于web方向的网站开发。在这个领域，是当之无愧的no1

网站开发

浏览器+服务器

##### 常见六大类

###### ● 桌面应用开发

各种税务管理软件，IDEA,Clion,pycharm

###### ● 企业级应用开发

微服务，springcloud

###### ● 移动应用开发

鸿蒙，Android，医疗设备

###### ● 科学计算

matlab

###### ● 大数据开发

hadoop

###### ● 游戏开发

我的世界

#### Java为什么这么火

###### ● Java的特性

● 面向对象

###### ● 跨平台

##### ● 开源

##### ● 简单易用

##### ● 多线程

##### ● 安全性

#### JRE和JDK

##### 1.JDK是什么?有哪些内容组成?

JDK是java开发工具包

JVM虚拟机:java程序运行的地方

核心类库:java已经写好的东西,我们可以直接御用.

开发工具:javac,java、jdb,jhat...

##### 2.JRE是什么?有哪些内容组成?

JRE是java运行环境

JVM,核心类库,运行工具

##### 3.JDK,JRE,JVM三者的包含关系

JDK包含了JRE

JRE包含了JVM

#### JAV程序初体验

##### 下载和安装

---

1.通过官网下载● .[http://www.oracle.com]

2.注意针对操作系统，下载对应安装包

3.安装路径不要包含中文

4jdk安装目录

```typescript
1.bin:该路径↓存放了各种工具命令其中比较重要的有:javac和Java
2.conf:该路径下存放了相关配置文件
3.include:该路径下存放了一些平台特定的头文件
4.jmods:该路径下存放了各种模块。
5.legal:该路径下存放了各模块的授权文档
6.lib:该路径下存放了工具一些补充jar包
```

##### **配置环境变量**

```java
●JAVA_HOME
变量值填写电脑安装jdk的跟目录(C:\Program Files\Java\jdk-22)
●Path
%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;
●CLASSPATH 
.;%JAVA_HOME%\lib;%JAVA_HOME%\lib\tools.jar

```

##### Notepad++

● 常见的高级记事本Editplus  notepad++  sublime等

### 第一个程序Hello Word

#### 1.创建一个Hello Word.JAVA文件

```java
public class Helloworld{
    public static void main(String[]args){
            System.out.println("Hello world");
    }
}
```

#### 2.打开cmd，跳转到程序所在目录

```typescript
javac 你需要编译的文件名称加后缀
```

#### 3.编译结束以后回出现一个class后缀的文件,现在去运行

![image-20240414111443960](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240414111443960.png)

```java
java 你需要运行的文件的名称(不需要后缀)
```

![image-20240414111731305](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240414111731305.png)

#### ● 案列常见问题

##### 中英文符号间隔

```
英文的是(;)
```

##### 单词拼写问题

```
System S为大写
```

##### 类 HelloWorld 是公共的

```
源文件名应与类名一致
```

## 2.JVAA基础语法

---

### 注释

使用细节

1.注释内容不会参与编译和运行,仅仅是对代码的解释说明

2.不管是单行注释还是多行注释,在书写的时候都不要嵌套

```typescript
单行注释
//注释信息
多行注释
/*注释信息*/
文档注释
/**注释信息**/
```

```java
public class HelloWorld{
	//叫做main方法,表示程序的主入口
	public static void main(String[] args){
			/*叫做输出语句(打印语句)
			会把小括号里面的内容进行输出打印*/
			System.out.println("HelloWorld");
	}
}

```



### 关键字

---

关键字::被java赋予了特定函数的英文单词

#### 关键字特点

关键字的字母**全部小写**

常营的的代码编辑器,针对关键字有特殊的颜色标记,非常直观.

```java
public class HelloWord{
    public static void main(String[] args){
        System.out.println("这是一个关键字");
    }
}
```

![image-20240414130048606](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240414130048606.png)

#### class

---

![image-20240414130323866](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240414130323866.png)

class:用于(创建/定义)一个类 类是java最基本的组成单元

### 字面量

---

告诉程序员:数据在程序中的书写格式

```java
public class HelloWorld{
	public static void main(string[] args){
		18	放心嘛	1.85
	}
}
```



#### 字面量的分类

|               **字面量类型**                |                         **说明**                         |               **举例**                |
| :-----------------------------------------: | :------------------------------------------------------: | :-----------------------------------: |
|                整数型类型int                |                     不带小数点的数字                     |                666,-88                |
| <font color='red'>**小数型**</font>(double) |         <font color='red'>带小数点的数字</font>          | <font color='red'>13.14 ,-5.21</font> |
|                 字符串类型                  |                   用双引号括起来的内容                   |         "HelloWorld","放心嘛"         |
|      <font color='red'>字符类型</font>      | <font color='red'>用单引号括起来的,内容只能有一个</font> |             'A','1','我'              |
|                  布尔类型                   |                     布尔值,表示真假                      |         只有两个值:true,false         |
|                   空类型                    |                    一个特殊的值,空值                     |               值是:null               |

空类型:null只能用字符串的形式进行打印

---



```java
public class valueDemo1{
	public static void main(String[] args){
		//目标:需要大家掌握常见的数据在代码中如何书写的?
		
		//整数
		System.out.println(666);
		System.out.println(-777);
		
		//小数
		System.out.println(666);
		System.out.println(-3.14);
		
		//字符串
		System.out.println("这是一串字符串");
		System.out.println("放心嘛");
		
		//字符
		System.out.println('男');
		System.out.println('女');
		System.out.println('A');
		System.out.println('1');
		
		//布尔
		System.out.println(true);
		System.out.println(false);
		
		//空类型
		//细节:null不能直接打印店
		//如果要打印null,那么只能用字符串的形式进行打印
		System.out.println("null");
	}
}


```

##### 扩展点:特殊字符

---

###### \t	制表符

在打印的时候,把前面的字符串的长度补齐到8,或者8的整数倍.最少补1个空格,最多补8个空格.

```java
public class HelloWorld
    public static void main(string[] args){
    System.out.println("abcd"+'\t');
}
```

---

用途可以使代码更好看

```
public class valueDemo2{
	public static void main(String[] args){
	//目标:更熟悉指标的基本用法
	
	System.out.println("name"+'\t'+"age");
	System.out.println("tom"+'\t'+"18");
	}
}
```

![image-20240414145525186](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240414145525186.png)

### 变量

变量:在程序执行过程中,其值有可能发生改变的量(数据)

---

####  1.变量的定义格式

> <font color='red'>数据类型 变量名=数据值;</font>
>
> 数据类型:为空间中存储的数据,加入类型[<font color='red'>限制</font>]整数?小数?...
>
> 变量名:为空间(小箱子)起的名字
>
> 数据值:存在空间里面的数值 

```java
public class valueDemo3{
	//主入口
	
	public static void main(String[]args){
		//定义变量
		//数据类型 变量名 =数据值;
		//数据类型:限定了变量能存储数据的类型
		//int(整数) double(小数)
		//变量名:就是存储空间的名字
		//作用:方便以后使用
		//数据值:真正存在变量中的数据
		
		//等号=赋值.把右边的数据赋值给左边的变量
		int age =19;
        System.out.println(age)	;	
	}
}
```

#### 2.变量的使用方法

---

##### 注意事项

###### 只能存在<font color='red'>一个值</font>

###### 变量名<font color='red'>不允许重复</font>定义

###### 一条语句<font color='red'>可以定义多个变量</font>

###### 变量在使用前<font color='red'>一定要进行赋值</font>

##### 1.输出打印

```java
int a = 10;
System.out.println(a);//10
```

##### 2.参与计算

```java
int a = 18;
int b = 12;
System.out.println(a+b);//30
```

##### 3.修改记录的值

```
int a = 10;
System.out.println(a);//10
a = 18;
System.out.println(a);//18
```

```
public class valueDemo4{
	//主入口
	
	public static void main(String[]args){
		//1.基本用法
		//定义变量,再进行输出
		int a = 10;
        System.out.println(a);	//10
		System.out.println(a);	//10
		System.out.println(a);	//10
		//2.变量参与计算
		int c =20;
		int b=20;
		System.out.println(c+b);
		//3.修改变量记录的值
		a = 50;
		System.out.println(a);//50
		System.out.println("------------");
		//注意事项
		//在一条语句中,可以使用多个变量
		int d = 100, e = 200, f = 300;
		System.out.println(d);
		System.out.println(e);
		System.out.println(f);
		System.out.println(d+e+f);
		
		//变量在使用之前必须要赋值
		//int = g;
		//g = 500;
		//建议:以后在定义变量的时候,请直接赋值
		//不要把赋值分开写.
		System.out.println(g);
	}
}
```

![image-20240414154900590](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240414154900590.png)

#### 3.使用场景

##### 重复使用某个值

##### 某个数据经常发生改变

#### 4.注意事项

##### 变量 只能存一个值

##### 变量名不能重复

##### 一条语句可以定义多个变量

##### 使用之前一定要赋值

#### 变量的练习(公交车)

----

##### 题目

```typescript
	//一开始没有乘客
	//第一站:上去一位乘客
	//第二站:上去两位乘客,下去一位乘客	
	//第三站:上去两位乘客.下去一位乘客
	//第四站:下去一位乘客
	//第五站:上去一位乘客
	//请问:到了终点站,车上还有几位乘客.
```

解答

```
public class VariableTest{
	//主入口
	public static void main(String[] args){
		//一开始没有乘客
		int count = 0;
		//第一站:上去一位乘客
		//在原有的基础上+1
		count = count + 1;
		//第二站:上去两位乘客,下去一位乘客
		//在原有的基础上+2-1,然后在赋值给count
		count = count+2-1;
		//第三站:上去两位乘客.下去一位乘客
		count = count+2-1;
		//第四站:下去一位乘客
		count = count-1;
		//第五站:上去一位乘客
		count = count+1;
		//请问:到了终点站,车上还有几位乘客.
		System.out.println(count);//3
		}
}
```

### 数据类型

#### 1.基本数据类型

<table>
    <tr>
        <td>数据类型</td>
        <td>关键字</td>
        <td>取值范围</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>整数</td>
        <td>byte</td>
        <td>-128~127</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>整数</td>
        <td>short</td>
        <td>-32768~32767</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>整数</td>
        <td>int</td>
        <td>-2.147483648~2147483647(10位数)</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>整数</td>
        <td>long</td>
        <td>-9223372036854775808~9223372036854775807(19位数)</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>浮点数</td>
        <td>float</td>
        <td>-3.401298e-324到1.797693e+308</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>字符</td>
        <td>char</td>
        <td>0-65535</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>布尔</td>
        <td>boolean</td>
        <td>true,false</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
</table>


```java
public class VariableDemo1{
	//主入口
	public static void main(String[] args){
		//byte
		byte b = -52;
		System.out.println(b);
		//short
		short s = 5625;
		System.out.println(s);
		//int
		int a = 1952;
		System.out.println(a);
		//long
		//数值后面要加L大小写都可以
		//推荐大写方便区分
		long l = 156325463L;
		System.out.println(l);
		//float
		//数值后面要加F
		float f = 1.6586F;
		System.out.println(f);
		//char
		char c = '航';
		System.out.println(c);
		//boolean
		boolean o = true;
		System.out.println(o);
	}
}
```

---

##### 整数和小数取值范围大小关系

![image-20240415122959158](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240415122959158.png)

##### **练习**

###### 练习1

![image-20240415123128282](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240415123128282.png)

```java
public class VariableTest1{
	//主入口
	public static void main (String[]args){
		//使用string定义name变量
		String name = "黑马谢广坤";
		System.out.println("姓名:"+name);
		//使用int定义age变量
		int age = 18;
		System.out.println("年龄:"+age);
		//使用char定义gender
		char gender = '男';
		System.out.println("性别:"+gender);
		//使用doulbe定义height
		double height = 178.9;
		System.out.println("身高:"+height);
		//使用bollean定义ds
		boolean ds = true;
		System.out.println("是否单身:"+ds);
	}
}
```



###### 练习2

![image-20240415125816010](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240415125816010.png)

```java
public class VariableTest2{
	//主入口
	public static void main (String[]args){
		//使用String定义test
		String test = "送初恋回家";
		//使用String定义name
		String name = "刘鑫 张雨提 高媛";
		//使用int定义years
		int years = 2020;
		//使用double定义score
		double score = 9.0;
		System.out.println("电影名称:"+test);
		System.out.println("主演:"+name);
		System.out.println("年份:"+years);
		System.out.println("评分:"+score);
	}
}
```

###### 练习3

![image-20240415134252922](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240415134252922.png)

```java
public class VariableTest3{
	//主入口
	public static void main (String[]args){
	//定义手机价格
	double price = 2599.00;
	//定义手机品牌
	String name = "华为";
	System.out.println("手机价格:"+price);
	System.out.println("手机品牌:"+name);
	}
}
```



#### 2.引用数据类型

### 标识符

---

标识符:就是给类 方法 变量等起名字

<font color='red'>由数字,字母下划线_和美元$组成</font>

<font color='red'>不能以数字开头</font>

<font color='red'>不能是关键字</font>

<font color='red'>区分大小写</font>

---

小驼峰![image-20240415140603137](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240415140603137.png)

大驼峰

![image-20240415140851292](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240415140851292.png)

### 键盘录入Scanner

第一套体系

```
nextint();接收整数
nextdouble();接收小数
next();接收字符串
```

```
第二套
nextline();结合搜字符串
```



#### 步骤一:导包---Scanner这个类在哪

```java
import java.util.Scanner;		//导包的动作必须出现在类定义的上边.
```

#### 步骤二:创建对象---表示我要开始用Scanner这个类了

```java
Scanner sc = new Scanner(System.in);
//上面这个格式里面,只有sc是变量名,可以改变,其他的都可以变
```

#### 步骤三:接受数据---真正开始干活了

```java
int i = sc.nextInt();
//这个格式里面,只有i是变量,可以变,其他的都不允许变.
```



例子

```java
	//导包
	import java.util.Scanner;
public class ScannerDemo1{
	public static void main(String[] args){
		//导包
		
		//创建对象
		Scanner sc = new Scanner(System.in);
		//提示防止你不知道在做什么
		System.out.println("请输入整数");
		int i = sc.nextInt();
		System.out.println(i);
	}
}
```

##### 练习

<font color='red'>键盘录入两个整数,求他们的和并打印出来</font>

```java
import java.util.Scanner;
public class ScannerTest{
	public static void main(String[] args){
		//导包
		//创建对象
		Scanner sc = new Scanner(System.in);
		System.out.println("请输入第一个数字");
		//接受数据
		int number1 = sc.nextInt();
		System.out.println("请输入第二个数字");
		int number2 = sc.nextInt();
			System.out.println(number1+number2);
		
	}
}
```

### 运算符

---

运算符优先级

#### 1.算术运算符

---

```
+	加
-	减
*	乘
/	除
%	取余,取模
```



##### 隐式转换

---

![image-20240416081413775](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240416081413775.png)

##### 强制转换

a=97 A=65

#### 2.自增自减运算符

![image-20240416085357634](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240416085357634.png)

![image-20240416090252134](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240416090252134.png)

#### 3.赋值运算符

![image-20240416090826361](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240416090826361.png)

#### 4.关系运算符

![image-20240416094331027](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240416094331027.png)

练习

![image-20240416101428973](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240416101428973.png)

```
package com.Compare1.a;

import java.util.Scanner;

public class lianxi {
    public static void main(String[] args) {
        //键盘录入
        Scanner sc = new Scanner(System.in);
        System.out.println("请输入你的衣服时髦度");
        int me = sc.nextInt();
        System.out.println("请输入相亲对象的时髦度");
        int dx = sc.nextInt();
        System.out.println("相亲"+(me > dx));

    }
}

```



#### 5.逻辑运算符

![image-20240416102955465](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240416102955465.png)

```
&
```

![image-20240416105302134](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240416105302134.png)

练习

```
package com.Compare1.a;

import java.sql.SQLOutput;
import java.util.Scanner;

public class lianxi2 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("请输入第一个数");
        int numb1 = sc.nextInt();
        System.out.println("请输入第二");
        int numb2 = sc.nextInt();
        boolean result = numb1 == 6 || numb2 == 6 || (numb1+numb2) % 6 ==0;
        System.out.println(result);

    }

}


```



#### 6.三元运算符

---

格式:关系表达式?表达式1:表达式2;

```
条件 ? 表达式1 : 表达式2
如果条件为真，则整个表达式的值为表达式1的值。
如果条件为假，则整个表达式的值为表达式2的值。
```



```
package com.Compare1.a.com.max;

import java.util.Scanner;

public class max {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("请输入第一个值");
        int number1 = sc.nextInt();
        System.out.println("请输入第二个值");
        int number2 = sc.nextInt();
        int max = number1 > number2 ? number1 : number2;
        System.out.println(max);


    }
}
```

![image-20240416114712100](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240416114712100.png)

### 流程控制语句

#### if

```
if (条件) {
    // 如果条件为真，则执行这里的代码块
} else if (另一个条件) {
    // 如果上面的条件为假，且另一个条件为真，则执行这里的代码

```



![image-20240416162803833](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240416162803833.png)

if嵌套

```java
if(){
if(){

}else{

}
}else{

}
```

![image-20240417222236497](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240417222236497.png)

#### Switch

```
switch (表达式) {
    case 值1:
        // 当表达式的值等于值1时执行的代码
        break;
    case 值2:
        // 当表达式的值等于值2时执行的代码
        break;
    // 可以有多个 case 分支
    default:
        // 如果表达式的值不匹配任何 case 分支时执行的代码
}

```



![image-20240418072447056](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240418072447056.png)



#### for

```java
for (初始化语句; 条件判断语句;条件控制语句) {
	循环语句;	
}
```



#### while

格式

```
while(条件判断语句){
循环语句;
条件控制语句
}
```

#### for和while对比

相同点:运行规则一样

不同点:<font color='red'>for循坏</font>中,控制循环的变量,因为for循环的语法结构中,在for循环中就结束了,就不能再次被访问到了

<font color='red'>while循坏</font>中,控制循环的变量,对于while循环来说不归属其语法中,在while循环结束后,该变量还可以继续使用

``

#### do..while

```java
do {
    // 循环体内的代码
} while (条件);

```

```
首先执行循环体内的代码。
执行完一次循环后，检查条件。
如果条件为真，则继续执行循环体内的代码，并继续进行下一次循环。
如果条件为假，则退出循环，继续执行循环体外的代码。
下面是一个简单的示例，演示了如何使用 do...while 循环：
public class DoWhileExample {
    public static void main(String[] args) {
        int i = 1;
        
        // 打印出1到5的数字
        do {
            System.out.println(i);
            i++;
        } while (i <= 5);
    }
}

```

#### 无限循环

for

```
for (;;) {
    // 循环体内的代码
}

```

while

```
while (true) {
    // 循环体内的代码
}

```

```
do...while
```

```
do {
    // 循环体内的代码
} while (true);


```

### `continue`

```
for (int i = 0; i < 10; i++) {
    if (i % 2 == 0) {
        continue; // 当 i 为偶数时，跳过本次循环的剩余代码，继续下一次循环
    }
    System.out.println(i);
}

```

#### 质数

```
public class nozhi {
    public static void main(String[] args) {
        //判断一个数是不是质数,要看他能不能被其他数整除
        //4 2*2 1*4
        //键盘录入一个数字
        Scanner sc = new Scanner(System.in);
        System.out.println("请输入一个整数");
        int number = sc.nextInt();
        //定义标点
        boolean flog = true;
        //对number进行判断
        for (int i = 2; i <= number-1; i++){
            if (number % i == 0){
                //如果能被整数那么他不上质数
                flog = false;
                //System.out.println(number+"不是一个质数");
                break;
            }
        }
        if (flog){
            System.out.println(number+"是质数");
        }else {
            System.out.println(number+"不是一个质数");
        }

    }

}

```

### 随机数Random

---

秘诀用来生成任意数

比如我要随机生成7~15

1.让这个范围头尾都减去一个值,让这个值的范围从0开始-7  范围就是0~8

2.尾巴+1 8+1=9

3.最终结果,再加上第一不减去的值

那么最终结果就是 int number =random.nextInt(bound :9)+7

```
public class suijishu {
    public static void main(String[] args) {
        Random random = new Random();
        Scanner sc = new Scanner(System.in);
        int randomNumber = random.nextInt(100);
        System.out.println("请输入一个数字来猜数");
        int number = sc.nextInt();
        System.out.println("已为你生成");
        System.out.println("正在为你进行判断");
        //System.out.println("该提示是用来验证的随机数"+randomNumber);
        while(number != randomNumber) {
            if(number > randomNumber) {
                System.out.println("你输入的数字太大了");
                //重新输入数字
                System.out.println("请重新输入一个比"+number+"小的数字");
                number= number = sc.nextInt();
                break;
            }else{
                System.out.println("你输入的数字太小了");
                System.out.println("请输入一个比"+number+"大的数字");
                number= number = sc.nextInt();
            }
        }{
            System.out.println("你输入的数字正确了");
        }
    }

}
```

## 数组

---

数组指的是一种容器,可以用来存储<font color='red'>同种数据类型</font>的多个值

<font color='green'>建议:容器类型和存储数据类型一致</font>

#### 定义

 格式一

---

数据类型 []数组名

范例:int []array

格式二

---

数据类型 数组名[]

int	arry[]

#### 数据初始化有两种

#### 静态初始化

完整格式:数据类型[]数组名=new 数据类型[]{元素1,元素2 ,元素3...}

简化版int[]arry={11,22,33};

int[] array=new int[]{11,22,33};

double[]array2=new double[]{11.1,22.2,33.3};

地址值的格式[D@776ec8df

[表示当前是一个数组

D表示数组里面的元素都是double类型的

@表示一个间隔符号

776ec8df是真正的地址值(十六进制)

###### 动态初始化

#### 数组元素的访问

#### 格式:数组名[索引];

调用数组长度

格式:数组名.length

快速生成数组遍历方式

格式数组名.fori

#### 数据存储到数组中

格式:数组名[索引]=具体数据/变量;

索引:也叫做下标,角标

索引的特点:从0开始,逐个+1增长,连续不间断

#### 动态初始化

格式itn[]arr=new int[3];

#### 数组动态初始化和静态初始化有啥区别

##### 动态初始化:手动指定数组长度,系统给默认值

---

<font color='red'>明确</font>元素个数,不明确具体数值,推荐使用动态



###### 静态初始化:手动指定元素,系统会根据元素个数,计算数组长度

---

需求中已明确了具体操作的具体数据,这直接静态初始化即可.

#### 常见问题

##### 数组越界

#### 常见操作

##### 求最大值

```java
package cmo.day05.com;

public class arr3 {
    public static void main(String[] args) {
        //定义一个数组35,5,22,44,55
        //遍历数组求最大值
        int[] arr ={35,5,22,44,55};
        int max = arr[0];
        for (int i = 0; i < arr.length; i++) {
            if(arr[i] >max){
                max = arr[i];
            }
        }
        System.out.println("最大值为"+max);
    }
}

```

---

##### 最小值

```java
package cmo.day05.com;

public class arr3 {
    public static void main(String[] args) {
        //定义一个数组35,5,22,44,55
        //遍历数组求最小值
        int[] arr ={35,5,22,44,55};
        int mmin = arr[0];
        for (int i = 0; i < arr.length; i++) {
            if(arr[i] <in){
                min = arr[i];
            }
        }
        System.out.println("最小值为"+min);
    }
}
```



##### 求和

```java
package cmo.day05.com;

import java.util.Random;

public class arr4 {
    public static void main(String[] args) {
        //生成10个1~100的随机数存入数组.
        //求出所有数据的和
        //求出所有数据的平均数
        //统计有多少个数据比平均值小
        Random rand = new Random();
        //随机1~100数字
        //int randomNum = rand.nextInt(100)+1;
        //定义一个动态数组10
        int [] arr = new int[10];
        //使用for循环把随机数写入数组
        for (int i = 0; i < arr.length; i++) {
            //数组写入随机数
            arr[i] =rand.nextInt(100)+1;
        }
        //求出所有数据的和
        //定义一个临时变量sum
        int sum = 0;
        for (int i = 0; i < arr.length; i++) {
            sum += arr[i];
        }
        System.out.println("数据的和为:"+sum);
        //求出所有数据的平均数
        //平均数pingjun
        double pingjun= sum/arr.length;
        System.out.println("所有数据的平均数为:"+pingjun);
        //统计有多少个数据比平均值小
        //定义一个临时变量min
        int min=0;
        for (int i = 0; i < arr.length; i++) {
            if(arr[i]<pingjun){
                min++;
            }

        }
        System.out.println("有"+min+"个数据比平均值小");
        System.out.println("遍历数组防止程序出错进行判断");
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i]+" ");

        }
    }
}

```



##### 交换数据

```java
package cmo.day05.com;

public class arr5 {
    public static void main(String[] args) {
        //首位交换
        int [] arr ={1,2,3,4,5};
        for (int i =0,j =arr.length-1; i<j;i++,j--) {
            int temp = arr[i];
            arr[i] = arr[j];
            arr[j] = temp;
        }
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");

        }
    }
}

```



##### 打乱数据

---

```java
package cmo.day05.com;

import java.util.Random;

public class arr6 {
    public static void main(String[] args) {
        //随机打乱数组中的顺序
        //随机需要用到随机数
        Random rand = new Random();

        int[] arr = {1, 2, 3, 4, 5};
        for (int i = 0; i < arr.length; i++) {
            //定义一个临时变量
            //定义一个随机数
            int randnumber = rand.nextInt(arr.length);
            int temp = arr[i];
            arr[i] = arr[randnumber];
            arr[randnumber] = temp;
        }
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i]);

        }

    }
}

```

#### Java内存分配

![image-20240419225016711](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240419225016711.png)

- #### 栈

  ---

  方法运行时使用的内存,比如main方法运行,进入方法栈中执行

- 堆

  存储对象或者数组,new来创建的,都存储在堆内存中

- 方法区

  存储可以运行的class文件

- 本地方法栈

  jvm在使用操作系统功能的时候使用,和我们开发无关

- 寄存器

  给cpu使用的,和我们开发无关

##### 总结

![image-20240419225611829](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240419225611829.png)

1. 只要是new出来的一定是在堆里面开辟了一个小空间
2. 如果new了多次,那么在堆里面有多个小空间,每个小空间中都有各自的数据
3. 当两个数组指向同一个小空间是,其中一个数组对小空间的值发生了改变,那么其他数组再次访问的时候都是修改之后的结果

## 3.方法

### 1什么是方法

方法(method)是程序中最小的执行单元.

```java
public static void main(String[] args) {

    }
    main就是方法
```

---

什么时候使用方法

重复的代码.具有独立功能的代码可以抽取到方法中

---

##### 方法的好处

可以提高代码的复用性

可以提高代码的维护性

### 方法的格式 

#### 最简单的方法定义格式和调用

##### 格式

```java
 public static void 方法名(){
 方法体(就是打包起来的代码)
 }
```

---

示例

```java
 public static void playGame(){
 七个打印语句;
 }
```

##### 调用

<font color='red'>先定义后调用</font>

```java
格式
	方法名();
```

范例

```
范例 
	playGame();
```



#### 带猜数的方法定义

---

<font color='red'>形参和实参</font>

形参:全程形式参数,是指方法定义中的参数

实参:全称实际参数,方法调用中的参数

<font color='red'>注意</font>

注意:方法调用时，参数的数量与类型必须与方法定义中小括号里面的变量一一对应，否则程序将报错。

格式

```java
 		单个猜数
public static void 方法名 (猜数){.....}
		范例
public static void method (int number){.....}
 		多个参数
public static void 方法名 (猜数,猜数,猜数){.....}
	范例
public static void method2(itn number1,int nuimber2){....}
```

---

调用

```
	单个参数
格式 方法名(参数);
method(10);
method(变量);
	多个参数
格式:方法名(参数1,参数2,参数3,...)
范例
getsum(10,20);
getsum(变量1,变量2);
```

<font color='red'>方法定义的小技巧</font>

1.我需要干什么     	<font color='red'>方法体</font>

2.我干这件事情需要做什么才能完成 	<font color='red'>形参</font>

#### 带返回值方法的定义

方法的返回值其实就是方法运行的最终结果

格式

```java
public static 返回值类型 方法名 (参数){
  方法体;
    return 返回值;
}
	范例
public static int sum (int number1 , int number2){
  int c = number1+number2;
    return c;
}
```

调用

```
1.直接调用:
方法名(实参);
2.赋值调用:
整数类型 变量名 = 方法名(实惨);
3.输出调用:
System.out.println(方法名 (实参));
```



方法的小结

```
public static 返回值类型 方法名 （参数）{
	方法体
	return 返回值;
}
```

方法的注意事项

方法不调用就不执行

方法与方法之间是平级关系,不能互相嵌套定义

方法的编写顺序和执行顺序无关

方法的返回值类型为void,表示方法没有返回值

没有返回值可以省略return语句不写.

如果要编写return,后面不能跟具体的数据

### 方法的重载

在一个统统类中,定义了多个<font color='red'>同名的方法</font>,这些同名的方法具有同体重的功能

每一方法具有<font color='red'>不同的参数类型或参数个数,</font>这些同名单方法就构成了重载

简单记忆:同一个类中,方法名相同,参数不同的方法.与返回值无关

参数不同:个数不同,类型不同,顺序不同

#### 方法的内存 

1.方法的调用的基本内存

2.方法传递基本数据类型的内存原理

![image-20240427181604831](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240427181604831.png)

基本数据类型

整数类型

浮点数类型

布尔类型

字符串类型

二维数组的静态初始化

格式:数据类型[ ][ ]数组名=new 数组类型[][]{{元素1,元素2},{元素1,元素2;};

范例

int[][]arr=new [] [] {11,22},{33,44};

![image-20240429101420083](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240429101420083.png)

二维数组的动态初始化

![image-20240429103619205](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240429103619205.png)

![image-20240429104454364](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240429104454364.png)

![image-20240429104715874](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240429104715874.png)

练习

![image-20240429110221637](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240429110221637.png)

```java
package Overloaded;

import java.time.YearMonth;

public class Twodimensional {
    public static void main(String[] args) {
        //第一个季度:22,66,44
        //第二个季度:77,33,88
        //第三个季度:25,45,65
        //第四个季度:11,66,99
        //要求计算出每个季度的总营业额和全年的总营业额
        //定义二维数组
        int[][] yeararr = {
                {22, 66, 44},
                {77, 33, 88},
                {25, 45, 65},
                {11, 66, 99}
        };
        //求每个季度的营业额
        for (int i = 0; i < yeararr.length; i++) {
            //创建一个一维数组来接受
            int[] quartearr= yeararr[i];
            int sum=getSum(quartearr);
            System.out.println("第"+(i+1)+"个季度的营业额为"+sum+"元");
        }
        System.out.println("年营业额为"+getyearsum(yeararr));
    }
    //求个季度的营业额
    public static int getSum(int[]arr){
        int sum = 0;
        for(int i=0; i<arr.length; i++){
            sum += arr[i];
        }
        return sum;
    }
    //求年营业额
    public static int getyearsum(int[][]yeararr){
        //年营业额
        int yearsum = 0;
        for (int i = 0; i < yeararr.length; i++) {
            yearsum=yearsum+getSum(yeararr[i]);
        }
        return yearsum;
    }
}

```

## 面向对象

![image-20240429112034481](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240429112034481.png)

### 设计对象并使用.

#### 类(设计图):是对象共同特征的描述;

#### 对象:是真实存在的具体东西.   

#### 定义类的补充注意事项

#### 用来秒速一类事物的类,专业叫做:<font color='red'>Javabean类</font>

#### 在javabean类中,是不写main方法的

---

在以前,编写main方法的类,叫做<font color='red'>测试类</font>

我们可以在测试类中创建javabean类的对象并进行赋值调用

---

<font color='red'>类名首字母建议大写</font>,需要见名知意,驼峰模式

一个java文件中可以定义多个class类,且只能一个类是public修饰,而且public修饰的类名必须为文件名   <font color='red'>实际开发中建议还是一个文件定义一个class类</font>

成员变量的完整定义格式是:<font color='red'>修饰符 数据类型 变量名称 =初始值</font>;一般无需直指定初始化值,存在默认值

![image-20240429113502187](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240429113502187.png)  

#### 1.类和对象是什么

类:是共同特征的描述(设计图);对象:是真实存在的具体示例;

#### 2.如何得到对象

```
public class 类名{
	1.成员变量(代表属性,一般是名词)
	2.成员方法(代表行为,一般是动词)
}
```

<font color='red'>类名 对象名=new 类名();</font>

### 开发中类的设计

 

### 封装

---

告诉我们,如何<font color='red'>正确设计对象的属性和方法</font>

---

对象代表什么,就得封装对应的数据,并提供数据对应的行为

### private关键字

是一个权限修饰符

可以修饰成员(成员变量和成员方法)

被<font color='red'>private</font>修饰的成员只能在本类中才能访问

### this关键字(成员变量)

区分成员变量和局部变量

1.就近原则

---

```
```



### 构造方法

---

概念

创造对象的时候,虚拟机会自动调用构造方法,作用是给成员变量进行初始化的

作用:在创建对象的时候给成员变量进行赋值的.

构造方法的格式

注意事项

1.如果没有定义构造方法,系统将会给出一个<font color='red'>默认</font>的<font color='red'>无参数构造方法</font>

如果定义了构造方法,系统将会不在提供默认的构造方法

2.构造方法重载

带参构造方法,和无参数构造方法,两者方法名相同,但是参数不同,这叫做构造方法的重载

3.推荐使用方法

无论<font color='red'>是否使用</font>,都<font color='red'>手动书写无参数构造方法,和带全部参数的构造方法</font>

```
public class student{
	修饰符 类名(参数){
		方法体;
	}

}
```

<font color='red'>特点</font>

1.方法名与类名相同,大小写也要一致

2.没有返回值类型,连void都没有

3.没有具体的返回值(不能由return带回结果数据)

<font color='red'>执行时机</font>

1.创建对象的时候由虚拟机调用,不能手动调用构造方法

2.每创建一次对象,就会调用一次构造方法

![image-20240429135935289](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240429135935289.png)

### 标准javaBean

```
1.类名需要见名知意
2.成员变量使用private修饰
3.提供至少两个构造方法
无参构造方法
带全部参数构造方法
4.成员的方法
提供每一个成员的变量对应的setxxx()/getxxx()
如果还有其他行为,请提供写出
```

<font color='red'>基本数据类型</font>:数据值是存储在自己的空间中

特点:赋值给其他变量,也是符的真实得知

<font color='red'>引用数据类型</font>:数据值是存储在其他空间中,自己空间中存储的是地址值

特点:赋值给其他变量,付的地址值

### 对象内存图

### 补充知识:成员变量,局部变量

 ![image-20240429190122154](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240429190122154.png)
