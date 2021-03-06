#### JavaScript教程

这是小白的零基础JavaScript全栈教程。

JavaScript是世界上最流行的脚本语言，因为你在电脑、手机、平板上浏览的所有的网页，以及无数基于HTML5的手机App，交互逻辑都是由JavaScript驱动的。

简单地说，JavaScript是一种运行在浏览器中的解释型的编程语言。

那么问题来了，为什么我们要学JavaScript？尤其是当你已经掌握了某些其他编程语言如Java、C++的情况下。

简单粗暴的回答就是：因为你没有选择。在Web世界里，只有JavaScript能跨平台、跨浏览器驱动网页，与用户交互。

Flash背后的ActionScript曾经流行过一阵子，不过随着移动应用的兴起，没有人用Flash开发手机App，所以它目前已经边缘化了。相反，随着HTML5在PC和移动端越来越流行，JavaScript变得更加重要了。并且，新兴的Node.js把JavaScript引入到了服务器端，JavaScript已经变成了全能型选手。

JavaScript一度被认为是一种玩具编程语言，它有很多缺陷，所以不被大多数后端开发人员所重视。很多人认为，写JavaScript代码很简单，并且JavaScript只是为了在网页上添加一点交互和动画效果。

但这是完全错误的理解。JavaScript确实很容易上手，但其精髓却不为大多数开发人员所熟知。编写高质量的JavaScript代码更是难上加难。

一个合格的开发人员应该精通JavaScript和其他编程语言。如果你已经掌握了其他编程语言，或者你还什么都不会，请立刻开始学习JavaScript，不要被Web时代所淘汰。

等等，你会问道，现在有这么多在线JavaScript教程和各种从入门到精通的JavaScript书籍，为什么我要选择这个教程？

原因是，这个教程：

### 是JavaScript全栈教程！

 

#### **JavaScript简介**

阅读: 66255

 

### JavaScript历史

要了解JavaScript，我们首先要回顾一下JavaScript的诞生。

在上个世纪的1995年，当时的网景公司正凭借其Navigator浏览器成为Web时代开启时最著名的第一代互联网公司。

由于网景公司希望能在静态HTML页面上添加一些动态效果，于是叫Brendan Eich这哥们在两周之内设计出了JavaScript语言。你没看错，这哥们只用了10天时间。

为什么起名叫JavaScript？原因是当时Java语言非常红火，所以网景公司希望借Java的名气来推广，但事实上JavaScript除了语法上有点像Java，其他部分基本上没啥关系。

### ECMAScript

因为网景开发了JavaScript，一年后微软又模仿JavaScript开发了JScript，为了让JavaScript成为全球标准，几个公司联合ECMA（European Computer Manufacturers Association）组织定制了JavaScript语言的标准，被称为ECMAScript标准。

所以简单说来就是，ECMAScript是一种语言标准，而JavaScript是网景公司对ECMAScript标准的一种实现。

那为什么不直接把JavaScript定为标准呢？因为JavaScript是网景的注册商标。

不过大多数时候，我们还是用JavaScript这个词。如果你遇到ECMAScript这个词，简单把它替换为JavaScript就行了。

### JavaScript版本

JavaScript语言是在10天时间内设计出来的，虽然语言的设计者水平非常NB，但谁也架不住“时间紧，任务重”，所以，JavaScript有很多设计缺陷，我们后面会慢慢讲到。

此外，由于JavaScript的标准——ECMAScript在不断发展，最新版ECMAScript 6标准（简称ES6）已经在2015年6月正式发布了，所以，讲到JavaScript的版本，实际上就是说它实现了ECMAScript标准的哪个版本。

由于浏览器在发布时就确定了JavaScript的版本，加上很多用户还在使用IE6这种古老的浏览器，这就导致你在写JavaScript的时候，要照顾一下老用户，不能一上来就用最新的ES6标准写，否则，老用户的浏览器是无法运行新版本的JavaScript代码的。

不过，JavaScript的核心语法并没有多大变化。我们的教程会先讲JavaScript最核心的用法，然后，针对ES6讲解新增特性。

 

#### 快速入门

阅读: 70610

 

JavaScript代码可以直接嵌在网页的任何地方，不过通常我们都把JavaScript代码放到<head>中：

<html><head>

  <script>

​    alert('Hello, world');

  </script></head><body>

  ...</body></html>

由<script>...</script>包含的代码就是JavaScript代码，它将直接被浏览器执行。

第二种方法是把JavaScript代码放到一个单独的.js文件，然后在HTML中通过<script src="..."></script>引入这个文件：

<html><head>

  <script src="/static/js/abc.js"></script></head><body>

  ...</body></html>

这样，/static/js/abc.js就会被浏览器执行。

把JavaScript代码放入一个单独的.js文件中更利于维护代码，并且多个页面可以各自引用同一份.js文件。

可以在同一个页面中引入多个.js文件，还可以在页面中多次编写<script> js代码... </script>，浏览器按照顺序依次执行。

有些时候你会看到<script>标签还设置了一个type属性：

<script type="text/javascript">

  ...</script>

但这是没有必要的，因为默认的type就是JavaScript，所以不必显式地把type指定为JavaScript。

### 如何编写JavaScript

可以用任何文本编辑器来编写JavaScript代码。这里我们推荐以下几种文本编辑器：

#### Sublime Text

免费，但不注册会不定时弹出提示框。

#### Notepad++

免费

注意：不可以用Word或写字板来编写JavaScript或HTML，因为带格式的文本保存后不是纯文本文件，无法被浏览器正常读取。

### 如何运行JavaScript

要让浏览器运行JavaScript，必须先有一个HTML页面，在HTML页面中引入JavaScript，然后，让浏览器加载该HTML页面，就可以执行JavaScript代码。

你也许会想，直接在我的硬盘上创建好HTML和JavaScript文件，然后用浏览器打开，不就可以看到效果了吗？

这种方式运行部分JavaScript代码没有问题，但由于浏览器的安全限制，以file://开头的地址无法执行如联网等JavaScript代码，最终，你还是需要架设一个Web服务器，然后以http://开头的地址来正常执行所有JavaScript代码。

不过，开始学习阶段，你无须关心如何搭建开发环境的问题，我们提供在页面输入JavaScript代码并直接运行的功能，让你专注于JavaScript的学习。

试试直接点击“Run”按钮执行下面的JavaScript代码：

窗体顶端

// 以//开头直到行末的是注释，将被浏览器忽略

// 第一个JavaScript代码:

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2C48.tmp.png) Run

窗体底端

浏览器将弹出一个对话框，显示“Hello, world”。你也可以修改两个单引号中间的内容，再试着运行。

### 调试

俗话说得好，“工欲善其事，必先利其器。”，写JavaScript的时候，如果期望显示ABC，结果却显示XYZ，到底代码哪里出了问题？不要抓狂，也不要泄气，作为小白，要坚信：JavaScript本身没有问题，浏览器执行也没有问题，有问题的一定是我的代码。

如何找出问题代码？这就需要调试。

怎么在浏览器中调试JavaScript代码呢？

首先，你需要安装Google Chrome浏览器，Chrome浏览器对开发者非常友好，可以让你方便地调试JavaScript代码。从这里[下载Chrome浏览器](https://www.google.com/chrome/browser/desktop/index.html?system=true&standalone=1)。打开网页出问题的童鞋请移步[国内镜像](#path=/chrome)。

安装后，随便打开一个网页，然后点击菜单“查看(View)”-“开发者(Developer)”-“开发者工具(Developer Tools)”，浏览器窗口就会一分为二，下方就是开发者工具：

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2C58.tmp.png)

先点击“控制台(Console)“，在这个面板里可以直接输入JavaScript代码，按回车后执行。

要查看一个变量的内容，在Console中输入console.log(a);，回车后显示的值就是变量的内容。

关闭Console请点击右上角的“×”按钮。请熟练掌握Console的使用方法，在编写JavaScript代码时，经常需要在Console运行测试代码。

如果你对自己还有更高的要求，可以研究开发者工具的“源码(Sources)”，掌握断点、单步执行等高级调试技巧。

### 练习

