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


