# javascript规范




[1 前言](#1-%E5%89%8D%E8%A8%80)

[2 代码风格](#2-%E4%BB%A3%E7%A0%81%E9%A3%8E%E6%A0%BC)

　　[2.1 文件](#21-%E6%96%87%E4%BB%B6)

　　[2.2 结构](#22-%E7%BB%93%E6%9E%84)

　　　　[2.2.1 缩进](#221-%E7%BC%A9%E8%BF%9B)

　　　　[2.2.2 空格](#222-%E7%A9%BA%E6%A0%BC)

　　　　[2.2.3 换行](#223-%E6%8D%A2%E8%A1%8C)

　　　　[2.2.4 语句](#224-%E8%AF%AD%E5%8F%A5)

　　[2.3 命名](#23-%E5%91%BD%E5%90%8D)

　　[2.4 注释](#24-%E6%B3%A8%E9%87%8A)

　　　　[2.4.1 单行注释](#241-%E5%8D%95%E8%A1%8C%E6%B3%A8%E9%87%8A)

　　　　[2.4.2 多行注释](#242-%E5%A4%9A%E8%A1%8C%E6%B3%A8%E9%87%8A)

　　　　[2.4.3 文档化注释](#243-%E6%96%87%E6%A1%A3%E5%8C%96%E6%B3%A8%E9%87%8A)

　　　　[2.4.4 类型定义](#244-%E7%B1%BB%E5%9E%8B%E5%AE%9A%E4%B9%89)

　　　　[2.4.5 文件注释](#245-%E6%96%87%E4%BB%B6%E6%B3%A8%E9%87%8A)

　　　　[2.4.6 命名空间注释](#246-%E5%91%BD%E5%90%8D%E7%A9%BA%E9%97%B4%E6%B3%A8%E9%87%8A)

　　　　[2.4.7 类注释](#247-%E7%B1%BB%E6%B3%A8%E9%87%8A)

　　　　[2.4.8 函数/方法注释](#248-%E5%87%BD%E6%95%B0/%E6%96%B9%E6%B3%95%E6%B3%A8%E9%87%8A)

　　　　[2.4.9 事件注释](#249-%E4%BA%8B%E4%BB%B6%E6%B3%A8%E9%87%8A)

　　　　[2.4.10 常量注释](#2410-%E5%B8%B8%E9%87%8F%E6%B3%A8%E9%87%8A)

　　　　[2.4.11 复杂类型注释](#2411-%E5%A4%8D%E6%9D%82%E7%B1%BB%E5%9E%8B%E6%B3%A8%E9%87%8A)

　　　　[2.4.12 AMD 模块注释](#2412-amd-%E6%A8%A1%E5%9D%97%E6%B3%A8%E9%87%8A)

　　　　[2.4.13 细节注释](#2413-%E7%BB%86%E8%8A%82%E6%B3%A8%E9%87%8A)

[3 变量声明](#3%E5%8F%98%E9%87%8F%E5%A3%B0%E6%98%8E)

　　[3.1 变量](#31-%E5%8F%98%E9%87%8F)

　　[3.2 条件](#32-%E6%9D%A1%E4%BB%B6)

　　[3.3 循环](#33-%E5%BE%AA%E7%8E%AF)

　　[3.4 类型](#34-%E7%B1%BB%E5%9E%8B)

　　　　[3.4.1 类型检测](#341-%E7%B1%BB%E5%9E%8B%E6%A3%80%E6%B5%8B)

　　　　[3.4.2 类型转换](#342-%E7%B1%BB%E5%9E%8B%E8%BD%AC%E6%8D%A2)

　　[3.5 字符串](#35-%E5%AD%97%E7%AC%A6%E4%B8%B2)

　　[3.6 对象](#36-%E5%AF%B9%E8%B1%A1)

　　[3.7 数组](#37-%E6%95%B0%E7%BB%84)

　　[3.8 函数](#38-%E5%87%BD%E6%95%B0)

　　　　[3.8.1 函数长度](#381-%E5%87%BD%E6%95%B0%E9%95%BF%E5%BA%A6)

　　　　[3.8.2 参数设计](#382-%E5%8F%82%E6%95%B0%E8%AE%BE%E8%AE%A1)

　　　　[3.8.3 闭包](#383-%E9%97%AD%E5%8C%85)

　　　　[3.8.4 空函数](#384-%E7%A9%BA%E5%87%BD%E6%95%B0)

　　[3.9 面向对象](#39-%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1)

　　[3.10 动态特性](#310-%E5%8A%A8%E6%80%81%E7%89%B9%E6%80%A7)

　　　　[3.10.1 eval](#3101-eval)

　　　　[3.10.2 动态执行代码](#3102-%E5%8A%A8%E6%80%81%E6%89%A7%E8%A1%8C%E4%BB%A3%E7%A0%81)

　　　　[3.10.3 with](#3103-with)

　　　　[3.10.4 delete](#3104-delete)

　　　　[3.10.5 对象属性](#3105-%E5%AF%B9%E8%B1%A1%E5%B1%9E%E6%80%A7)

[4 浏览器环境](#4-%E6%B5%8F%E8%A7%88%E5%99%A8%E7%8E%AF%E5%A2%83)

　　[4.1 模块化](#41-%E6%A8%A1%E5%9D%97%E5%8C%96)

　　　　[4.1.1 AMD](#411-amd)

　　　　[4.1.2 define](#412-define)

　　　　[4.1.3 require](#413-require)

　　[4.2 DOM](#42-dom)

　　　　[4.2.1 元素获取](#421-%E5%85%83%E7%B4%A0%E8%8E%B7%E5%8F%96)

　　　　[4.2.2 样式获取](#422-%E6%A0%B7%E5%BC%8F%E8%8E%B7%E5%8F%96)

　　　　[4.2.3 样式设置](#423-%E6%A0%B7%E5%BC%8F%E8%AE%BE%E7%BD%AE)

　　　　[4.2.4 DOM 操作](#424-dom-%E6%93%8D%E4%BD%9C)

　　　　[4.2.5 DOM 事件](#425-dom-%E4%BA%8B%E4%BB%B6)





## 1 前言


JavaScript在百度一直有着广泛的应用，特别是在浏览器端的行为管理。本文档的目标是使JavaScript代码风格保持一致，容易被理解和被维护。

虽然本文档是针对JavaScript设计的，但是在使用各种JavaScript的预编译语言时(如TypeScript等)时，适用的部分也应尽量遵循本文档的约定。



## 2 代码风格


## 文件
##### [建议] `JavaScript` 文件使用无 `BOM` 的 `UTF-8` 编码。

>UTF-8 编码具有更广泛的适应性。BOM 在使用程序或工具处理文件时可能造成不必要的干扰。

##### [强制] 文件名必须全部用小写，文件名分隔符用中划线连接，版本连接符用实心点，合并文件的文件名连接符用下划线.如： 

>`passport-core.min.js`和`reset-1.0_utils-1.0.css` 。

##### [建议] 在文件结尾处，保留一个空行。



## 3变量声明
-------------
* 声明变量必须加上 `var`  关键字
* 常量的形式如: `NAMES_LIKE_THIS` , 即使用大写字符, 并用下划线分隔
* 语句结束使用`;`结尾
* 使用驼峰式命名变量和函数 如：`var thisIsMyName;`
* 私有成员变量和方法命名以下划线开头，如：`var _this`
* 涉及Android的，一律大写第一个字母 如：`var AndroidVersion`
* 使用的ID的地方一定全大写 如：`var goodID`；
* 涉及iOS的，一律小写第一个，大写后两个字母 `var iOSVersion` 
* 禁止用new来实例化基本类型，错误的范例： ` var x = new Boolean(false) ` 
* 直接定义数组或对象，而不使用new关键字声明

```javascript
	//bad
	var a = new Array(), o = new Object();
	//bad
	var colors = new Array("red", "green", "blue");
	//bad
	var team = new Team();
	team.title = "bszTeam";
	team.count = 25;

	//good
	var a = [],o = {};
	// Good
	var colors = [ "red", "green", "blue" ];
	// Good  semi colon 采用 Followed by space 的形式
	var team = {
	    title: "bszTeam",
	    count: 25
	};
```
* 使用单引号来定义字符串


***
## 函数声明
* 禁止在代码块中声明函数.错误的范例：`if (true) {function foo() {}}`
* 函数参数大于3个时，应以对象形式作为参数集传递
* function declaration 和 function expression 的不同，function expression的()前后必须有空格，而function declaration 在有函数名的时候不需要空格， 没有函数名的时候需要空格。
* 函数调用括号前后不需要空格

```javascript
    function doSomething(item) {
	    // do something
	}

	var doSomething = function (item) {
	    // do something
	}

	// Good
	doSomething(item);

	// Bad: Looks like a block statement
	doSomething (item);
```
* 立即执行函数的写法, 最外层必须包一层括号
* "use strict" 决不允许全局使用， 必须放在函数的第一行， 可以用自执行函数包含大的代码段, 如果 "use strict" 在函数外使用， JSLint 和 JSHint 均会报错
```javascript
	// Good
	var value = (function() {

		// function body
		return {
		    message: "Hi"
		}
	}());

	// Good
	(function() {

		function doSomething() {
		    // code
		}

		function doSomethingElse() {
		    // code
		}

	})();
```


*** 
## null的使用场景

*  初始化一个将来可能被声明为一个对象的变量。
*  与一个可能是对象或者非对象的初始化变量相比。
*  传入一个对象待定的函数。
*  作为一个对象待定的函数的返回值。


* * * 
## 不适合null的使用场景

* 不要使用null来测试一个变量是否存在。
* 不要用null来测试一个没声明的变量。


* * * 
## undefined使用场景

* 永远不要直接使用undefined进行变量判断 
```javascript
  // Bad
 var person;
 console log(person === undefined);    //true
```

* 使用字符串 "undefined" 对变量进行判断
```javascript
// Good
console log(typeof person);    // "undefined"
```



* * * 
## 安全

* 审查用户输入
* 禁止通过在iframe使用script进行跨域回调
* 尽量在可能但不确定出现异常的地方（大量运算，AJAX请求，数组操作或DOM操作等）用**try-catch(e)**来抛出异常，这样有利于规模较大的项目中排查错误,输出异常抛出错误信息
* 禁止使用evel 函数
* with 非特殊业务， 禁用！！！



* * * 
## 面向对象

* 类中的成员变量使用构造函数来初始化
* 除非是必须移除类的成员，否则析构函数中对成员的销毁应通过将其设置为null，而不是用delete，因为重新赋值方式性能比用delete好
* 避免通过prototype方式污染内置对象原型链，插件除外



* * * 
## 作用域相关

* this仅用于类成员函数或对象中
* 通用全局函数，特别是通用组件代码应将业务逻辑放入闭包中，并通过“命名空间”将其引入
* 若函数中使用到全局变量，则访问全局变量时应使用window来引入
* 尽量使用优雅的模版写法，避免多行字符串用\加换行的方式或使用+运算连接字符串这种难维护的编码方式



* * * 
## 格式化

* 格式化代码 JSFomat
* 对于代码中需要进行==逻辑判断的变量，建议进行强制类型转换或使用===代替



* * * 
## 注释

* 文档注释遵循YUIDoc规范(http://yui.github.io/yuidoc/syntax/)
所有的文件、类、方法和属性都应该用合适的标记和类型进行注释。
	*  YUIDoc要求文档中至少要有一个class和constructor标记来定义类和构造函数；
	*  YUIDoc中注释块必须以/* * （至少两个星号）开头；
	*  方法、参数和返回值等必须有注释说明；
	*  单行注释使用//；
	*  对于代码中特殊用途的变量、存在临界值、函数中使用的hack、使用了某种算法或思路等需要进行注释描述；
	*  建议加入开发者个人信息及最后修改时间注释，虽然这些信息不会被YUIDoc解析显示
* 提交的代码需要通过 JSHint 审查



* * * 
## for

*  普通for循环, 分号后留有一个空格， 判断条件等内的操作符两边不留空格， 前置条件如果有多个，逗号后留一个空格.
```javascript
	var values = [ 1, 2, 3, 4, 5, 6, 7 ],
	    i, len;
	for (i=0, len=values.length; i<len; i++) {
	    process(values[i]);
	}
```
* for-in 一定要有 hasOwnProperty 的判断， 否则 JSLint 或者 JSHint 都会有一个 warn
```javascript
	var prop;

	for (prop in object) {

	    // 注意这里一定要有 hasOwnProperty 的判断， 否则 JSLint 或者 JSHint 都会有一个 warn ！
	    if (object.hasOwnProperty(prop)) {
	        console.log("Property name is " + prop);
	        console.log("Property value is " + object[prop]);
	    }
	}
```

***
##DEMO
```javascript
/**
 * == Javascript eXtension 模块 =========================================================================
 * @version 2.0
 * @author  YJL(<a href="mailto:YJL@gmail.com">YJL@gmail.com</a>)
 * @description 描述文字
 * -------------------------------------------------------------- 2015.02.26 ----------------------------
 */

var bsz = require('bsz');
/**
 * 注释
 */
routerApp.config(function($stateProvider, $urlRouterProvider) {
    var packageContext = this,
        $D = bsz.dom,
        $E = bsz.event,
        $H = bsz.http;

    // 输出字符串：Hello world!
    console.log('Hello world!');

    // 输出this === bsz.team的判断结果
    console.log(this === bsz.team);
});

```



***
##参考

* [google-style-guide](https://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml) 
* [w3c-guid](http://www.w3.org/TR/DOM-Level-2-HTML/html.html)
* [jshint-guid](http://jshint.com/)
* [alloyteam-code-guide](http://alloyteam.github.io/code-guide/#js-indentation) 