打开[新浪首页](http://www.sina.com.cn/)，然后查看页面源代码，找一找引入的JavaScript文件和直接编写在页面中的JavaScript代码。然后在Chrome中打开开发者工具，在控制台输入console.log('Hello');，回车查看JavaScript代码执行结果。

 

 

#### 基本语法

阅读: 63108

 

### 语法

JavaScript的语法和Java语言类似，每个语句以;结束，语句块用{...}。但是，JavaScript并不强制要求在每个语句的结尾加;，浏览器中负责执行JavaScript代码的引擎会自动在每个语句的结尾补上;。

注意：让JavaScript引擎自动加分号在某些情况下会改变程序的语义，导致运行结果与期望不一致。在本教程中，我们不会省略;，所有语句都会添加;。

例如，下面的一行代码就是一个完整的赋值语句：

**var** x = 1;

下面的一行代码是一个字符串，但仍然可以视为一个完整的语句：

'Hello, world';

下面的一行代码包含两个语句，每个语句用;表示语句结束：

**var** x = 1; **var** y = 2; *// 不建议一行写多个语句!*

语句块是一组语句的集合，例如，下面的代码先做了一个判断，如果判断成立，将执行{...}中的所有语句：

**if** (2 > 1) {

​    x = 1;

​    y = 2;

​    z = 3;

}

注意花括号{...}内的语句具有缩进，通常是4个空格。缩进不是JavaScript语法要求必须的，但缩进有助于我们理解代码的层次，所以编写代码时要遵守缩进规则。很多文本编辑器具有“自动缩进”的功能，可以帮助整理代码。

{...}还可以嵌套，形成层级结构：

**if** (2 > 1) {

​    x = 1;

​    y = 2;

​    z = 3;

​    **if** (x < y) {

​        z = 4;

​    }

​    **if** (x > y) {

​        z = 5;

​    }

}

JavaScript本身对嵌套的层级没有限制，但是过多的嵌套无疑会大大增加看懂代码的难度。遇到这种情况，需要把部分代码抽出来，作为函数来调用，这样可以减少代码的复杂度。

### 注释

以//开头直到行末的字符被视为行注释，注释是给开发人员看到，JavaScript引擎会自动忽略：

*// 这是一行注释*

alert('hello'); *// 这也是注释*

另一种块注释是用/*...*/把多行字符包裹起来，把一大“块”视为一个注释：

*/\* 从这里开始是块注释*

*仍然是注释*

*仍然是注释*

*注释结束 \*/*

练习：

分别利用行注释和块注释把下面的语句注释掉，使它不再执行：

窗体顶端

// 请注释掉下面的语句:

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2C59.tmp.png) Run

窗体底端

### 大小写

请注意，JavaScript严格区分大小写，如果弄错了大小写，程序将报错或者运行不正常。

 

#### 数据类型和变量

阅读: 60196

 

### 数据类型

计算机顾名思义就是可以做数学计算的机器，因此，计算机程序理所当然地可以处理各种数值。但是，计算机能处理的远不止数值，还可以处理文本、图形、音频、视频、网页等各种各样的数据，不同的数据，需要定义不同的数据类型。在JavaScript中定义了以下几种数据类型：

#### Number

JavaScript不区分整数和浮点数，统一用Number表示，以下都是合法的Number类型：

123; *// 整数123*0.456; *// 浮点数0.456*1.2345e3; *// 科学计数法表示1.2345x1000，等同于1234.5*

-99; *// 负数*NaN; *// NaN表示Not a Number，当无法计算结果时用NaN表示*Infinity; *// Infinity表示无限大，当数值超过了JavaScript的Number所能表示的最大值时，就表示为Infinity*

计算机由于使用二进制，所以，有时候用十六进制表示整数比较方便，十六进制用0x前缀和0-9，a-f表示，例如：0xff00，0xa5b4c3d2，等等，它们和十进制表示的数值完全一样。

Number可以直接做四则运算，规则和数学一致：

1 + 2; // 3

(1 + 2) * 5 / 2; // 7.52 / 0; // Infinity0 / 0; // NaN10 % 3; // 110.5 % 3; // 1.5

注意%是求余运算。

#### 字符串

字符串是以单引号'或双引号"括起来的任意文本，比如'abc'，"xyz"等等。请注意，''或""本身只是一种表示方式，不是字符串的一部分，因此，字符串'abc'只有a，b，c这3个字符。

#### 布尔值

布尔值和布尔代数的表示完全一致，一个布尔值只有true、false两种值，要么是true，要么是false，可以直接用true、false表示布尔值，也可以通过布尔运算计算出来：

**true**; // 这是一个**true**值**false**; // 这是一个**false**值2 > 1; // 这是一个**true**值2 >= 3; // 这是一个**false**值

&&运算是与运算，只有所有都为true，&&运算结果才是true：

**true** && **true**; // 这个&&语句计算结果为**truetrue** && **false**; // 这个&&语句计算结果为**falsefalse** && **true** && **false**; // 这个&&语句计算结果为**false**

||运算是或运算，只要其中有一个为true，||运算结果就是true：

**false** || **false**; // 这个||语句计算结果为**falsetrue** || **false**; // 这个||语句计算结果为**truefalse** || **true** || **false**; // 这个||语句计算结果为**true**

!运算是非运算，它是一个单目运算符，把true变成false，false变成true：

! **true**; // 结果为**false**

! **false**; // 结果为**true**

! (2 > 5); // 结果为**true**

布尔值经常用在条件判断中，比如：

**var** age = 15;**if** (age >= 18) {

​    alert('adult');

} **else** {

​    alert('teenager');

}

### 比较运算符

当我们对Number做比较时，可以通过比较运算符得到一个布尔值：

2 > 5; // **false**5 >= 2; // **true**7 == 7; // **true**

实际上，JavaScript允许对任意数据类型做比较：

**false** == 0; // **truefalse** === 0; // **false**

要特别注意相等运算符==。JavaScript在设计时，有两种比较运算符：

第一种是==比较，它会自动转换数据类型再比较，很多时候，会得到非常诡异的结果；

第二种是===比较，它不会自动转换数据类型，如果数据类型不一致，返回false，如果一致，再比较。

由于JavaScript这个设计缺陷，不要使用==比较，始终坚持使用===比较。

另一个例外是NaN这个特殊的Number与所有其他值都不相等，包括它自己：

NaN === NaN; *// false*

唯一能判断NaN的方法是通过isNaN()函数：

isNaN(NaN); // **true**

最后要注意浮点数的相等比较：

1 / 3 === (1 - 2 / 3); // **false**

这不是JavaScript的设计缺陷。浮点数在运算过程中会产生误差，因为计算机无法精确表示无限循环小数。要比较两个浮点数是否相等，只能计算它们之差的绝对值，看是否小于某个阈值：

Math.abs(1 / 3 - (1 - 2 / 3)) < 0.0000001; // **true**

#### null和undefined

null表示一个“空”的值，它和0以及空字符串''不同，0是一个数值，''表示长度为0的字符串，而null表示“空”。

在其他语言中，也有类似JavaScript的null的表示，例如Java也用null，Swift用nil，Python用None表示。但是，在JavaScript中，还有一个和null类似的undefined，它表示“未定义”。

JavaScript的设计者希望用null表示一个空的值，而undefined表示值未定义。事实证明，这并没有什么卵用，区分两者的意义不大。大多数情况下，我们都应该用null。undefined仅仅在判断函数参数是否传递的情况下有用。

#### 数组

数组是一组按顺序排列的集合，集合的每个值称为元素。JavaScript的数组可以包括任意数据类型。例如：

[1, 2, 3.14, 'Hello', null, true];

上述数组包含6个元素。数组用[]表示，元素之间用,分隔。

另一种创建数组的方法是通过Array()函数实现：

**new** **Array**(1, 2, 3); *// 创建了数组[1, 2, 3]*

然而，出于代码的可读性考虑，强烈建议直接使用[]。

数组的元素可以通过索引来访问。请注意，索引的起始值为0：

**var** arr = [1, 2, 3.14, 'Hello', null, true];

arr[0]; *// 返回索引为0的元素，即1*

arr[5]; *// 返回索引为5的元素，即true*

arr[6]; *// 索引超出了范围，返回undefined*

#### 对象

JavaScript的对象是一组由键-值组成的无序集合，例如：

**var** person = {

​    name: 'Bob',

​    age: 20,

​    tags: ['js', 'web', 'mobile'],

​    city: 'Beijing',

​    hasCar: true,

​    zipcode: null

};

JavaScript对象的键都是字符串类型，值可以是任意数据类型。上述person对象一共定义了6个键值对，其中每个键又称为对象的属性，例如，person的name属性为'Bob'，zipcode属性为null。

要获取一个对象的属性，我们用对象变量.属性名的方式：

person.name; // 'Bob'

person.zipcode; // null

### 变量

变量的概念基本上和初中代数的方程变量是一致的，只是在计算机程序中，变量不仅可以是数字，还可以是任意数据类型。

变量在JavaScript中就是用一个变量名表示，变量名是大小写英文、数字、$和_的组合，且不能用数字开头。变量名也不能是JavaScript的关键字，如if、while等。申明一个变量用var语句，比如：

**var** a; *// 申明了变量a，此时a的值为undefined***var** $b = 1; *// 申明了变量$b，同时给$b赋值，此时$b的值为1***var** s_007 = '007'; *// s_007是一个字符串***var** Answer = **true**; *// Answer是一个布尔值true***var** t = **null**; *// t的值是null*

变量名也可以用中文，但是，请不要给自己找麻烦。

在JavaScript中，使用等号=对变量进行赋值。可以把任意数据类型赋值给变量，同一个变量可以反复赋值，而且可以是不同类型的变量，但是要注意只能用var申明一次，例如：

**var** a = 123; *// a的值是整数123*

a = 'ABC'; *// a变为字符串*

这种变量本身类型不固定的语言称之为动态语言，与之对应的是静态语言。静态语言在定义变量时必须指定变量类型，如果赋值的时候类型不匹配，就会报错。例如Java是静态语言，赋值语句如下：

**int** a = 123; *// a是整数类型变量，类型用int申明*

a = "ABC"; *// 错误：不能把字符串赋给整型变量*

和静态语言相比，动态语言更灵活，就是这个原因。

请不要把赋值语句的等号等同于数学的等号。比如下面的代码：

**var** x = 10;

x = x + 2;

如果从数学上理解x = x + 2那无论如何是不成立的，在程序中，赋值语句先计算右侧的表达式x + 2，得到结果12，再赋给变量x。由于x之前的值是10，重新赋值后，x的值变成12。

### strict模式

JavaScript在设计之初，为了方便初学者学习，并不强制要求用var申明变量。这个设计错误带来了严重的后果：如果一个变量没有通过var申明就被使用，那么该变量就自动被申明为全局变量：

i = 10; // i现在是全局变量

在同一个页面的不同的JavaScript文件中，如果都不用var申明，恰好都使用了变量i，将造成变量i互相影响，产生难以调试的错误结果。

使用var申明的变量则不是全局变量，它的范围被限制在该变量被申明的函数体内（函数的概念将稍后讲解），同名变量在不同的函数体内互不冲突。

为了修补JavaScript这一严重设计缺陷，ECMA在后续规范中推出了strict模式，在strict模式下运行的JavaScript代码，强制通过var申明变量，未使用var申明变量就使用的，将导致运行错误。

启用strict模式的方法是在JavaScript代码的第一行写上：

'use strict';

这是一个字符串，不支持strict模式的浏览器会把它当做一个字符串语句执行，支持strict模式的浏览器将开启strict模式运行JavaScript。

来测试一下你的浏览器是否能支持strict模式：

窗体顶端

'use strict';

// 如果浏览器支持strict模式，

// 下面的代码将报ReferenceError错误:

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2C6A.tmp.png) Run

窗体底端

运行代码，如果浏览器报错，请修复后再运行。如果浏览器不报错，说明你的浏览器太古老了，需要尽快升级。

不用var申明的变量会被视为全局变量，为了避免这一缺陷，所有的JavaScript代码都应该使用strict模式。我们在后面编写的JavaScript代码将全部采用strict模式。

 

 

#### 字符串

阅读: 46290

 

JavaScript的字符串就是用''或""括起来的字符表示。

如果'本身也是一个字符，那就可以用""括起来，比如"I'm OK"包含的字符是I，'，m，空格，O，K这6个字符。

如果字符串内部既包含'又包含"怎么办？可以用转义字符\来标识，比如：

'I\'m \"OK\"!';

表示的字符串内容是：I'm "OK"!

转义字符\可以转义很多字符，比如\n表示换行，\t表示制表符，字符\本身也要转义，所以\\表示的字符就是\。

ASCII字符可以以\x##形式的十六进制表示，例如：

'\x41'; // 完全等同于 'A'

还可以用\u####表示一个Unicode字符：

'\u4e2d\u6587'; // 完全等同于 '中文'

由于多行字符串用\n写起来比较费事，所以最新的ES6标准新增了一种多行字符串的表示方法，用` ... `表示：

`这是一个

多行

字符串`;

练习：测试你的浏览器是否支持ES6标准，如果不支持，请把多行字符串用\n重新表示出来：

窗体顶端

// 如果浏览器不支持ES6，将报SyntaxError错误:

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2C6B.tmp.png) Run

窗体底端

字符串常见的操作如下：

**var** s = 'Hello, world!';

s.length; *// 13*

要获取字符串某个指定位置的字符，使用类似Array的下标操作，索引号从0开始：

**var** s = 'Hello, world!';

 

s[0]; *// 'H'*

s[6]; *// ' '*

s[7]; *// 'w'*

s[12]; *// '!'*

s[13]; *// undefined 超出范围的索引不会报错，但一律返回undefined*

需要特别注意的是，字符串是不可变的，如果对字符串的某个索引赋值，不会有任何错误，但是，也没有任何效果：

**var** s = 'Test';

s[0] = 'X';

alert(s); *// s仍然为'Test'*

JavaScript为字符串提供了一些常用方法，注意，调用这些方法本身不会改变原有字符串的内容，而是返回一个新字符串：

### toUpperCase

toUpperCase()把一个字符串全部变为大写：

**var** s = 'Hello';

s.toUpperCase(); *// 返回'HELLO'*

### toLowerCase

toLowerCase()把一个字符串全部变为小写：

**var** s = 'Hello';**var** lower = s.toLowerCase(); *// 返回'hello'并赋值给变量lower*

lower; *// 'hello'*

### indexOf

indexOf()会搜索指定字符串出现的位置：

**var** s = 'hello, world';

s.indexOf('world'); *// 返回7*

s.indexOf('World'); *// 没有找到指定的子串，返回-1*

### substring

substring()返回指定索引区间的子串：

**var** s = 'hello, world'

s.substring(0, 5); *// 从索引0开始到5（不包括5），返回'hello'*

s.substring(7); *// 从索引7开始到结束，返回'world'*

#### 数组

阅读: 50693

 

JavaScript的Array可以包含任意数据类型，并通过索引来访问每个元素。

要取得Array的长度，直接访问length属性：

**var** arr = [1, 2, 3.14, 'Hello', null, true];

arr.length; *// 6*

请注意，直接给Array的length赋一个新的值会导致Array大小的变化：

**var** arr = [1, 2, 3];

arr.length; *// 3*

arr.length = 6;

arr; *// arr变为[1, 2, 3, undefined, undefined, undefined]*

arr.length = 2;

arr; *// arr变为[1, 2]*

Array可以通过索引把对应的元素修改为新的值，因此，对Array的索引进行赋值会直接修改这个Array：

**var** arr = ['A', 'B', 'C'];

arr[1] = 99;

arr; *// arr现在变为['A', 99, 'C']*

请注意，如果通过索引赋值时，索引超过了范围，同样会引起Array大小的变化：

**var** arr = [1, 2, 3];

arr[5] = 'x';

arr; *// arr变为[1, 2, 3, undefined, undefined, 'x']*

大多数其他编程语言不允许直接改变数组的大小，越界访问索引会报错。然而，JavaScript的Array却不会有任何错误。在编写代码时，不建议直接修改Array的大小，访问索引时要确保索引不会越界。

### indexOf

与String类似，Array也可以通过indexOf()来搜索一个指定的元素的位置：

**var** arr = [10, 20, '30', 'xyz'];

arr.indexOf(10); *// 元素10的索引为0*

arr.indexOf(20); *// 元素20的索引为1*

