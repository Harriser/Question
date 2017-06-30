**Table of Contents**  *generated with [DocToc](http://doctoc.herokuapp.com/)*

- [FE-Problem Finishing](#fe-problem-finishing)
  - [$HTML，HTTP，web综合问题](#$html，-http，web综合问题)
    - [HTML 整理](#HTML-整理)
    - A
    - A
    - A
  - [$CSS部分](#$css部分)
    - [CSS选择器有哪些](#css选择器有哪些)
    - A
    - A
    - A
  - [$Javascript 部分](#Javascript部分)
    - [严格模式和正常模式](#严格模式和正常模式)
    - [Scope作用范围](#Scope作用范围)
    - [函数内,`var a=b=5;`,b为什么会是全局变量](#函数内var-a-b-5-b为什么会是全局变量)
    - [基本数据类型和引用类型](#基本数据类型和引用类型)
    - [`const`,`var`,`let`区别](#constvarlet区别)
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A
    - A

<!-- END doctoc generated TOC -->

# FE-Problem Finishing

个人收集常见或遇到的知识点、答案，参考答案仅代表个人观点，通过文档内搜索目录可快速定位

####
```
⒈、⒉、⒊、⒋、⒌、⒍、⒎、⒏、⒐、⒑
⑴、⑵、⑶、⑷、⑸、⑹、⑺、⑻、⑼、⑽
㈠、㈡、㈢、㈣、㈤、㈥、㈦、㈧、㈨、㈩
Ⅰ、Ⅱ、Ⅲ、Ⅳ、Ⅴ、Ⅵ、Ⅶ、Ⅷ、Ⅸ、Ⅹ、Ⅺ、Ⅻ
```

## $HTML综合问题
### 三级标题


## Javascript部分

### 严格模式和正常模式
　　除了正常运行模式，ECMAscript 5添加了第二种运行模式："严格模式"（strict mode）。顾名思义，这种模式使得Javascript在更严格的条件下运行。
```
    function strict(){
      "use strict";
      return "这是严格模式。";
    }
    function notStrict() {
      return "这是正常模式。";
    }
```

### Scope作用范围
```
    var scope="global";
    (function(){
      console.log(scope);  //undefined
      var scope="local";
      console.log(scope);  //local
    })();
```
　　第二次定义的"scope"，作用域提升为全局作用域，全局作用域在未定义前调用，所以第一次输出会报错。
　　script标签下的变量是全局变量即属于window对象的变量，按照作用域链的原理，当一个变量在当前作用域下找不到该变量的定义，那么就会沿着作用域链往上找直到在全局作用域里查找。

### 函数内,`var a=b=5;`,b为什么会是全局变量
```
    (function () {
      var a=b=5;
    })();
    console.log(a);  //undefined
    console.log(b);  //5
```
　　此处赋值给a“b=1”，a是不存在的；var a=b=1，等价于b=1; var a=b;。
　　b=5;是全局变量，var a=b;是局部变量所以a在外部是访问不到的
　　所以顺序执行时，a先执行会报错不存在，b先执行则会正常打印

### 基本数据类型和引用类型
　　基本类型是指：Undefined、Null、Boolean、Number和String，基本类型值就是简单的数据段；
　　引用类型：Object(对象)、Array(数组)、function(函数)。 
　　引用类型是指多个指构成的对象，JS中对象指的是引用类型，引用类型值可能由多个值构成的对象。

### `const`,`var`,`let`区别

- let声明的变量拥有块级作用域。let声明的变量的作用域只是外层块，而不是整个外层函数。
- let声明的全局变量不是全局对象的属性。
- let声明的变量直到控制流到达该变量被定义的代码行时才会被装载，所以在到达之前使用该变量会触发错误。
- 用let重定义变量会抛出一个语法错误（SyntaxError）
- const声明的变量只可以在声明时赋值，不可随意修改，否则会导致SyntaxError（语法错误）。

- 1.const定义的变量不可以修改，而且必须初始化。
```
    const b=2;  //正确
    //const b;  //错误，必须初始化 
    console.log('函数外const定义b:'+b);  //有输出值
    //b=5;
    //console.log('函数外修改const定义b:'+b);  //无法输出 
```

- 2.var定义的变量可以修改，如果不初始化会输出undefined，不会报错。
```
    var a = 1;
    //var a;  //不会报错
    console.log('函数外var定义a：' + a);  //可以输出a=1
    function change(){
      a = 4;
      console.log('函数内var定义a：' + a);  //可以输出a=4
    } 
    change();
    console.log('函数调用后var定义a为函数内部修改值：' + a);//可以输出a=4
```

- 3.let是块级作用域，函数内部使用let定义后，对函数外部无影响。
```
    let c = 3;
    console.log('函数外let定义c：' + c);  //输出c=3
    function change(){
      let c = 6;
      console.log('函数内let定义c：' + c);  //输出c=6
    } 
    change();
    console.log('函数调用后let定义c不受函数内部定义影响：' + c);  //输出c=3
```




### 


### 


### 


### 


### 


### 


### 


