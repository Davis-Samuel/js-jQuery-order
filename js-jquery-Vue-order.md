# 1.js基础

- ![image-20200219211015247](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200219211015247.png)
- ![image-20200219212932138](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200219212932138.png)
- ![image-20200219211252747](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200219211252747.png)
- ![image-20200219211514566](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200219211514566.png)
- ![image-20200219211814646](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200219211814646.png)
- ![image-20200219211632689](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200219211632689.png)
- ![image-20200219212249077](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200219212249077.png)
- ![image-20200219212650447](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200219212650447.png)

# 2.严格检查模式

- **‘user strict’；**  **必须写在js的第一行**
- **局部变量尽量用 let 定义，前提是支持ES6语法**

# 3.数据类型

## 字符串

- ![image-20200220221555007](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200220221555007.png)
- ![image-20200220221701515](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200220221701515.png)
- ![image-20200220221913891](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200220221913891.png)

## 数组

- ![image-20200220222904201](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200220222904201.png)
- ![image-20200220223754833](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200220223754833.png)
- ![image-20200220224035196](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200220224035196.png)
- ![image-20200220224227949](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200220224227949.png)
- ![image-20200220224432127](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200220224432127.png)

## 对象

- ![image-20200221121954120](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200221121954120.png)
- ![image-20200221122339832](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200221122339832.png)

## 流程控制

- ![image-20200221130736476](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200221130736476.png)
- ![image-20200223150938492](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200223150938492.png)

## Set，Map

- ![image-20200221132651712](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200221132651712.png)

# 4.函数

## 函数基础

- ```JavaScript
  function abs(x) {
      if (x >= 0) {
          return x;
      } else {
          return -x;
      }
  }
  ```

- ```javascript
  var abs = function (x) {
      if (x >= 0) {
          return x;
      } else {
          return -x;
      }
  };
  ```

- ```JavaScript
  function abs(x) {
      //判断x的类型不是number，就抛出异常
      if (typeof x !== 'number') {
          throw 'Not a number';
      }
      if (x >= 0) {
          return x;
      } else {
          return -x;
      }
  }
  ```

## argument

-  它只在函数内部起作用，并且永远指向当前函数的调用者传入的所有参数。利用arguments，你可以获得调用者传入的所有参数。也就是说，即使函数不定义任何参数，还是可以拿到参数的值

- ```JavaScript
  function abs(x) {
      if (arguments.length === 0) {
          return 0;
      }
      var x = arguments[0];
      return x >= 0 ? x : -x;
  }
  
  abs(); // 0
  abs(10); // 10
  abs(-9); // 9
  ```

## rest

- rest参数只能写在最后，前面用...标识，从运行结果可知，传入的参数先绑定a、b，多余的参数以数组形式交给变量rest，所以，不再需要arguments我们就获取了全部参数。

  如果传入的参数连正常定义的参数都没填满，也不要紧，rest参数会接收一个空数组（注意不是undefined）。

- ```JavaScript
  function foo(a, b, ...rest) {
      console.log('a = ' + a);
      console.log('b = ' + b);
      console.log(rest);
  }
  
  foo(1, 2, 3, 4, 5);
  // 结果:
  // a = 1
  // b = 2
  // Array [ 3, 4, 5 ]
  
  foo(1);
  // 结果:
  // a = 1
  // b = undefined
  // Array []
  ```


# 面向对象：

## 方法：

- ![image-20200228083352390](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200228083352390.png)

- ![image-20200228083504398](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200228083504398.png)
- ![image-20200228083519657](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200228083519657.png)

# 内部对象

## Date

- ![image-20200228083628831](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200228083628831.png)

## JSON入门

- ![image-20200228083700487](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200228083700487.png)
- ![image-20200228083721919](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200228083721919.png)

# BOM对象

## window对象

- ![image-20200228083829817](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200228083829817.png)

## Navigator对象

- 大多时候不使用，因为可以认为修改

## document对象

- ![image-20200228084106832](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200228084106832.png)

## location对象

- 修改你当前访问的地址
- ![image-20200228084133954](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200228084133954.png)

# DOM对象

- 获取更新节点：

  ![image-20200229131602604](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200229131602604.png)

  ![image-20200229131656241](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200229131656241.png)

  ![image-20200229131825549](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200229131825549.png)

- 删除节点：![image-20200229131506445](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200229131506445.png)

- 添加：

  ![image-20200229131724493](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200229131724493.png)

- ![image-20200301111358661](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200301111358661.png)

# 操作表单验证

- ![image-20200302121700779](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200302121700779.png)

- 引入md5加密的js地址：

  ```javascript
  <script src="https://cdn.bootcss.com/blueimp-md5/2.10.0/js/md5.js"></script>
  
  <!--格式md5(pwd)-->
  ```

# JQuery

- 学习视频：https://www.bilibili.com/video/av40716170
- 辅助文档：http://jquery.cuishifeng.cn/

- 在线引入JQuery:

  ```javascript
  <script src="https://code.jquery.com/jquery-3.1.1.min.js"></script>
  ```

- **公式：$(selector).action()**

- ![image-20200302123308463](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200302123308463.png)

  **给id选择器这个部分，一个click点击动作，点击之后执行function(){**

  **alter('hello......')}**

- **css选择器，jQuery都能用。**

- **标签选择器：$('p').click();    id选择器：$('#id').click();     类选择器：$('.class').click();** 

- 获取鼠标当前的一个坐标：

  ```JavaScript
  <!DOCTYPE html>
  <html>
  <head>
  	<title></title>
  </head>
  <script src="https://code.jquery.com/jquery-3.1.1.min.js"></script>
  <body>
  
  <!--页面加载完毕后，获取鼠标当前的一个坐标。$()表示页面加载完毕后-->
  鼠标坐标为：<span id="mouse"></span>
  <div id="move" style="height: 1000px;width: 1000px;background: red;border-width: 2px;">
  	鼠标在此移动
  </div>
  
  <script>
  	$(function(){
  		$('#move').mousemove(function(e){
  			$('#mouse').text('x:' + e.pageX + 'y:' + e.pageY)
  		})
  	});
  </script>
  </body>
  </html>
  ```

- 操作dom：![image-20200302130431847](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200302130431847.png)

- 先先写一个入口函数：

  ```js
  $(function(){});
  ```

- ![image-20200303133340821](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200303133340821.png)

- ![image-20200303133834421](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200303133834421.png)
- ![image-20200303144027350](C:\Users\91566\AppData\Roaming\Typora\typora-user-images\image-20200303144027350.png)