arr.indexOf(30); *// 元素30没有找到，返回-1*

arr.indexOf('30'); *// 元素'30'的索引为2*

注意了，数字30和字符串'30'是不同的元素。

### slice

slice()就是对应String的substring()版本，它截取Array的部分元素，然后返回一个新的Array：

**var** arr = ['A', 'B', 'C', 'D', 'E', 'F', 'G'];

arr.slice(0, 3); *// 从索引0开始，到索引3结束，但不包括索引3: ['A', 'B', 'C']*

arr.slice(3); *// 从索引3开始到结束: ['D', 'E', 'F', 'G']*

注意到slice()的起止参数包括开始索引，不包括结束索引。

如果不给slice()传递任何参数，它就会从头到尾截取所有元素。利用这一点，我们可以很容易地复制一个Array：

**var** arr = ['A', 'B', 'C', 'D', 'E', 'F', 'G'];**var** aCopy = arr.slice();

aCopy; *// ['A', 'B', 'C', 'D', 'E', 'F', 'G']*

aCopy === arr; *// false*

### push和pop

push()向Array的末尾添加若干元素，pop()则把Array的最后一个元素删除掉：

**var** arr = [1, 2];

arr.push('A', 'B'); *// 返回Array新的长度: 4*

arr; *// [1, 2, 'A', 'B']*

arr.pop(); *// pop()返回'B'*

arr; *// [1, 2, 'A']*

arr.pop(); arr.pop(); arr.pop(); *// 连续pop 3次*

arr; *// []*

arr.pop(); *// 空数组继续pop不会报错，而是返回undefined*

arr; *// []*

### unshift和shift

如果要往Array的头部添加若干元素，使用unshift()方法，shift()方法则把Array的第一个元素删掉：

**var** arr = [1, 2];

arr.unshift('A', 'B'); *// 返回Array新的长度: 4*

arr; *// ['A', 'B', 1, 2]*

arr.shift(); *// 'A'*

arr; *// ['B', 1, 2]*

arr.shift(); arr.shift(); arr.shift(); *// 连续shift 3次*

arr; *// []*

arr.shift(); *// 空数组继续shift不会报错，而是返回undefined*

arr; *// []*

### sort

sort()可以对当前Array进行排序，它会直接修改当前Array的元素位置，直接调用时，按照默认顺序排序：

**var** arr = ['B', 'C', 'A'];

arr.sort();

arr; *// ['A', 'B', 'C']*

能否按照我们自己指定的顺序排序呢？完全可以，我们将在后面的函数中讲到。

### reverse

reverse()把整个Array的元素给掉个个，也就是反转：

**var** arr = ['one', 'two', 'three'];

arr.reverse(); 

arr; *// ['three', 'two', 'one']*

### splice

splice()方法是修改Array的“万能方法”，它可以从指定的索引开始删除若干元素，然后再从该位置添加若干元素：

**var** arr = ['Microsoft', 'Apple', 'Yahoo', 'AOL', 'Excite', 'Oracle'];*// 从索引2开始删除3个元素,然后再添加两个元素:*

arr.splice(2, 3, 'Google', 'Facebook'); *// 返回删除的元素 ['Yahoo', 'AOL', 'Excite']*

arr; *// ['Microsoft', 'Apple', 'Google', 'Facebook', 'Oracle']// 只删除,不添加:*

arr.splice(2, 2); *// ['Google', 'Facebook']*

arr; *// ['Microsoft', 'Apple', 'Oracle']// 只添加,不删除:*

arr.splice(2, 0, 'Google', 'Facebook'); *// 返回[],因为没有删除任何元素*

arr; *// ['Microsoft', 'Apple', 'Google', 'Facebook', 'Oracle']*

### concat

concat()方法把当前的Array和另一个Array连接起来，并返回一个新的Array：

**var** arr = ['A', 'B', 'C'];**var** added = arr.concat([1, 2, 3]);

added; *// ['A', 'B', 'C', 1, 2, 3]*

arr; *// ['A', 'B', 'C']*

请注意，concat()方法并没有修改当前Array，而是返回了一个新的Array。

实际上，concat()方法可以接收任意个元素和Array，并且自动把Array拆开，然后全部添加到新的Array里：

**var** arr = ['A', 'B', 'C'];

arr.concat(1, 2, [3, 4]); *// ['A', 'B', 'C', 1, 2, 3, 4]*

### join

join()方法是一个非常实用的方法，它把当前Array的每个元素都用指定的字符串连接起来，然后返回连接后的字符串：

**var** arr = ['A', 'B', 'C', 1, 2, 3];

arr.join('-'); *// 'A-B-C-1-2-3'*

如果Array的元素不是字符串，将自动转换为字符串后再连接。

### 多维数组

如果数组的某个元素又是一个Array，则可以形成多维数组，例如：

**var** arr = [[1, 2, 3], [400, 500, 600], '-'];

上述Array包含3个元素，其中头两个元素本身也是Array。

练习：如何通过索引取到500这个值：

窗体顶端

'use strict';

var arr = [[1, 2, 3], [400, 500, 600], '-'];

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2C6C.tmp.png) 

alert(x); // x应该为500

 Run

窗体底端

### 小结

Array提供了一种顺序存储一组元素的功能，并可以按索引来读写。

练习：在新生欢迎会上，你已经拿到了新同学的名单，请排序后显示：欢迎XXX，XXX，XXX和XXX同学！：

窗体顶端

'use strict';

var arr = ['小明', '小红', '大军', '阿黄'];

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2C6D.tmp.png) Run

窗体底端

### 分享给朋友

### 您的鼓励是作者写作最大的动力

如果您认为本网站的教程质量不错，读后觉得收获很大，预期工资涨幅能超过30%，不妨小额赞助我一下，让我有动力继续写出高质量的教程：

#### 对象

阅读: 36398

 

JavaScript的对象是一种无序的集合数据类型，它由若干键值对组成。

JavaScript的对象用于描述现实世界中的某个对象。例如，为了描述“小明”这个淘气的小朋友，我们可以用若干键值对来描述他：

**var** xiaoming = {

​    name: '小明',

​    birth: 1990,

​    school: 'No.1 Middle School',

​    height: 1.70,

​    weight: 65,

​    score: null

};

JavaScript用一个{...}表示一个对象，键值对以xxx: xxx形式申明，用,隔开。注意，最后一个键值对不需要在末尾加,，如果加了，有的浏览器（如低版本的IE）将报错。

上述对象申明了一个name属性，值是'小明'，birth属性，值是1990，以及其他一些属性。最后，把这个对象赋值给变量xiaoming后，就可以通过变量xiaoming来获取小明的属性了：

xiaoming.name; // '小明'

xiaoming.birth; // 1990

访问属性是通过.操作符完成的，但这要求属性名必须是一个有效的变量名。如果属性名包含特殊字符，就必须用''括起来：

**var** xiaohong = {

​    name: '小红',

​    'middle-school': 'No.1 Middle School'

};

xiaohong的属性名middle-school不是一个有效的变量，就需要用''括起来。访问这个属性也无法使用.操作符，必须用['xxx']来访问：

xiaohong['middle-school']; // 'No.1 Middle School'

xiaohong['name']; // '小红'

xiaohong.name; // '小红'

也可以用xiaohong['name']来访问xiaohong的name属性，不过xiaohong.name的写法更简洁。我们在编写JavaScript代码的时候，属性名尽量使用标准的变量名，这样就可以直接通过object.prop的形式访问一个属性了。

实际上JavaScript对象的所有属性都是字符串，不过属性对应的值可以是任意数据类型。

如果访问一个不存在的属性会返回什么呢？JavaScript规定，访问不存在的属性不报错，而是返回undefined：

**var** xiaoming = {

​    name: '小明'

};

xiaoming.age; *// undefined*

由于JavaScript的对象是动态类型，你可以自由地给一个对象添加或删除属性：

**var** xiaoming = {

​    name: '小明'

};

xiaoming.age; *// undefined*

xiaoming.age = 18; *// 新增一个age属性*

xiaoming.age; *// 18***delete** xiaoming.age; *// 删除age属性*

xiaoming.age; *// undefined***delete** xiaoming['name']; *// 删除name属性*

xiaoming.name; *// undefined***delete** xiaoming.school; *// 删除一个不存在的school属性也不会报错*

如果我们要检测xiaoming是否拥有某一属性，可以用in操作符：

var xiaoming = {

​    name: '小明',

​    birth: 1990,

​    school: 'No.1 Middle School',

​    height: 1.70,

​    weight: 65,

​    score: null

};'name' **in** xiaoming; // **true**'grade' **in** xiaoming; // **false**

不过要小心，如果in判断一个属性存在，这个属性不一定是xiaoming的，它可能是xiaoming继承得到的：

'toString' **in** xiaoming; // **true**

因为toString定义在object对象中，而所有对象最终都会在原型链上指向object，所以xiaoming也拥有toString属性。

要判断一个属性是否是xiaoming自身拥有的，而不是继承得到的，可以用hasOwnProperty()方法：

var xiaoming = {

​    name: '小明'

};

xiaoming.hasOwnProperty('name'); // **true**

xiaoming.hasOwnProperty('toString'); // **false**

#### 条件判断

阅读: 26566

 

JavaScript使用if () { ... } else { ... }来进行条件判断。例如，根据年龄显示不同内容，可以用if语句实现如下：

var age = 20;**if** (age >= 18) { // 如果age >= 18为**true**，则执行**if**语句块

​    alert('adult');

} **else** { // 否则执行**else**语句块

​    alert('teenager');

}

其中else语句是可选的。如果语句块只包含一条语句，那么可以省略{}：

**var** age = 20;**if** (age >= 18)

​    alert('adult');**else**

​    alert('teenager');

省略{}的危险之处在于，如果后来想添加一些语句，却忘了写{}，就改变了if...else...的语义，例如：

var age = 20;**if** (age >= 18)

​    alert('adult');**else**

​    console.log('age < 18'); // 添加一行日志

​    alert('teenager'); // <- 这行语句已经不在**else**的控制范围了

上述代码的else子句实际上只负责执行console.log('age < 18');，原有的alert('teenager');已经不属于if...else...的控制范围了，它每次都会执行。

相反地，有{}的语句就不会出错：

**var** age = 20;**if** (age >= 18) {

​    alert('adult');

} **else** {

​    console.log('age < 18');

​    alert('teenager');

}

这就是为什么我们建议永远都要写上{}。

### 多行条件判断

如果还要更细致地判断条件，可以使用多个if...else...的组合：

**var** age = 3;**if** (age >= 18) {

​    alert('adult');

} **else** **if** (age >= 6) {

​    alert('teenager');

} **else** {

​    alert('kid');

}

上述多个if...else...的组合实际上相当于两层if...else...：

**var** age = 3;**if** (age >= 18) {

​    alert('adult');

} **else** {

​    **if** (age >= 6) {

​        alert('teenager');

​    } **else** {

​        alert('kid');

​    }

}

但是我们通常把else if连写在一起，来增加可读性。这里的else略掉了{}是没有问题的，因为它只包含一个if语句。注意最后一个单独的else不要略掉{}。

请注意，if...else...语句的执行特点是二选一，在多个if...else...语句中，如果某个条件成立，则后续就不再继续判断了。

试解释为什么下面的代码显示的是teenager：

窗体顶端

'use strict';

var age = 20;

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2C7E.tmp.png) Run

窗体底端

由于age的值为20，它实际上同时满足条件age >= 6和age >= 18，这说明条件判断的顺序非常重要。请修复后让其显示adult。

如果if的条件判断语句结果不是true或false怎么办？例如：

**var** s = '123';**if** (s.length) { *// 条件计算结果为3*

​    *//*

}

JavaScript把null、undefined、0、NaN和空字符串''视为false，其他值一概视为true，因此上述代码条件判断的结果是true。

### 练习

小明身高1.75，体重80.5kg。请根据BMI公式（体重除以身高的平方）帮小明计算他的BMI指数，并根据BMI指数：

低于18.5：过轻

18.5-25：正常

25-28：过重

28-32：肥胖

高于32：严重肥胖

用if...else...判断并显示结果：

窗体顶端

'use strict';

 

var height = parseFloat(prompt('请输入身高(m):'));

var weight = parseFloat(prompt('请输入体重(kg):'));

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2C7F.tmp.png) Run

