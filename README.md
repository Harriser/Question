<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
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
    - [函数内，var a=b=5;b为什么会是全局变量？](#函数内,vara-b-5;b为什么会是全局变量?)
    - [基本数据类型和引用类型](#基本数据类型和引用类型)
    - [`const`,`var`,`let`区别](#const,var,let区别)
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
<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# FE-Problem Finishing

个人收集常见或遇到的知识点、答案，参考答案仅代表个人观点，通过文档内搜索目录可快速定位

## $HTML综合问题
### 三级标题


## Javascript部分

### 严格模式和正常模式
　　除了正常运行模式，ECMAscript 5添加了第二种运行模式："严格模式"（strict mode）。顾名思义，这种模式使得Javascript在更严格的条件下运行。

    function strict(){
      "use strict";
      return "这是严格模式。";
    }
    function notStrict() {
      return "这是正常模式。";
    }

### Scope作用范围
    var scope="global";
    (function(){
      console.log(scope);  //undefined
      var scope="local";
      console.log(scope);  //local
    })();
　　第二次定义的"scope"，作用域提升为全局作用域，全局作用域在未定义前调用，所以第一次输出会报错。
　　script标签下的变量是全局变量即属于window对象的变量，按照作用域链的原理，当一个变量在当前作用域下找不到该变量的定义，那么就会沿着作用域链往上找直到在全局作用域里查找。

### 函数内，var a=b=5;b为什么会是全局变量？

    (function () {
      var a=b=5;
    })();
    console.log(a);  //undefined
    console.log(b);  //5
　　此处赋值给a“b=1”，a是不存在的；var a=b=1，等价于b=1; var a=b;。
　　b=5;是全局变量，var a=b;是局部变量所以a在外部是访问不到的
　　所以顺序执行时，a先执行会报错不存在，b先执行则会正常打印

### 基本数据类型和引用类型
　　基本类型是指：Undefined、Null、Boolean、Number和String，基本类型值就是简单的数据段；
　　引用类型：Object(对象)、Array(数组)、function(函数)。 
　　引用类型是指多个指构成的对象，JS中对象指的是引用类型，引用类型值可能由多个值构成的对象。

### `const`,`var`,`let`区别


### 


### 


### 


### 


### 


### 


### 


