
## 2017-02-24

* 问下面代码输出什么
```
for(var i = 0; i < 5; i++){
	setTimeout(()=>{
		console.log(i);
	}, 0);
}//5 5 5 5 5
```
解释为什么会出现上面这种情况，我回答了执行栈

然后下面这段代码输出什么

```
for(let i = 0; i < 5; i++){
	setTimeout(()=>{
		console.log("three:", i);
	}, 0);
}//0 1 2 3 4
```

* 给下面这样一个树结构，输出树结点
```
{
  left: { ... },
  right: { ... },
  value: 1
}
```

我的代码
```
function logTree(node){
  if(node == null) return;
  logTree(node.left);
  console.log(node.value);
  logTree(node.right);
}
```
然后说这是左－根－右，中序遍历

给下面这颗树，用上面代码输出的结果是什么
```
var tree = {
  left: {
    left: { value: 3 },
    right: { value: 4 },
    value: 1
  },
  right: {
    left: { value: 5 },
    right: { value: 6 },
    value: 2
  },
  value: 0
}
```
画了下树结构，输出3 1 4 0 5 2 6

* 介绍vue和vuex：

	[vue](http://www.csdn.net/article/1970-01-01/2825439)：组件化开发，[虚拟dom](http://www.cnblogs.com/lvyongbo/p/5931636.html)、数据双向绑定

	[vuex](http://vuex.vuejs.org/zh-cn/intro.html): 集中存储所有组件共享的状态。当有多个组件共享状态时，把共享状态抽取出来集中管理。

* webpack和其它打包工具比好在哪儿？

	webpack是一个模块化加载器兼打包工具，同时支持AMD和CMD加载规范。优势是：

1. 代码分割

	webpack支持两种依赖加载：同步和异步。同步的依赖会在编译时直接打包输出到目的文件中；异步的依赖会单独生成一个代码块，只有在浏览器中运行需要的时候才会异步加载该代码块。

2. Loaders

	在默认情况下，webpack只能处理JS文件，但是通过加载器我们可以将其他类型的资源转换为JS输出。

3. 插件机制

	webpack提供了强大的插件系统，当webpack内置的功能不能满足我们的构建需求时，我们可以通过使用插件来提高工作效率。

* 介绍mongodb

1. MongoDB的提供了一个面向文档存储，操作起来比较简单和容易。
2. 你可以在MongoDB记录中设置任何属性的索引 (如：FirstName="Sameer",Address="8 Gandhi Road")来实现更快的排序。
3. 你可以通过本地或者网络创建数据镜像，这使得MongoDB有更强的扩展性。
4. 如果负载的增加（需要更多的存储空间和更强的处理能力） ，它可以分布在计算机网络中的其他节点上这就是所谓的分片。
5. Mongo支持丰富的查询表达式。查询指令使用JSON形式的标记，可轻易查询文档中内嵌的对象及数组。
6. MongoDb 使用update()命令可以实现替换完成的文档（数据）或者一些指定的数据字段 。
7. Mongodb中的Map/reduce主要是用来对数据进行批量处理和聚合操作。
8. Map和Reduce。Map函数调用emit(key,value)遍历集合中所有的记录，将key与value传给Reduce函数进行处理。
9. Map函数和Reduce函数是使用Javascript编写的，并可以通过db.runCommand或mapreduce命令来执行MapReduce操作。
10. GridFS是MongoDB中的一个内置功能，可以用于存放大量小文件。
11. MongoDB允许在服务端执行脚本，可以用Javascript编写某个函数，直接在服务端执行，也可以把函数的定义存储在服务端，下次直接调用即可。
12. MongoDB支持各种编程语言:RUBY，PYTHON，JAVA，C++，PHP，C#等多种语言。
13. MongoDB安装简单。

## 2017-02-14

* CSS中相对定位与绝对定位的区别
```
relative相对元素本身位置定位
absolute相对于父元素position:relative，如果没有相对于body定位

绝对定位脱离文档流
```

* display的属性：block、inline、inline-block区别。还有什么属性，我说了flex，然后简单介绍flex。

* 对JS原型有什么了解，用原型创建对象和普通new一个对象有什么区别。
```
创建对象的三种方法：工厂模式、构造函数、原型

工厂模式——无法判断对象类型：
function person(name){
	var o = new Object();
	o.name = name;
	return o;
}

构造函数模式——每个方法都要在每个实例上重新创建一遍：
function Person(name){
	this.name = name;
	this.sayName = function(){alert(this.name);}
}
var person = new Person("kad");
alert(person.constructor == Person); // true
alert(person instanceof Person); // true
不同实例的同名函数是不相等的

原型——使用原型对象的好处是可以让所有对象实例共享它所包含的属性和方法
function Person(){}
Person.prototype.name = "kad";
Person.prototype.sayName = function(){alert(this.name);}
var person = new Person();
```

* JS继承的几种方法
```
1. 原型链继承：将父类的实例作为子类的原型
function Father(name){
	this.name = name;
}
Father.prototype.sayName = function(){
	return this.name;
}
function Child(){}
Child.prototype = new Person("kad");
var child = new Child();
child.sayName();//'kad'

缺点：所有子类共享父类实例，如果某个子类修改了父类，其他子类继承会出问题。
在构造子类型实例时不能给父类传参

2. 构造函数继承
function Parent(name){
	console.log(this);
	this.name = name;
	this.sayName = function(){
		console.log(this.name);
	}
}
function Child(name){
	this.parent = Parent;//此时Parent中的this指向的是Child，也就是把Parent中的属性和方法都给了Child
	this.parent(name);
	//这里直接delete this.parent也可以
}
var child = new Child("kad");
child.sayName(); //'kad'
console.log(child); 
/**
Child
-name: "kad"
-parent: Parent
-sayName: ()
*/

缺点：无法继承父类原型链上的属性和方法。

3. call、apply实现继承
function Parent(name){
	console.log(this);
	this.name = name;
	this.sayName = function(){
		console.log(this.name);
	}
}
function Child(name){
	Parent.call(this, name);
}
var child = new Child("kad");
child.sayName();//'kad'
console.log(child);
/**
Child
-name: "kad"
sayName: ()
*/
```

* 怎么理解闭包，闭包用在什么地方
```
读取函数内部变量
让变量值始终保存在内存中
```

* 怎么理解同步异步。然后问谁来执行当前任务，我说了执行栈和任务队列。又问你认为ajax是在js线程中执行的？怎么理解线程？我说每次只做一件事情。
```
同步：阻塞
异步：非阻塞
```

* 支付宝pc端支付时出现二维码，手机端扫描二维码支付成功后，pc端会跳转到支付成功页面，如何实现的？
```
手机端支付成功返回给服务器一个标识，而pc端二维码页面加载完成，http连接会断开，这时服务器怎么把支付成功的标识返回给pc端？
我说了ajax轮询（这个方法服务器压力大），html5的websocket
```
然后接着问websocket和http的keep-alive的区别。
```
http长连接需要每次发送header
```

* http协议中get和post的区别

* 记住密码自动登录怎么实现？cookie

* [vue数据双向绑定实现机制](https://segmentfault.com/a/1190000006599500)

* CSS3中transition（过渡）和transform（变形）的区别

* AngularJS有没有学过