窗体底端

 

#### 循环

阅读: 30382

 

### 循环

要计算1+2+3，我们可以直接写表达式：

1 + 2 + 3; // 6

要计算1+2+3+...+10，勉强也能写出来。

但是，要计算1+2+3+...+10000，直接写表达式就不可能了。

为了让计算机能计算成千上万次的重复运算，我们就需要循环语句。

JavaScript的循环有两种，一种是for循环，通过初始条件、结束条件和递增条件来循环执行语句块：

**var** x = 0;**var** i;**for** (i=1; i<=10000; i++) {

​    x = x + i;

}

x; *// 50005000*

让我们来分析一下for循环的控制条件：

i=1 这是初始条件，将变量i置为1；

i<=10000 这是判断条件，满足时就继续循环，不满足就退出循环；

i++ 这是每次循环后的递增条件，由于每次循环后变量i都会加1，因此它终将在若干次循环后不满足判断条件i<=10000而退出循环。

### 练习

利用for循环计算1 * 2 * 3 * ... * 10的结果：

窗体顶端

'use strict';

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2C80.tmp.png) 

if (x === 3628800) {

​    alert('1 x 2 x 3 x ... x 10 = ' + x);

}

else {

​    alert('计算错误');

}

 Run

窗体底端

for循环最常用的地方是利用索引来遍历数组：

var arr = ['Apple', 'Google', 'Microsoft'];

var i, x;

for (i=0; i<arr.length; i++) {

​    x = arr[i];

​    alert(x);

}

for循环的3个条件都是可以省略的，如果没有退出循环的判断条件，就必须使用break语句退出循环，否则就是死循环：

var x = 0;**for** (;;) { // 将无限循环下去

​    **if** (x > 100) {

​        **break**; // 通过**if**判断来退出循环

​    }

​    x ++;

}

### for ... in

for循环的一个变体是for ... in循环，它可以把一个对象的所有属性依次循环出来：

**var** o = {

​    name: 'Jack',

​    age: 20,

​    city: 'Beijing'

};**for** (**var** key **in** o) {

​    alert(key); *// 'name', 'age', 'city'*

}

要过滤掉对象继承的属性，用hasOwnProperty()来实现：

**var** o = {

​    name: 'Jack',

​    age: 20,

​    city: 'Beijing'

};**for** (**var** key **in** o) {

​    **if** (o.hasOwnProperty(key)) {

​        alert(key); *// 'name', 'age', 'city'*

​    }

}

由于Array也是对象，而它的每个元素的索引被视为对象的属性，因此，for ... in循环可以直接循环出Array的索引：

**var** a = ['A', 'B', 'C'];**for** (**var** i **in** a) {

​    alert(i); *// '0', '1', '2'*

​    alert(a[i]); *// 'A', 'B', 'C'*

}

请注意，for ... in对Array的循环得到的是String而不是Number。

### while

for循环在已知循环的初始和结束条件时非常有用。而上述忽略了条件的for循环容易让人看不清循环的逻辑，此时用while循环更佳。

while循环只有一个判断条件，条件满足，就不断循环，条件不满足时则退出循环。比如我们要计算100以内所有奇数之和，可以用while循环实现：

**var** x = 0;**var** n = 99;**while** (n > 0) {

​    x = x + n;

​    n = n - 2;

}

x; *// 2500*

在循环内部变量n不断自减，直到变为-1时，不再满足while条件，循环退出。

### do ... while

最后一种循环是do { ... } while()循环，它和while循环的唯一区别在于，不是在每次循环开始的时候判断条件，而是在每次循环完成的时候判断条件：

**var** n = 0;**do** {

​    n = n + 1;

} **while** (n < 100);

n; *// 100*

用do { ... } while()循环要小心，循环体会至少执行1次，而for和while循环则可能一次都不执行。

### 练习

请利用循环遍历数组中的每个名字，并显示Hello, xxx!：

窗体顶端

'use strict';

var arr = ['Bart', 'Lisa', 'Adam'];

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2C90.tmp.png) Run

窗体底端

请尝试for循环和while循环，并以正序、倒序两种方式遍历。

### 小结

循环是让计算机做重复任务的有效的方法，有些时候，如果代码写得有问题，会让程序陷入“死循环”，也就是永远循环下去。JavaScript的死循环会让浏览器无法正常显示或执行当前页面的逻辑，有的浏览器会直接挂掉，有的浏览器会在一段时间后提示你强行终止JavaScript的执行，因此，要特别注意死循环的问题。

在编写循环代码时，务必小心编写初始条件和判断条件，尤其是边界值。特别注意i < 100和i <= 100是不同的判断逻辑。

 

#### Map和Set

阅读: 41432

 

JavaScript的默认对象表示方式{}可以视为其他语言中的Map或Dictionary的数据结构，即一组键值对。

但是JavaScript的对象有个小问题，就是键必须是字符串。但实际上Number或者其他数据类型作为键也是非常合理的。

为了解决这个问题，最新的ES6规范引入了新的数据类型Map。要测试你的浏览器是否支持ES6规范，请执行以下代码，如果浏览器报ReferenceError错误，那么你需要换一个支持ES6的浏览器：

窗体顶端

'use strict';

var m = new Map();

var s = new Set();

alert('你的浏览器支持Map和Set！');

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2C91.tmp.png) Run

窗体底端

### Map

Map是一组键值对的结构，具有极快的查找速度。

举个例子，假设要根据同学的名字查找对应的成绩，如果用Array实现，需要两个Array：

**var** names = ['Michael', 'Bob', 'Tracy'];**var** scores = [95, 75, 85];

给定一个名字，要查找对应的成绩，就先要在names中找到对应的位置，再从scores取出对应的成绩，Array越长，耗时越长。

如果用Map实现，只需要一个“名字”-“成绩”的对照表，直接根据名字查找成绩，无论这个表有多大，查找速度都不会变慢。用JavaScript写一个Map如下：

**var** m = **new** Map([['Michael', 95], ['Bob', 75], ['Tracy', 85]]);

m.get('Michael'); *// 95*

初始化Map需要一个二维数组，或者直接初始化一个空Map。Map具有以下方法：

**var** m = **new** Map(); *// 空Map*

m.set('Adam', 67); *// 添加新的key-value*

m.set('Bob', 59);

m.has('Adam'); *// 是否存在key 'Adam': true*

m.get('Adam'); *// 67*

m.**delete**('Adam'); *// 删除key 'Adam'*

m.get('Adam'); *// undefined*

由于一个key只能对应一个value，所以，多次对一个key放入value，后面的值会把前面的值冲掉：

var m = new Map();

m.**set**('Adam', 67);

m.**set**('Adam', 88);

m.get('Adam'); // 88

### Set

Set和Map类似，也是一组key的集合，但不存储value。由于key不能重复，所以，在Set中，没有重复的key。

要创建一个Set，需要提供一个Array作为输入，或者直接创建一个空Set：

**var** s1 = **new** Set(); *// 空Set***var** s2 = **new** Set([1, 2, 3]); *// 含1, 2, 3*

重复元素在Set中自动被过滤：

var s = new **Set**([1, 2, 3, 3, '3']);

s; // **Set** {1, 2, 3, "3"}

注意数字3和字符串'3'是不同的元素。

通过add(key)方法可以添加元素到Set中，可以重复添加，但不会有效果：

\>>> s.add(4)>>> s

{1, 2, 3, 4}>>> s.add(4)>>> s

{1, 2, 3, 4}

通过delete(key)方法可以删除元素：

var s = new **Set**([1, 2, 3]);

s; // **Set** {1, 2, 3}

s.**delete**(3);

s; // **Set** {1, 2}

### 小结

Map和Set是ES6标准新增的数据类型，请根据浏览器的支持情况决定是否要使用。

 

#### iterable

阅读: 31126

 

遍历Array可以采用下标循环，遍历Map和Set就无法使用下标。为了统一集合类型，ES6标准引入了新的iterable类型，Array、Map和Set都属于iterable类型。

具有iterable类型的集合可以通过新的for ... of循环来遍历。

for ... of循环是ES6引入的新的语法，请测试你的浏览器是否支持：

窗体顶端

'use strict';

var a = [1, 2, 3];

for (var x of a) {

}

alert('你的浏览器支持for ... of');

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2C92.tmp.png) Run

窗体底端

用for ... of循环遍历集合，用法如下：

**var** a = ['A', 'B', 'C'];**var** s = **new** Set(['A', 'B', 'C']);**var** m = **new** Map([[1, 'x'], [2, 'y'], [3, 'z']]);**for** (**var** x of a) { *// 遍历Array*

​    alert(x);

}**for** (**var** x of s) { *// 遍历Set*

​    alert(x);

}**for** (**var** x of m) { *// 遍历Map*

​    alert(x[0] + '=' + x[1]);

}

你可能会有疑问，for ... of循环和for ... in循环有何区别？

for ... in循环由于历史遗留问题，它遍历的实际上是对象的属性名称。一个Array数组实际上也是一个对象，它的每个元素的索引被视为一个属性。

当我们手动给Array对象添加了额外的属性后，for ... in循环将带来意想不到的意外效果：

**var** a = ['A', 'B', 'C'];

a.name = 'Hello';**for** (**var** x **in** a) {

​    alert(x); *// '0', '1', '2', 'name'*

}

for ... in循环将把name包括在内，但Array的length属性却不包括在内。

for ... of循环则完全修复了这些问题，它只循环集合本身的元素：

**var** a = ['A', 'B', 'C'];

a.name = 'Hello';**for** (**var** x of a) {

​    alert(x); 'A', 'B', 'C'

}

这就是为什么要引入新的for ... of循环。

然而，更好的方式是直接使用iterable内置的forEach方法，它接收一个函数，每次迭代就自动回调该函数。以Array为例：

**var** a = ['A', 'B', 'C'];

a.**forEach**(**function** (element, index, array) {

​    *// element: 指向当前元素的值*

​    *// index: 指向当前索引*

​    *// array: 指向Array对象本身*

​    alert(element);

});

注意，forEach()方法是ES5.1标准引入的，你需要测试浏览器是否支持。

Set与Array类似，但Set没有索引，因此回调函数的前两个参数都是元素本身：

**var** s = **new** Set(['A', 'B', 'C']);

s.**forEach**(**function** (element, sameElement, set) {

​    alert(element);

});

Map的回调函数参数依次为value、key和map本身：

**var** m = **new** Map([[1, 'x'], [2, 'y'], [3, 'z']]);

m.**forEach**(**function** (value, key, map) {

​    alert(value);

});

如果对某些参数不感兴趣，由于JavaScript的函数调用不要求参数必须一致，因此可以忽略它们。例如，只需要获得Array的element：

**var** a = ['A', 'B', 'C'];

a.**forEach**(**function** (element) {

​    alert(element);

});

 

 

 

 

#### 函数

阅读: 15268

 

我们知道圆的面积计算公式为：

S = πr2

当我们知道半径r的值时，就可以根据公式计算出面积。假设我们需要计算3个不同大小的圆的面积：

**var** r1 = 12.34;**var** r2 = 9.08;**var** r3 = 73.1;**var** s1 = 3.14 * r1 * r1;**var** s2 = 3.14 * r2 * r2;**var** s3 = 3.14 * r3 * r3;

当代码出现有规律的重复的时候，你就需要当心了，每次写3.14 * x * x不仅很麻烦，而且，如果要把3.14改成3.14159265359的时候，得全部替换。

有了函数，我们就不再每次写s = 3.14 * x * x，而是写成更有意义的函数调用s = area_of_circle(x)，而函数area_of_circle本身只需要写一次，就可以多次调用。

基本上所有的高级语言都支持函数，JavaScript也不例外。JavaScript的函数不但是“头等公民”，而且可以像变量一样使用，具有非常强大的抽象能力。

### 抽象

抽象是数学中非常常见的概念。举个例子：

计算数列的和，比如：1 + 2 + 3 + ... + 100，写起来十分不方便，于是数学家发明了求和符号∑，可以把1 + 2 + 3 + ... + 100记作：

100

∑n

n=1

这种抽象记法非常强大，因为我们看到 ∑ 就可以理解成求和，而不是还原成低级的加法运算。

而且，这种抽象记法是可扩展的，比如：

100

∑(n2+1)

n=1

