# JS基本语法
## 1. 语句：
JavaScript 程序的执行单位为行（line），也就是一行一行地执行。一般情况下，每一行就是一个语句。
语句（statement）是为了完成某种任务而进行的操作，比如下面就是一行赋值语句。
    
    var a = 1 + 3
    
    这条语句先用var命令，声明了变量a，然后将1 + 3的运算结果赋值给变量a。
1 + 3叫做表达式（expression），指一个为了得到返回值的计算式。语句和表达式的区
别在于，前者主要为了进行某种操作，一般情况下不需要返回值；后者则是为了得到返回值，
一定会返回一个值。凡是 JavaScript 语言中预期为值的地方，都可以使用表达式。比如，
赋值语句的等号右边，预期是一个值，因此可以放置各种表达式。
## 2. 标识符：
标识符（identifier）指的是用来识别各种值的合法名称。最常见的标识符就是变量名，
以及后面要提到的函数名。JavaScript 语言的标识符对大小写敏感，所以a和A是两个不同的标识符。
标识符有一套命名规则，不符合规则的就是非法标识符。JavaScript 引擎遇到非法标识符，就会报错。
简单说，标识符命名规则如下。
* 第一个字符，可以是任意 Unicode 字母（包括英文字母和其他语言的字母），以及美元符号（$）和下划线（_）。
* 第二个字符及后面的字符，除了 Unicode 字母、美元符号和下划线，还可以用数字0-9。
* JavaScript 有一些保留字，不能用作标识符：arguments、break、case、catch、class、const、continue、
debugger、default、delete、do、else、enum、eval、export、extends、false、finally、for、function、
if、implements、import、in、instanceof、interface、let、new、null、package、private、protected、
public、return、static、super、switch、this、throw、true、try、typeof、var、void、while、with、yield。
## 3.注释：
源码中被 JavaScript 引擎忽略的部分就叫做注释，它的作用是对代码进行解释。JavaScript 提供两种注释的写法：一种是单行注释，用//起头；另一种是多行注释，放在/*和*/之间。
## if else 语句：
if代码块后面，还可以跟一个else代码块，表示不满足条件时，所要执行的代码。
````    
    if (m === 3) {
  // 满足条件时，执行的语句
} else {
  // 不满足条件时，执行的语句
}
````

## while for 语句：
1. While语句包括一个循环条件和一段代码块，只要条件为真，就不断循环执行代码块。
````
    while (条件)
    语句;

    // 或者
    while (条件) 语句;
````

2. for语句是循环命令的另一种形式，可以指定循环的起点、终点和终止条件。它的格式如下。

````
    for (初始化表达式; 条件; 递增表达式)
    语句

    // 或者

    for (初始化表达式; 条件; 递增表达式) {
      语句
    }
````


    
### for语句后面的括号里面，有三个表达式。
* 初始化表达式（initialize）：确定循环变量的初始值，只在循环开始时执行一次。
* 条件表达式（test）：每轮循环开始时，都要执行这个条件表达式，只有值为真，才继续进行循环。
* 递增表达式（increment）：每轮循环的最后一个操作，通常用来递增循环变量。
## break 语句和 continue 语句:
break语句和continue语句都具有跳转作用，可以让代码不按既有的顺序执行。
* break语句用于跳出代码块或循环。
* continue语句用于立即终止本轮循环，返回循环结构的头部，开始下一轮循环。
## 标签（label）:
JavaScript 语言允许，语句的前面有标签（label），相当于定位符，用于跳转到程序的任意位置，标签的格式如下。

````
    label:
    语句
````

标签也可以用于跳出代码块

````
    foo: {
   console.log(1);
   break foo;
   console.log('本行不会输出');
    }
    console.log(2);
````
上面代码执行到break foo，就会跳出区块。









    

    
    
