# JavaScript编码规范

## 1 声明

####1.明变量必须加上 var 关键字
####2.常量的形式如: NAMES_LIKE_THIS, 即使用大写字符, 并用下划线分隔
####3.语句结束使用;结尾
####4.使用驼峰式命名变量和函数 如：var thisIsMyName;
####5.私有成员变量和方法命名以下划线开头，如：var _this；
####6.涉及Android的，一律大写第一个字母 如：var AndroidVersion;
####7.使用的ID的地方一定全大写 如：var goodID
####8.涉及iOS的，一律小写第一个，大写后两个字母 var iOSVersion;
####9.函数参数大于3个时，应以对象形式作为参数集传递.
####10.禁止在代码块中声明函数，错误的范例：if (true) {function foo() {}}
####11.禁止用new来实例化基本类型，错误的范例：var x = new Boolean(false)；
####12.直接定义数组或对象，而不使用new关键字声明，错误的范例：var a = new Array();var o = new Object()；
####13.使用单引号来定义字符串
文件名必须全部用小写，文件名分隔符用中划线连接，版本连接符用实心点，合并文件的文件名连接符用下划线，如：passport-core.min.js和reset-1.0_utils-1.0.css。