还原成加法运算就变成了：

(1 x 1 + 1) + (2 x 2 + 1) + (3 x 3 + 1) + ... + (100 x 100 + 1)

可见，借助抽象，我们才能不关心底层的具体计算过程，而直接在更高的层次上思考问题。

写计算机程序也是一样，函数就是最基本的一种代码抽象的方式。

 

 

 

#### 函数定义和调用

阅读: 37797

 

### 定义函数

在JavaScript中，定义函数的方式如下：

**function** abs(x) {

​    **if** (x >= 0) {

​        **return** x;

​    } **else** {

​        **return** -x;

​    }

}

上述abs()函数的定义如下：

function指出这是一个函数定义；

abs是函数的名称；

(x)括号内列出函数的参数，多个参数以,分隔；

{ ... }之间的代码是函数体，可以包含若干语句，甚至可以没有任何语句。

请注意，函数体内部的语句在执行时，一旦执行到return时，函数就执行完毕，并将结果返回。因此，函数内部通过条件判断和循环可以实现非常复杂的逻辑。

如果没有return语句，函数执行完毕后也会返回结果，只是结果为undefined。

由于JavaScript的函数也是一个对象，上述定义的abs()函数实际上是一个函数对象，而函数名abs可以视为指向该函数的变量。

因此，第二种定义函数的方式如下：

**var** abs = **function** (x) {

​    **if** (x >= 0) {

​        **return** x;

​    } **else** {

​        **return** -x;

​    }

};

在这种方式下，function (x) { ... }是一个匿名函数，它没有函数名。但是，这个匿名函数赋值给了变量abs，所以，通过变量abs就可以调用该函数。

上述两种定义完全等价，注意第二种方式按照完整语法需要在函数体末尾加一个;，表示赋值语句结束。

### 调用函数

调用函数时，按顺序传入参数即可：

abs(10); // 返回10

abs(-9); // 返回9

由于JavaScript允许传入任意个参数而不影响调用，因此传入的参数比定义的参数多也没有问题，虽然函数内部并不需要这些参数：

abs(10, 'blablabla'); *// 返回10*

abs(-9, 'haha', 'hehe', null); *// 返回9*

传入的参数比定义的少也没有问题：

abs(); // 返回NaN

此时abs(x)函数的参数x将收到undefined，计算结果为NaN。

要避免收到undefined，可以对参数进行检查：

**function** abs(x) {

​    **if** (**typeof** x !== 'number') {

​        **throw** 'Not a number';

​    }

​    **if** (x >= 0) {

​        **return** x;

​    } **else** {

​        **return** -x;

​    }

}

### arguments

JavaScript还有一个免费赠送的关键字arguments，它只在函数内部起作用，并且永远指向当前函数的调用者传入的所有参数。arguments类似Array但它不是一个Array：

**function** foo(x) {

​    alert(x); *// 10*

​    **for** (**var** i=0; i<arguments.length; i++) {

​        alert(arguments[i]); *// 10, 20, 30*

​    }

}

foo(10, 20, 30);

利用arguments，你可以获得调用者传入的所有参数。也就是说，即使函数不定义任何参数，还是可以拿到参数的值：

**function** abs() {

​    **if** (arguments.length === 0) {

​        **return** 0;

​    }

​    **var** x = arguments[0];

​    **return** x >= 0 ? x : -x;

}

 

abs(); *// 0*

abs(10); *// 10*

abs(-9); *// 9*

实际上arguments最常用于判断传入参数的个数。你可能会看到这样的写法：

*// foo(a[, b], c)// 接收2~3个参数，b是可选参数，如果只传2个参数，b默认为null：***function** foo(a, b, c) {

​    **if** (arguments.length === 2) {

​        *// 实际拿到的参数是a和b，c为undefined*

​        c = b; *// 把b赋给c*

​        b = null; *// b变为默认值*

​    }

​    *// ...*

}

要把中间的参数b变为“可选”参数，就只能通过arguments判断，然后重新调整参数并赋值。

### rest参数

由于JavaScript函数允许接收任意个参数，于是我们就不得不用arguments来获取所有参数：

**function** foo(a, b) {

​    **var** i, rest = [];

​    **if** (arguments.length > 2) {

​        **for** (i = 2; i<arguments.length; i++) {

​            rest.push(arguments[i]);

​        }

​    }

​    console.log('a = ' + a);

​    console.log('b = ' + b);

​    console.log(rest);

}

为了获取除了已定义参数a、b之外的参数，我们不得不用arguments，并且循环要从索引2开始以便排除前两个参数，这种写法很别扭，只是为了获得额外的rest参数，有没有更好的方法？

ES6标准引入了rest参数，上面的函数可以改写为：

**function** foo(a, b, ...rest) {

​    console.log('a = ' + a);

​    console.log('b = ' + b);

​    console.log(rest);

}

 

foo(1, 2, 3, 4, 5);*// 结果:// a = 1// b = 2// Array [ 3, 4, 5 ]*

 

foo(1);*// 结果:// a = 1// b = undefined// Array []*

rest参数只能写在最后，前面用...标识，从运行结果可知，传入的参数先绑定a、b，多余的参数以数组形式交给变量rest，所以，不再需要arguments我们就获取了全部参数。

如果传入的参数连正常定义的参数都没填满，也不要紧，rest参数会接收一个空数组（注意不是undefined）。

因为rest参数是ES6新标准，所以你需要测试一下浏览器是否支持。请用rest参数编写一个sum()函数，接收任意个参数并返回它们的和：

窗体顶端

'use strict';

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2CA3.tmp.png) 

// 测试:

var i, args = [];

for (i=1; i<=100; i++) {

​    args.push(i);

}

if (sum() !== 0) {

​    alert('测试失败: sum() = ' + sum());

} else if (sum(1) !== 1) {

​    alert('测试失败: sum(1) = ' + sum(1));

} else if (sum(2, 3) !== 5) {

​    alert('测试失败: sum(2, 3) = ' + sum(2, 3));

} else if (sum.apply(null, args) !== 5050) {

​    alert('测试失败: sum(1, 2, 3, ..., 100) = ' + sum.apply(null, args));

} else {

​    alert('测试通过!');

}

 Run

窗体底端

### 小心你的return语句

前面我们讲到了JavaScript引擎有一个在行末自动添加分号的机制，这可能让你栽到return语句的一个大坑：

**function** foo() {

​    **return** { name: 'foo' };

}

 

foo(); *// { name: 'foo' }*

如果把return语句拆成两行：

**function** foo() {

​    **return**

​        { name: 'foo' };

}

 

foo(); *// undefined*

要小心了，由于JavaScript引擎在行末自动添加分号的机制，上面的代码实际上变成了：

**function** foo() {

​    **return**; *// 自动添加了分号，相当于return undefined;*

​        { name: 'foo' }; *// 这行语句已经没法执行到了*

}

所以正确的多行写法是：

**function** foo() {

​    **return** { *// 这里不会自动加分号，因为{表示语句尚未结束*

​        name: 'foo'

​    };

}

### 练习

定义一个计算圆面积的函数area_of_circle()，它有两个参数：

r: 表示圆的半径；

pi: 表示π的值，如果不传，则默认3.14

窗体顶端

'use strict';

 

function area_of_circle(r, pi) {

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2CA4.tmp.png) 

}

// 测试:

if (area_of_circle(2) === 12.56 && area_of_circle(2, 3.1416) === 12.5664) {

​    alert('测试通过');

} else {

​    alert('测试失败');

}

 Run

窗体底端

Max是一个JavaScript新手，他写了一个max()函数，返回两个数中较大的那个：

窗体顶端

'use strict';

 

function max(a, b) {

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2CA5.tmp.png) 

}

alert(max(15, 20));

 Run

窗体底端

但是Max抱怨他的浏览器出问题了，无论传入什么数，max()函数总是返回undefined。请帮他指出问题并修复。

 

 

#### 变量作用域

阅读: 24811

 

在JavaScript中，用var申明的变量实际上是有作用域的。

如果一个变量在函数体内部申明，则该变量的作用域为整个函数体，在函数体外不可引用该变量：

'use strict';

**function** foo() {

​    **var** x = 1;

​    x = x + 1;

}

 

x = x + 2; *// ReferenceError! 无法在函数体外引用变量x*

如果两个不同的函数各自申明了同一个变量，那么该变量只在各自的函数体内起作用。换句话说，不同函数内部的同名变量互相独立，互不影响：

'use strict';

**function** foo() {

​    **var** x = 1;

​    x = x + 1;

}

**function** bar() {

​    **var** x = 'A';

​    x = x + 'B';

}

由于JavaScript的函数可以嵌套，此时，内部函数可以访问外部函数定义的变量，反过来则不行：

'use strict';

**function** foo() {

​    **var** x = 1;

​    **function** bar() {

​        **var** y = x + 1; *// bar可以访问foo的变量x!*

​    }

​    **var** z = y + 1; *// ReferenceError! foo不可以访问bar的变量y!*

}

如果内部函数和外部函数的变量名重名怎么办？

'use strict';

**function** foo() {

​    **var** x = 1;

​    **function** bar() {

​        **var** x = 'A';

​        alert('x in bar() = ' + x); *// 'A'*

​    }

​    alert('x in foo() = ' + x); *// 1*

​    bar();

}

这说明JavaScript的函数在查找变量时从自身函数定义开始，从“内”向“外”查找。如果内部函数定义了与外部函数重名的变量，则内部函数的变量将“屏蔽”外部函数的变量。

### 变量提升

JavaScript的函数定义有个特点，它会先扫描整个函数体的语句，把所有申明的变量“提升”到函数顶部：

'use strict';

**function** foo() {

​    **var** x = 'Hello, ' + y;

​    alert(x);

​    **var** y = 'Bob';

}

 

foo();

虽然是strict模式，但语句var x = 'Hello, ' + y;并不报错，原因是变量y在稍后申明了。但是alert显示Hello, undefined，说明变量y的值为undefined。这正是因为JavaScript引擎自动提升了变量y的声明，但不会提升变量y的赋值。

对于上述foo()函数，JavaScript引擎看到的代码相当于：

**function** foo() {

​    **var** y; *// 提升变量y的申明*

​    **var** x = 'Hello, ' + y;

​    alert(x);

​    y = 'Bob';

}

由于JavaScript的这一怪异的“特性”，我们在函数内部定义变量时，请严格遵守“在函数内部首先申明所有变量”这一规则。最常见的做法是用一个var申明函数内部用到的所有变量：

**function** foo() {

​    **var**

​        x = 1, *// x初始化为1*

​        y = x + 1, *// y初始化为2*

​        z, i; *// z和i为undefined*

​    *// 其他语句:*

​    **for** (i=0; i<100; i++) {

​        ...

​    }

}

### 全局作用域

不在任何函数内定义的变量就具有全局作用域。实际上，JavaScript默认有一个全局对象window，全局作用域的变量实际上被绑定到window的一个属性：

'use strict';

**var** course = 'Learn JavaScript';

alert(course); *// 'Learn JavaScript'*

alert(window.course); *// 'Learn JavaScript'*

因此，直接访问全局变量course和访问window.course是完全一样的。

你可能猜到了，由于函数定义有两种方式，以变量方式var foo = function () {}定义的函数实际上也是一个全局变量，因此，顶层函数的定义也被视为一个全局变量，并绑定到window对象：

'use strict';

**function** foo() {

​    alert('foo');

}

 

foo(); *// 直接调用foo()*

window.foo(); *// 通过window.foo()调用*

进一步大胆地猜测，我们每次直接调用的alert()函数其实也是window的一个变量：

窗体顶端

'use strict';

 

window.alert('调用window.alert()');

// 把alert保存到另一个变量:

var old_alert = window.alert;

// 给alert赋一个新函数:

window.alert = function () {}

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2CB5.tmp.png) 

// 恢复alert:

window.alert = old_alert;

alert('又可以用alert()了!');

 Run

窗体底端

这说明JavaScript实际上只有一个全局作用域。任何变量（函数也视为变量），如果没有在当前函数作用域中找到，就会继续往上查找，最后如果在全局作用域中也没有找到，则报ReferenceError错误。

### 名字空间

全局变量会绑定到window上，不同的JavaScript文件如果使用了相同的全局变量，或者定义了相同名字的顶层函数，都会造成命名冲突，并且很难被发现。

