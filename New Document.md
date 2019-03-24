##javaScript
###概念
>JavaScript一种直译式脚本语言，是一种动态类型、弱类型、基于原型的语言.
###历史来历
>布兰登.艾奇在1955年,用了不到10天研发出来的,原名叫livescript,当时为了蹭java的热度,就改名为javaScript.
###JS的用途:
#####实现用户和浏览器的交互作用,具体表现:
+ 网页特效
+ app
+ 服务端开发
+ 网页小游戏
+ .....

###js的组成
+ ECMAScript
+ DOM
+ BOM

##ECMAScript
###ECMAScript的声明方式


		<html>
			<head>
				<title></title>
			</head>
			<body>
				<script>
					var 变量名=赋值
                </script>
			</body>

		</html>
	


####变量输出的类型
* number===========数字类型
* String===========字符串类型
* boolean==========布尔类型
* null=============空
* underfined=======声明未赋值
* Object===========对象类型


###ECMAScript基本语法---结构:
+ 流程控制
  - 顺序结构:从小到下,从左往右
  - 分支结构
     - if else
     - swith-case
     - if else else if else if
  - 循环结构:   
     - for
     - do while
     - while


###ECMAScript基本语法---关键字:
 + break 跳出单独执行
 + continue  跳过单独执行
 

###ECMAScript基本语法---数组:
>格式:

		<html>
			<head>
				<title></title>
			</head>
			<body>
				<script>
					var arr=[10,"你好","ex",true];
                </script>
			</body>

		</html>
>作用:可以一次存储多个变量,并且可以多种数据.

###数组---小技巧
+ arr.length   可以获取数组的长度或者个数
+ arr.length=0  可以用来清空数组


###数组---经典案例
>数组的反转

         <html>
			<head>
				<title></title>
			</head>
			<body>
				<script>
					  var arr=[10,20,30,40,50];
				      var newArr=[];
				      for(var i=arr.length-1;i>=0;i--){
				            newArr[newArr.length]=arr[i];
				        }
				       console.log(newArr)
                </script>
			</body>

		</html>
  
    
>数组的冒泡
  
      <html>
			<head>
				<title></title>
			</head>
			<body>
				<script>
				var arr=[20,30,100,60,40,80];
		       for(var i=0;i<arr.length;i++){
		       	 for(var j=0;j<arr.length-i;j++){
		       	 		 if(arr[j]>arr[j+1]){
		       	 	var temp=arr[j]
		       	 	arr[j]=arr[j+1]
		       	 	arr[j+1]=temp
		       	 }
		        }
		      }console.log(arr);
                </script>
			</body>

		</html>

###数组---API
+ push ==================增加一个元素,从最后的位置添加 返回的是增加之后数组的长度
+ pop====================删除一个元素,从最后开始删除,返回的是删除的元素.
+ shirt==================删除一个元素,从开头(arr[0])删除,返回的也是删除的元素;
+ unshift================增加一个元素,从开头(arr[0])增加,返回的是增加之后数组的长度
+ reverse================数组的反转,数组里面的元素变成倒序 不能从小到大,或者从大到小.
+ sort===================数组的冒泡排序,元素依次比较,数据从大到小或者从小到大排序;
+ splice=================splice(开始的索引,删除的个数,替换的元素)一般用于数组元素的删除和替换.
+ concat=================数组的拼接;
+ filter=================根据条件可以删除数组中的某些元素; 
+ join===================在每个数组后面加一个元素,返回的是字符串模式一般用来文字之间＋竖线一类的



###ECMAScript基本语法---函数:
>格式:

		<html>
			<head>
				<title></title>
			</head>
			<body>
				<script>
					function 函数名(){
                                      console.log("你回家");
 									}
                          函数名()   =======函数的调用
                </script>
			</body>

		</html>
>作用: 可以把需要重复使用的代码进行封装,然后在需要的时候调用;减少代码量;


###函数---参数
+ 形参:函数名后面笑括号里的变量
  + **arguments**--用来获取实参传给形参的个数
+ 实参:函数调用的时候,小括号里面的变量或者值;


###函数---返回值:
+ 函数中没有return,函数有返回值;
+ 函数在没有return,没有返回值;


###函数---经典案例
>数组的反转,函数封装

         <html>
			<head>
				<title></title>
			</head>
			<body>
				<script>
					  function getArr(arr){
				      var newArr=[];
				      for(var i=arr.lenth-1;i>=0;i--){
				            newArr[newArr.length]=arr[i];
				        }return newArr;
				       }var result=newArr([10,20,30,40]);
                        console.log(result);

                </script>
			</body>

		</html>
  
    
>数组的冒泡 ,函数封装.
  
      <html>
			<head>
				<title></title>
			</head>
			<body>
				<script>
				function getArr(arr){
		       for(var i=0;i<arr.length;i++){
		       	 for(var j=0;j<arr.length-i;j++){
		       	 		 if(arr[j]>arr[j+1]){
		       	 	var temp=arr[j]
		       	 	arr[j]=arr[j+1]
		       	 	arr[j+1]=temp
		       	 }
		        }
		      }
             } console.log(getArr([10,60,50,40,30]))
                </script>
			</body>

		</html>