减少冲突的一个方法是把自己的所有变量和函数全部绑定到一个全局变量中。例如：

*// 唯一的全局变量MYAPP:***var** MYAPP = {};

*// 其他变量:*

MYAPP.name = 'myapp';

MYAPP.version = 1.0;

*// 其他函数:*

MYAPP.foo = **function** () {

​    **return** 'foo';

};

把自己的代码全部放入唯一的名字空间MYAPP中，会大大减少全局变量冲突的可能。

许多著名的JavaScript库都是这么干的：jQuery，YUI，underscore等等。

### 局部作用域

由于JavaScript的变量作用域实际上是函数内部，我们在for循环等语句块中是无法定义具有局部作用域的变量的：

'use strict';

**function** foo() {

​    **for** (**var** i=0; i<100; i++) {

​        *//*

​    }

​    i += 100; *// 仍然可以引用变量i*

}

为了解决块级作用域，ES6引入了新的关键字let，用let替代var可以申明一个块级作用域的变量：

'use strict';

**function** foo() {

​    **var** sum = 0;

​    **for** (**let** i=0; i<100; i++) {

​        sum += i;

​    }

​    i += 1; *// SyntaxError*

}

### 常量

由于var和let申明的是变量，如果要申明一个常量，在ES6之前是不行的，我们通常用全部大写的变量来表示“这是一个常量，不要修改它的值”：

**var** PI = 3.14;

ES6标准引入了新的关键字const来定义常量，const与let都具有块级作用域：

'use strict';

**const** PI = 3.14;

PI = 3; *// 某些浏览器不报错，但是无效果！*

PI; *// 3.14*

 

 

#### 方法

阅读: 21364

 

在一个对象中绑定函数，称为这个对象的方法。

在JavaScript中，对象的定义是这样的：

**var** xiaoming = {

​    name: '小明',

​    birth: 1990

};

但是，如果我们给xiaoming绑定一个函数，就可以做更多的事情。比如，写个age()方法，返回xiaoming的年龄：

**var** xiaoming = {

​    name: '小明',

​    birth: 1990,

​    age: **function** () {

​        **var** y = **new** Date().getFullYear();

​        **return** y - **this**.birth;

​    }

};

 

xiaoming.age; *// function xiaoming.age()*

xiaoming.age(); *// 今年调用是25,明年调用就变成26了*

绑定到对象上的函数称为方法，和普通函数也没啥区别，但是它在内部使用了一个this关键字，这个东东是什么？

在一个方法内部，this是一个特殊变量，它始终指向当前对象，也就是xiaoming这个变量。所以，this.birth可以拿到xiaoming的birth属性。

让我们拆开写：

**function** getAge() {

​    **var** y = **new** Date().getFullYear();

​    **return** y - **this**.birth;

}

**var** xiaoming = {

​    name: '小明',

​    birth: 1990,

​    age: getAge

};

 

xiaoming.age(); *// 25, 正常结果*

getAge(); *// NaN*

单独调用函数getAge()怎么返回了NaN？请注意，我们已经进入到了JavaScript的一个大坑里。

JavaScript的函数内部如果调用了this，那么这个this到底指向谁？

答案是，视情况而定！

如果以对象的方法形式调用，比如xiaoming.age()，该函数的this指向被调用的对象，也就是xiaoming，这是符合我们预期的。

如果单独调用函数，比如getAge()，此时，该函数的this指向全局对象，也就是window。

坑爹啊！

更坑爹的是，如果这么写：

**var** fn = xiaoming.age; *// 先拿到xiaoming的age函数*

fn(); *// NaN*

也是不行的！要保证this指向正确，必须用obj.xxx()的形式调用！

由于这是一个巨大的设计错误，要想纠正可没那么简单。ECMA决定，在strict模式下让函数的this指向undefined，因此，在strict模式下，你会得到一个错误：

'use strict';

**var** xiaoming = {

​    name: '小明',

​    birth: 1990,

​    age: **function** () {

​        **var** y = **new** Date().getFullYear();

​        **return** y - **this**.birth;

​    }

};

**var** fn = xiaoming.age;

fn(); *// Uncaught TypeError: Cannot read property 'birth' of undefined*

这个决定只是让错误及时暴露出来，并没有解决this应该指向的正确位置。

有些时候，喜欢重构的你把方法重构了一下：

'use strict';

**var** xiaoming = {

​    name: '小明',

​    birth: 1990,

​    age: **function** () {

​        **function** getAgeFromBirth() {

​            **var** y = **new** Date().getFullYear();

​            **return** y - **this**.birth;

​        }

​        **return** getAgeFromBirth();

​    }

};

 

xiaoming.age(); *// Uncaught TypeError: Cannot read property 'birth' of undefined*

结果又报错了！原因是this指针只在age方法的函数内指向xiaoming，在函数内部定义的函数，this又指向undefined了！（在非strict模式下，它重新指向全局对象window！）

修复的办法也不是没有，我们用一个that变量首先捕获this：

'use strict';

**var** xiaoming = {

​    name: '小明',

​    birth: 1990,

​    age: **function** () {

​        **var** that = **this**; *// 在方法内部一开始就捕获this*

​        **function** getAgeFromBirth() {

​            **var** y = **new** Date().getFullYear();

​            **return** y - that.birth; *// 用that而不是this*

​        }

​        **return** getAgeFromBirth();

​    }

};

 

xiaoming.age(); *// 25*

用var that = this;，你就可以放心地在方法内部定义其他函数，而不是把所有语句都堆到一个方法中。

### apply

虽然在一个独立的函数调用中，根据是否是strict模式，this指向undefined或window，不过，我们还是可以控制this的指向的！

要指定函数的this指向哪个对象，可以用函数本身的apply方法，它接收两个参数，第一个参数就是需要绑定的this变量，第二个参数是Array，表示函数本身的参数。

用apply修复getAge()调用：

**function** getAge() {

​    **var** y = **new** Date().getFullYear();

​    **return** y - **this**.birth;

}

**var** xiaoming = {

​    name: '小明',

​    birth: 1990,

​    age: getAge

};

 

xiaoming.age(); *// 25*

getAge.apply(xiaoming, []); *// 25, this指向xiaoming, 参数为空*

另一个与apply()类似的方法是call()，唯一区别是：

 

apply()把参数打包成Array再传入；

 

 

call()把参数按顺序传入。

 

比如调用Math.max(3, 5, 4)，分别用apply()和call()实现如下：

Math.max.apply(null, [3, 5, 4]); *// 5*

Math.max.call(null, 3, 5, 4); *// 5*

对普通函数调用，我们通常把this绑定为null。

### 装饰器

利用apply()，我们还可以动态改变函数的行为。

JavaScript的所有对象都是动态的，即使内置的函数，我们也可以重新指向新的函数。

现在假定我们想统计一下代码一共调用了多少次parseInt()，可以把所有的调用都找出来，然后手动加上count += 1，不过这样做太傻了。最佳方案是用我们自己的函数替换掉默认的parseInt()：

**var** count = 0;**var** oldParseInt = parseInt; *// 保存原函数*

 

window.parseInt = **function** () {

​    count += 1;

​    **return** oldParseInt.apply(null, arguments); *// 调用原函数*

};

*// 测试:*

parseInt('10');

parseInt('20');

parseInt('30');

count; *// 3*

#### 高阶函数

阅读: 12124

 

高阶函数英文叫Higher-order function。那么什么是高阶函数？

JavaScript的函数其实都指向某个变量。既然变量可以指向函数，函数的参数能接收变量，那么一个函数就可以接收另一个函数作为参数，这种函数就称之为高阶函数。

一个最简单的高阶函数：

**function** add(x, y, f) {

​    **return** f(x) + f(y);

}

当我们调用add(-5, 6, Math.abs)时，参数x，y和f分别接收-5，6和函数Math.abs，根据函数定义，我们可以推导计算过程为：

x = -5;

y = 6;

f = Math.abs;

f(x) + f(y) ==> Math.abs(-5) + Math.abs(6) ==> 11;**return** 11;

用代码验证一下：

add(-5, 6, Math.abs); // 11

编写高阶函数，就是让函数的参数能够接收别的函数。

 

 

#### map/reduce

阅读: 29206

 

如果你读过Google的那篇大名鼎鼎的论文“[MapReduce: Simplified Data Processing on Large Clusters](http://research.google.com/archive/mapreduce.html)”，你就能大概明白map/reduce的概念。

### map

举例说明，比如我们有一个函数f(x)=x2，要把这个函数作用在一个数组[1, 2, 3, 4, 5, 6, 7, 8, 9]上，就可以用map实现如下：

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2CB6.tmp.jpg)

由于map()方法定义在JavaScript的Array中，我们调用Array的map()方法，传入我们自己的函数，就得到了一个新的Array作为结果：

**function** pow(x) {

​    **return** x * x;

}

**var** arr = [1, 2, 3, 4, 5, 6, 7, 8, 9];

arr.map(pow); *// [1, 4, 9, 16, 25, 36, 49, 64, 81]*

map()传入的参数是pow，即函数对象本身。

你可能会想，不需要map()，写一个循环，也可以计算出结果：

**var** f = **function** (x) {

​    **return** x * x;

};

**var** arr = [1, 2, 3, 4, 5, 6, 7, 8, 9];**var** result = [];**for** (**var** i=0; i<arr.length; i++) {

​    result.push(f(arr[i]));

}

的确可以，但是，从上面的循环代码，我们无法一眼看明白“把f(x)作用在Array的每一个元素并把结果生成一个新的Array”。

所以，map()作为高阶函数，事实上它把运算规则抽象了，因此，我们不但可以计算简单的f(x)=x2，还可以计算任意复杂的函数，比如，把Array的所有数字转为字符串：

**var** arr = [1, 2, 3, 4, 5, 6, 7, 8, 9];

arr.map(String); *// ['1', '2', '3', '4', '5', '6', '7', '8', '9']*

只需要一行代码。

### reduce

再看reduce的用法。Array的reduce()把一个函数作用在这个Array的[x1, x2, x3...]上，这个函数必须接收两个参数，reduce()把结果继续和序列的下一个元素做累积计算，其效果就是：

[x1, x2, x3, x4].reduce(f) = f(f(f(x1, x2), x3), x4)

比方说对一个Array求和，就可以用reduce实现：

**var** arr = [1, 3, 5, 7, 9];

arr.reduce(**function** (x, y) {

​    **return** x + y;

}); *// 25*

练习：利用reduce()求积：

窗体顶端

'use strict';

 

function product(arr) {

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2CB7.tmp.png) 

}

 

// 测试:

if (product([1, 2, 3, 4]) === 24 && product([0, 1, 2]) === 0 && product([99, 88, 77, 66]) === 44274384) {

​    alert('测试通过!');

}

else {

​    alert('测试失败!');

}

 Run

窗体底端

要把[1, 3, 5, 7, 9]变换成整数13579，reduce()也能派上用场：

**var** arr = [1, 3, 5, 7, 9];

arr.reduce(**function** (x, y) {

​    **return** x * 10 + y;

}); *// 13579*

如果我们继续改进这个例子，想办法把一个字符串13579先变成Array——[1, 3, 5, 7, 9]，再利用reduce()就可以写出一个把字符串转换为Number的函数。

练习：不要使用JavaScript内置的parseInt()函数，利用map和reduce操作实现一个string2int()函数：

窗体顶端

'use strict';

 

function string2int(s) {

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2CC8.tmp.png) 

}

 

// 测试:

if (string2int('0') === 0 && string2int('12345') === 12345 && string2int('12300') === 12300) {

​    if (string2int.toString().indexOf('parseInt') !== -1) {

​        alert('请勿使用parseInt()!');

​    } else if (string2int.toString().indexOf('Number') !== -1) {

​        alert('请勿使用Number()!');

​    } else {

​        alert('测试通过!');

​    }

}

else {

​    alert('测试失败!');

}

 Run

窗体底端

### 练习

请把用户输入的不规范的英文名字，变为首字母大写，其他小写的规范名字。输入：['adam', 'LISA', 'barT']，输出：['Adam', 'Lisa', 'Bart']。

窗体顶端

'use strict';

 

function normalize(arr) {

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2CC9.tmp.png) 

}

 

// 测试:

if (normalize(['adam', 'LISA', 'barT']).toString() === ['Adam', 'Lisa', 'Bart'].toString()) {

​    alert('测试通过!');

}

else {

​    alert('测试失败!');

}

 Run

窗体底端

小明希望利用map()把字符串变成整数，他写的代码很简洁：

窗体顶端

'use strict';

 

var arr = ['1', '2', '3'];

var r;

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2CCA.tmp.png) 

alert('[' + r[0] + ', ' + r[1] + ', ' + r[2] + ']');

窗体底端

 

#### filter

阅读: 8195

 

filter也是一个常用的操作，它用于把Array的某些元素过滤掉，然后返回剩下的元素。

和map()类似，Array的filter()也接收一个函数。和map()不同的是，filter()把传入的函数依次作用于每个元素，然后根据返回值是true还是false决定保留还是丢弃该元素。

例如，在一个Array中，删掉偶数，只保留奇数，可以这么写：

**var** arr = [1, 2, 4, 5, 6, 9, 10, 15];**var** r = arr.filter(**function** (x) {

​    **return** x % 2 !== 0;

});

r; *// [1, 5, 9, 15]*

把一个Array中的空字符串删掉，可以这么写：

**var** arr = ['A', '', 'B', null, undefined, 'C', '  '];**var** r = arr.filter(**function** (s) {

​    **return** s && s.trim(); *// 注意：IE9以下的版本没有trim()方法*

});

r; *// ['A', 'B', 'C']*

可见用filter()这个高阶函数，关键在于正确实现一个“筛选”函数。

### 练习

请尝试用filter()筛选出素数：

窗体顶端

'use strict';

 

function get_primes(arr) {

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2CCB.tmp.png) 

}

 

// 测试:

var

​    x,

​    r,

​    arr = [];

for (x = 1; x < 100; x++) {

​    arr.push(x);

}

r = get_primes(arr);

if (r.toString() === [2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61, 67, 71, 73, 79, 83, 89, 97].toString()) {

​    alert('测试通过!');

} else {

​    alert('测试失败: ' + r.toString());

}

 Run

窗体底端

 

#### sort

阅读: 4222

 

### 排序算法

排序也是在程序中经常用到的算法。无论使用冒泡排序还是快速排序，排序的核心是比较两个元素的大小。如果是数字，我们可以直接比较，但如果是字符串或者两个对象呢？直接比较数学上的大小是没有意义的，因此，比较的过程必须通过函数抽象出来。通常规定，对于两个元素x和y，如果认为x < y，则返回-1，如果认为x == y，则返回0，如果认为x > y，则返回1，这样，排序算法就不用关心具体的比较过程，而是根据比较结果直接排序。

JavaScript的Array的sort()方法就是用于排序的，但是排序结果可能让你大吃一惊：

*// 看上去正常的结果:*

['Google', 'Apple', 'Microsoft'].sort(); *// ['Apple', 'Google', 'Microsoft'];*

*// apple排在了最后:*

['Google', 'apple', 'Microsoft'].sort(); *// ['Google', 'Microsoft", 'apple']*

*// 无法理解的结果:*

[10, 20, 1, 2].sort(); *// [1, 10, 2, 20]*

第二个排序把apple排在了最后，是因为字符串根据ASCII码进行排序，而小写字母a的ASCII码在大写字母之后。

第三个排序结果是什么鬼？简单的数字排序都能错？

这是因为Array的sort()方法默认把所有元素先转换为String再排序，结果'10'排在了'2'的前面，因为字符'1'比字符'2'的ASCII码小。

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2CCC.tmp.png)

如果不知道sort()方法的默认排序规则，直接对数字排序，绝对栽进坑里！

幸运的是，sort()方法也是一个高阶函数，它还可以接收一个比较函数来实现自定义的排序。

要按数字大小排序，我们可以这么写：

**var** arr = [10, 20, 1, 2];

arr.sort(**function** (x, y) {

​    **if** (x < y) {

​        **return** -1;

​    }

​    **if** (x > y) {

​        **return** 1;

​    }

​    **return** 0;

}); *// [1, 2, 10, 20]*

如果要倒序排序，我们可以把大的数放前面：

**var** arr = [10, 20, 1, 2];

arr.sort(**function** (x, y) {

​    **if** (x < y) {

​        **return** 1;

​    }

​    **if** (x > y) {

​        **return** -1;

​    }

​    **return** 0;

}); *// [20, 10, 2, 1]*

默认情况下，对字符串排序，是按照ASCII的大小比较的，现在，我们提出排序应该忽略大小写，按照字母序排序。要实现这个算法，不必对现有代码大加改动，只要我们能定义出忽略大小写的比较算法就可以：

**var** arr = ['Google', 'apple', 'Microsoft'];

arr.sort(**function** (s1, s2) {

​    x1 = s1.toUpperCase();

​    x2 = s2.toUpperCase();

​    **if** (x1 < x2) {

​        **return** -1;

​    }

​    **if** (x1 > x2) {

​        **return** 1;

​    }

​    **return** 0;

}); *// ['apple', 'Google', 'Microsoft']*

忽略大小写来比较两个字符串，实际上就是先把字符串都变成大写（或者都变成小写），再比较。

从上述例子可以看出，高阶函数的抽象能力是非常强大的，而且，核心代码可以保持得非常简洁。

最后友情提示，sort()方法会直接对Array进行修改，它返回的结果仍是当前Array：

**var** a1 = ['B', 'A', 'C'];**var** a2 = a1.sort();

a1; *// ['A', 'B', 'C']*

a2; *// ['A', 'B', 'C']*

a1 === a2; *// true, a1和a2是同一对象*

 

 

 

#### 闭包

阅读: 29745

 

### 函数作为返回值

高阶函数除了可以接受函数作为参数外，还可以把函数作为结果值返回。

我们来实现一个对Array的求和。通常情况下，求和的函数是这样定义的：

**function** sum(arr) {

​    **return** arr.reduce(**function** (x, y) {

​        **return** x + y;

​    });

}

 

sum([1, 2, 3, 4, 5]); *// 15*

但是，如果不需要立刻求和，而是在后面的代码中，根据需要再计算怎么办？可以不返回求和的结果，而是返回求和的函数！

**function** lazy_sum(arr) {

​    **var** sum = **function** () {

​        **return** arr.reduce(**function** (x, y) {

​            **return** x + y;

​        });

​    }

​    **return** sum;

}

当我们调用lazy_sum()时，返回的并不是求和结果，而是求和函数：

**var** f = lazy_sum([1, 2, 3, 4, 5]); *// function sum()*

调用函数f时，才真正计算求和的结果：

f(); // 15

在这个例子中，我们在函数lazy_sum中又定义了函数sum，并且，内部函数sum可以引用外部函数lazy_sum的参数和局部变量，当lazy_sum返回函数sum时，相关参数和变量都保存在返回的函数中，这种称为“闭包（Closure）”的程序结构拥有极大的威力。

请再注意一点，当我们调用lazy_sum()时，每次调用都会返回一个新的函数，即使传入相同的参数：

**var** f1 = lazy_sum([1, 2, 3, 4, 5]);**var** f2 = lazy_sum([1, 2, 3, 4, 5]);

f1 === f2; *// false*

f1()和f2()的调用结果互不影响。

### 闭包

注意到返回的函数在其定义内部引用了局部变量arr，所以，当一个函数返回了一个函数后，其内部的局部变量还被新函数引用，所以，闭包用起来简单，实现起来可不容易。

另一个需要注意的问题是，返回的函数并没有立刻执行，而是直到调用了f()才执行。我们来看一个例子：

**function** count() {

​    **var** arr = [];

​    **for** (**var** i=1; i<=3; i++) {

​        arr.push(**function** () {

​            **return** i * i;

​        });

​    }

​    **return** arr;

}

**var** results = count();**var** f1 = results[0];**var** f2 = results[1];**var** f3 = results[2];

在上面的例子中，每次循环，都创建了一个新的函数，然后，把创建的3个函数都添加到一个Array中返回了。

你可能认为调用f1()，f2()和f3()结果应该是1，4，9，但实际结果是：

f1(); // 16

f2(); // 16

f3(); // 16

全部都是16！原因就在于返回的函数引用了变量i，但它并非立刻执行。等到3个函数都返回时，它们所引用的变量i已经变成了4，因此最终结果为16。

返回闭包时牢记的一点就是：返回函数不要引用任何循环变量，或者后续会发生变化的变量。

如果一定要引用循环变量怎么办？方法是再创建一个函数，用该函数的参数绑定循环变量当前的值，无论该循环变量后续如何更改，已绑定到函数参数的值不变：

**function** count() {

​    **var** arr = [];

​    **for** (**var** i=1; i<=3; i++) {

​        arr.push((**function** (n) {

​            **return** **function** () {

​                **return** n * n;

​            }

​        })(i));

​    }

​    **return** arr;

}

**var** results = count();**var** f1 = results[0];**var** f2 = results[1];**var** f3 = results[2];

 

f1(); *// 1*

f2(); *// 4*

f3(); *// 9*

注意这里用了一个“创建一个匿名函数并立刻执行”的语法：

(**function** (x) {

​    **return** x * x;

})(3); *// 9*

理论上讲，创建一个匿名函数并立刻执行可以这么写：

**function** (x) { **return** x * x } (3);

但是由于JavaScript语法解析的问题，会报SyntaxError错误，因此需要用括号把整个函数定义括起来：

(**function** (x) { **return** x * x }) (3);

通常，一个立即执行的匿名函数可以把函数体拆开，一般这么写：

(**function** (x) {

​    **return** x * x;

})(3);

说了这么多，难道闭包就是为了返回一个函数然后延迟执行吗？

当然不是！闭包有非常强大的功能。举个栗子：

在面向对象的程序设计语言里，比如Java和C++，要在对象内部封装一个私有变量，可以用private修饰一个成员变量。

在没有class机制，只有函数的语言里，借助闭包，同样可以封装一个私有变量。我们用JavaScript创建一个计数器：

'use strict';

**function** create_counter(initial) {

​    **var** x = initial || 0;

​    **return** {

​        inc: **function** () {

​            x += 1;

​            **return** x;

​        }

​    }

}

它用起来像这样：

**var** c1 = create_counter();

c1.inc(); *// 1*

c1.inc(); *// 2*

c1.inc(); *// 3*

**var** c2 = create_counter(10);

c2.inc(); *// 11*

c2.inc(); *// 12*

c2.inc(); *// 13*

在返回的对象中，实现了一个闭包，该闭包携带了局部变量x，并且，从外部代码根本无法访问到变量x。换句话说，闭包就是携带状态的函数，并且它的状态可以完全对外隐藏起来。

闭包还可以把多参数的函数变成单参数的函数。例如，要计算xy可以用Math.pow(x, y)函数，不过考虑到经常计算x2或x3，我们可以利用闭包创建新的函数pow2和pow3：

**function** make_pow(n) {

​    **return** **function** (x) {

​        **return** Math.pow(x, n);

​    }

}

*// 创建两个新函数:***var** pow2 = make_pow(2);**var** pow3 = make_pow(3);

 

pow2(5); *// 25*

pow3(7); *// 343*

### 脑洞大开

很久很久以前，有个叫阿隆佐·邱奇的帅哥，发现只需要用函数，就可以用计算机实现运算，而不需要0、1、2、3这些数字和+、-、*、/这些符号。

JavaScript支持函数，所以可以用JavaScript用函数来写这些计算。来试试：

窗体顶端

'use strict';

 

// 定义数字0:

var zero = function (f) {

​    return function (x) {

​        return x;

​    }

};

 

// 定义数字1:

var one = function (f) {

​    return function (x) {

​        return f(x);

​    }

};

 

// 定义加法:

function add(n, m) {

​    return function (f) {

​        return function (x) {

​            return m(f)(n(f)(x));

​        }

​    }

}

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2CDD.tmp.png) Run

窗体底端

 

 

 

#### 箭头函数

阅读: 9697

 

ES6标准新增了一种新的函数：Arraw Function（箭头函数）。

为什么叫Arrow Function？因为它的定义用的就是一个箭头：

x => x * x

上面的箭头函数相当于：

**function** (x) {

​    **return** x * x;

}

在继续学习箭头函数之前，请测试你的浏览器是否支持ES6的Array Function：

窗体顶端

'use strict';

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2CDE.tmp.png) 

alert('你的浏览器支持ES6的Array Function!');

 Run

窗体底端

箭头函数相当于匿名函数，并且简化了函数定义。箭头函数有两种格式，一种像上面的，只包含一个表达式，连{ ... }和return都省略掉了。还有一种可以包含多条语句，这时候就不能省略{ ... }和return：

x => {

​    **if** (x > 0) {

​        **return** x * x;

​    }

​    **else** {

​        **return** - x * x;

​    }

}

如果参数不是一个，就需要用括号()括起来：

*// 两个参数:*

(x, y) => x * x + y * y

*// 无参数:*

() => 3.14

*// 可变参数:*

(x, y, ...rest) => {

​    **var** i, sum = x + y;

​    **for** (i=0; i<rest.length; i++) {

​        sum += rest[i];

​    }

​    **return** sum;

}

如果要返回一个对象，就要注意，如果是单表达式，这么写的话会报错：

*// SyntaxError:*

x => { foo: x }

因为和函数体的{ ... }有语法冲突，所以要改为：

*// ok:*

x => ({ foo: x })

### this

箭头函数看上去是匿名函数的一种简写，但实际上，箭头函数和匿名函数有个明显的区别：箭头函数内部的this是词法作用域，由上下文确定。

回顾前面的例子，由于JavaScript函数对this绑定的错误处理，下面的例子无法得到预期结果：

**var** obj = {

​    birth: 1990,

​    getAge: **function** () {

​        **var** b = **this**.birth; *// 1990*

​        **var** fn = **function** () {

​            **return** **new** Date().getFullYear() - **this**.birth; *// this指向window或undefined*

​        };

​        **return** fn();

​    }

};

现在，箭头函数完全修复了this的指向，this总是指向词法作用域，也就是外层调用者obj：

**var** obj = {

​    birth: 1990,

​    getAge: **function** () {

​        **var** b = **this**.birth; *// 1990*

​        **var** fn = () => **new** Date().getFullYear() - **this**.birth; *// this指向obj对象*

​        **return** fn();

​    }

};

obj.getAge(); *// 25*

如果使用箭头函数，以前的那种hack写法：

**var** that = **this**;

就不再需要了。

由于this在箭头函数中已经按照词法作用域绑定了，所以，用call()或者apply()调用箭头函数时，无法对this进行绑定，即传入的第一个参数被忽略：

**var** obj = {

​    birth: 1990,

​    getAge: **function** (year) {

​        **var** b = **this**.birth; *// 1990*

​        **var** fn = (y) => y - **this**.birth; *// this.birth仍是1990*

​        **return** fn.call({birth:2000}, year);

​    }

};

obj.getAge(2015); *// 25*

 

 

 

 

#### generator

阅读: 7267

 

generator（生成器）是ES6标准引入的新的数据类型。一个generator看上去像一个函数，但可以返回多次。

ES6定义generator标准的哥们借鉴了Python的generator的概念和语法，如果你对Python的generator很熟悉，那么ES6的generator就是小菜一碟了。如果你对Python还不熟，赶快恶补[Python教程](http://www.liaoxuefeng.com/wiki/0014316089557264a6b348958f449949df42a6d3a2e542c000/0014317799226173f45ce40636141b6abc8424e12b5fb27000)！。

我们先复习函数的概念。一个函数是一段完整的代码，调用一个函数就是传入参数，然后返回结果：

**function** foo(x) {

​    **return** x + x;

}

**var** r = foo(1); *// 调用foo函数*

函数在执行过程中，如果没有遇到return语句（函数末尾如果没有return，就是隐含的return undefined;），控制权无法交回被调用的代码。

generator跟函数很像，定义如下：

**function*** foo(x) {

​    **yield** x + 1;

​    **yield** x + 2;

​    **return** x + 3;

}

generator和函数不同的是，generator由function*定义（注意多出的*号），并且，除了return语句，还可以用yield返回多次。

大多数同学立刻就晕了，generator就是能够返回多次的“函数”？返回多次有啥用？

还是举个栗子吧。

我们以一个著名的斐波那契数列为例，它由0，1开头：

0 1 1 2 3 5 8 13 21 34 ...

要编写一个产生斐波那契数列的函数，可以这么写：

**function** fib(max) {

​    **var**

​        t,

​        a = 0,

​        b = 1,

​        arr = [0, 1];

​    **while** (arr.length < max) {

​        t = a + b;

​        a = b;

​        b = t;

​        arr.push(t);

​    }

​    **return** arr;

}

*// 测试:*

fib(5); *// [0, 1, 1, 2, 3]*

fib(10); *// [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]*

函数只能返回一次，所以必须返回一个Array。但是，如果换成generator，就可以一次返回一个数，不断返回多次。用generator改写如下：

**function*** fib(max) {

​    **var**

​        t,

​        a = 0,

​        b = 1,

​        n = 1;

​    **while** (n < max) {

​        **yield** a;

​        t = a + b;

​        a = b;

​        b = t;

​        n ++;

​    }

​    **return** a;

}

直接调用试试：

fib(5); // fib {[[GeneratorStatus]]: "suspended", [[GeneratorReceiver]]: Window}

直接调用一个generator和调用函数不一样，fib(5)仅仅是创建了一个generator对象，还没有去执行它。

调用generator对象有两个方法，一是不断地调用generator对象的next()方法：

var f = fib(5);

f.**next**(); // {value: 0, done: **false**}

f.**next**(); // {value: 1, done: **false**}

f.**next**(); // {value: 1, done: **false**}

f.**next**(); // {value: 2, done: **false**}

f.**next**(); // {value: 3, done: **true**}

next()方法会执行generator的代码，然后，每次遇到yield x;就返回一个对象{value: x, done: true/false}，然后“暂停”。返回的value就是yield的返回值，done表示这个generator是否已经执行结束了。如果done为true，则value就是return的返回值。

当执行到done为true时，这个generator对象就已经全部执行完毕，不要再继续调用next()了。

第二个方法是直接用for ... of循环迭代generator对象，这种方式不需要我们自己判断done：

**for** (**var** x of fib(5)) {

​    console.log(x); *// 依次输出0, 1, 1, 2, 3*

}

generator和普通函数相比，有什么用？

因为generator可以在执行过程中多次返回，所以它看上去就像一个可以记住执行状态的函数，利用这一点，写一个generator就可以实现需要用面向对象才能实现的功能。例如，用一个对象来保存状态，得这么写：

**var** fib = {

​    a: 0,

​    b: 1,

​    n: 0,

​    max: 5,

​    next: **function** () {

​        **var**

​            r = **this**.a,

​            t = **this**.a + **this**.b;

​        **this**.a = **this**.b;

​        **this**.b = t;

​        **if** (**this**.n < **this**.max) {

​            **this**.n ++;

​            **return** r;

​        } **else** {

​            **return** undefined;

​        }

​    }

};

用对象的属性来保存状态，相当繁琐。

generator还有另一个巨大的好处，就是把异步回调代码变成“同步”代码。这个好处要等到后面学了AJAX以后才能体会到。

没有generator之前的黑暗时代，用AJAX时需要这么写代码：

ajax('http://url-1', data1, **function** (err, result) {

​    **if** (err) {

​        **return** handle(err);

​    }

​    ajax('http://url-2', data2, **function** (err, result) {

​        **if** (err) {

​            **return** handle(err);

​        }

​        ajax('http://url-3', data3, **function** (err, result) {

​            **if** (err) {

​                **return** handle(err);

​            }

​            **return** success(result);

​        });

​    });

});

回调越多，代码越难看。

有了generator的美好时代，用AJAX时可以这么写：

**try** {

​    r1 = **yield** ajax('http://url-1', data1);

​    r2 = **yield** ajax('http://url-2', data2);

​    r3 = **yield** ajax('http://url-3', data3);

​    success(r3);

}**catch** (err) {

​    handle(err);

}

看上去是同步的代码，实际执行是异步的。

### 练习

要生成一个自增的ID，可以编写一个next_id()函数：

**var** current_id = 0;

**function** next_id() {

​    current_id ++;

​    **return** current_id;

}

由于函数无法保存状态，故需要一个全局变量current_id来保存数字。

不用闭包，试用generator改写：

窗体顶端

'use strict';

function* next_id() {

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\ksohtml\wps2CEE.tmp.png) 

}

 

// 测试:

var

​    x,

​    pass = true,

​    g = next_id();

for (x = 1; x < 100; x ++) {

​    if (g.next().value !== x) {

​        pass = false;

​        alert('测试失败!');

​        break;

​    }

}

if (pass) {

​    alert('测试通过!');

}

 Run

窗体底端

 

 

#### 标准对象

阅读: 3224

 

在JavaScript的世界里，一切都是对象。

但是某些对象还是和其他对象不太一样。为了区分对象的类型，我们用typeof操作符获取对象的类型，它总是返回一个字符串：

**typeof** 123; *// 'number'***typeof** NaN; *// 'number'***typeof** 'str'; *// 'string'***typeof** true; *// 'boolean'***typeof** undefined; *// 'undefined'***typeof** Math.abs; *// 'function'***typeof** null; *// 'object'***typeof** []; *// 'object'***typeof** {}; *// 'object'*

可见，number、string、boolean、function和undefined有别于其他类型。特别注意null的类型是object，Array的类型也是object，如果我们用typeof将无法区分出null、Array和通常意义上的object——{}。

### 包装对象

除了这些类型外，JavaScript还提供了包装对象，熟悉Java的小伙伴肯定很清楚int和Integer这种暧昧关系。

number、boolean和string都有包装对象。没错，在JavaScript中，字符串也区分string类型和它的包装类型。包装对象用new创建：

**var** n = **new** Number(123); *// 123,生成了新的包装类型***var** b = **new** Boolean(true); *// true,生成了新的包装类型***var** s = **new** String('str'); *// 'str',生成了新的包装类型*

虽然包装对象看上去和原来的值一模一样，显示出来也是一模一样，但他们的类型已经变为object了！所以，包装对象和原始值用===比较会返回false：

**typeof** **new** Number(123); *// 'object'***new** Number(123) === 123; *// false*

**typeof** **new** Boolean(true); *// 'object'***new** Boolean(true) === true; *// false*

**typeof** **new** String('str'); *// 'object'***new** String('str') === 'str'; *// false*

所以闲的蛋疼也不要使用包装对象！尤其是针对string类型！！！

如果我们在使用Number、Boolean和String时，没有写new会发生什么情况？

此时，Number()、Boolean和String()被当做普通函数，把任何类型的数据转换为number、boolean和string类型（注意不是其包装类型）：

**var** n = Number('123'); *// 123，相当于parseInt()或parseFloat()***typeof** n; *// 'number'*

**var** b = Boolean('true'); *// true***typeof** b; *// 'boolean'*

**var** b2 = Boolean('false'); *// true! 'false'字符串转换结果为true！因为它是非空字符串！***var** b3 = Boolean(''); *// false*

**var** s = String(123.45); *// '123.45'***typeof** s; *// 'string'*

是不是感觉头大了？这就是JavaScript特有的催眠魅力！

总结一下，有这么几条规则需要遵守：

 

不要使用new Number()、new Boolean()、new String()创建包装对象；

 

 

用parseInt()或parseFloat()来转换任意类型到number；

 

 

用String()来转换任意类型到string，或者直接调用某个对象的toString()方法；

 

 

通常不必把任意类型转换为boolean再判断，因为可以直接写if (myVar) {...}；

 

 

typeof操作符可以判断出number、boolean、string、function和undefined；

 

 

判断Array要使用Array.isArray(arr)；

 

 

判断null请使用myVar === null；

 

 

判断某个全局变量是否存在用typeof window.myVar === 'undefined'；

 

 

函数内部判断某个变量是否存在用typeof myVar === 'undefined'。

 

最后有细心的同学指出，任何对象都有toString()方法吗？null和undefined就没有！确实如此，这两个特殊值要除外，虽然null还伪装成了object类型。

更细心的同学指出，number对象调用toString()报SyntaxError：

123.toString(); // SyntaxError

遇到这种情况，要特殊处理一下：

123..toString(); // '123', 注意是两个点！

(123).toString(); // '123'

不要问为什么，这就是JavaScript代码的乐趣！

 