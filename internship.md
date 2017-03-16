## 2017-03-16 滴滴

* 研究生的研究方向，为什么面前端

* JavaScript学的怎么样？ES6有看过吗？你觉得ES6什么比较好用？

* 箭头函数和普通函数的区别。

* promise多异步流程怎么实现

* 用express搭建的多人博客。带用户管理吗？什么叫多人博客？用户管理是怎么写的？都是你自己写的吗？数据库用的是什么？

* 你还用过其他的数据库吗？mongodb和mysql的区别。

* mongodb能做笛卡尔积吗？就是[表的联合查询](http://chenzhou123520.iteye.com/blog/1637397)。
```
在关系型数据库中，通过join连接操作符可以实现多个表联合查询。
而非关系型数据库的特点就是表之间是弱关联，mongodb不建议对多collection之间关联处理。
```

* 后端用过什么语言？什么会用的好一点？

* 做web开发nodejs相对于python、java有什么优势？我说高并发，然后面试官问python、java不能解决高并发吗？node是怎么解决高并发的？我说异步，然后问python不能做异步吗？
* node做web开发有什么缺陷？

	上面两个关于Node的问题的回答：

	[使用 Node.js 的优势和劣势都有哪些？](https://www.zhihu.com/question/19653241)

	[为什么要用nodejs？](http://blog.jobbole.com/100058/)

* vue做的是单页应用吗？你觉得vue这种MVVM框架和之前的框架有什么区别？数据双向绑定是怎么实现的？vue有用虚拟dom概念吗？

* 你的单页能做到按需加载吗？首次加载很慢能做到切到哪个tap再加载能做到吗？[路由懒加载](https://router.vuejs.org/zh-cn/advanced/lazy-loading.html)
```
借助Vue的异步组件 和 Webpack的代码分割
```
* 单页会保存场景吗？localStorage和vuex存储数据哪个方便？
```
vuex存储的数据刷新就没了，localStorage存储的数据就算关闭浏览器只要你不清除就一直都在。
可以组合vuex和sessionStorage，刷新的时候判断sessionStorage有没有保存cache，有的话初始化状态的时候再填进去
```
* 归并和快排的区别。快排哪个地方比归并好？快排为什么不稳定？时间复杂度分析。快排怎么样能尽量做到平均复杂度？
```
快速排序是从头和尾开始对元素进行比较,有可能把关键值相同的两个元素调换了位置,所以说是不稳定的。
随机化枢轴的选取
```
* 你觉得做前端需不需要掌握算法？我说了数据可视化，排序的递归写法怎么变成非递归写法？

* sql语言熟吗？批量更新，更新内容不同，怎么用一个语句实现？

* 你用java做过抓包？你的检索是自己写的吗？
```
倒排索引就是存储某个单词在一组文档中存储位置的映射。
```
* echarts渲染使用canvas渲染，你觉得为什么不用svg渲染？[canvas和svg的区别](http://www.wyzu.cn/2016/0415/115522.html)

* echarts中的交互是怎么用canvas来实现的？比如鼠标hover线变粗。折线图是哪几个图层实现的？
```
貌似是对整个canvas进行监听，获得里面对象的一些信息索引，然后再绘制对应效果
```
* 你学算法有接触过动态规划和贪心吗？说一下区别。
```
动态规划必须有dp状态、状态转移方程，无后效性(当前状态只影响下一个状态而不会影响之后的状态)。
贪心就是按照某个策略每步取最优值，并且达到全局最优。
```

* C有引用吗？c没有引用，c++有。

* 栈存储和堆存储的区别。栈存储基本类型，堆内存为new出来的对象分配内存空间，栈内存存储对象在堆内存中的访问地址。

## 2017-03-14 携程

* 什么时间可以实习？你想做前端还是后端

* 有没有实习经历

* 做的前端开发的项目

* 闭包什么时候使用？闭包的定义。怎么处理内存泄露的问题？

* 说一下promise的基本用法。resolve和reject的作用。多个数据源的请求数据回来之后再处理，怎么用promise实现。

* js中的面向对象和java的面向对象区别? [JavaScript面向对象 MDN](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Introduction_to_Object-Oriented_JavaScript)

* 函数式编程和面向对象编程区别。es6中的剪头函数就是函数式编程的。函数式编程就是定义一个函数然后调用它，这种开发快速直接。面向对象的话关系逻辑清晰，维护方便简单。

* 快速排序，是稳定还是不稳定排序？

* 你有问题或要求？

## 2017-03-14 搜狐Offer

## 2017-03-10 搜狐二面

1. 自我介绍

2. 为什么做前端，对前端的理解，我看你的简历是偏向算法。

3. 前端的路你觉得应该怎么走，哪些地方你觉得不足，前端也有很多方向，你怎么看？

4. vue最常用的双向绑定是怎么实现的？

5. 有做过移动端的页面吗？

6. 布局这块儿有什么好的方案？flex有没有遇到什么问题？

7. webpack代码打包是怎么做的？内部代码合并压缩丑化是怎么实现的？[webpack源码学习](https://github.com/youngwind/blog/issues/99)

8. phantomjs原理是什么？模拟用户交互

9. 你自学前端你感觉自己哪方面还需要增强？

10. 你什么时间能来实习？你以后的打算？

11. 你有什么问题问我吗？

## 2017-03-10 爱奇艺Offer

## 2017-03-09 阿里

1. 在项目中的角色和核心产出。你原来的服务层是怎么做的？

2. vue的数据双向绑定实现原理？让你用原生js实现你怎么做？

3. MongoDB大量数据如何提升查询效率？索引？

4. 除了vue其它框架还有了解吗？你可以告诉我你的加分项还有什么？

5. SAP工作内容？

6. [MVC、MVVM](http://www.ruanyifeng.com/blog/2015/02/mvcmvp_mvvm.html) 是什么？

7. 优化页面加载速度的方法

8. 性能优化离线缓存技术。

9. ES6相对于ES5新添了哪些属性？[ES6新特性概览](http://www.cnblogs.com/Wayou/p/es6_new_features.html)

10. 前端范围需要扩大，多了解一些框架、技术，多理解为什么这么实现，而不是直接用现有的框架。



## 2017-03-08 搜狐焦点

* 自我介绍

* 你有让自己印象深刻的项目或经历吗？

* 对vue体验最深的点。你怎么知道虚拟dom数据更新了。

* 前端的缓存策略。我说了http缓存和localStorage，问localStorage可以存什么样的数据。

* 单链表判环。我说快慢指针，面试官问为什么这样就可以判断有环。

* 数组去重。我说了两种方法，让我分析时间空间复杂度。hash值怎么计算，js中是弱类型，hash值的计算会复杂一点。

* 实现最小栈，时间空间复杂度分析。时间复杂度不变，降低空间复杂度。

* 虚拟dom中，dom树不同时间的快照，比较两个快照之间的差异。两个快照不是完全不同，只是通过dom操作才发生的差异。然后问那如果是两个树比较是否相同，时间复杂度分析。

	[如何实现一个 Virtual DOM 算法](https://github.com/livoras/blog/issues/13)

	1. 用JS对象模拟DOM树

	2. 比较两棵虚拟DOM树的差异

	3. 把差异应用到真正的DOM树上

* 你有什么问题吗？

* 你对前端的学习计划。

## 2017-03-06 爱奇艺二面

* 你为什么做前端开发？你觉得你在前端方面最突出的技能是什么？

* 介绍一下参加ACM的情况

* 你在参赛的过程中，你在团队中起到的角色？团队中合作方式是怎么确定的？

* 在这两年的比赛中你觉得其中有多少想法是来自于你？

* 你之前有做过实习吗？

* 介绍一下调查问卷这个项目

* 问卷的数据怎么保存？

* 这个是练习做的项目还是有上线的成品？

* 你在实现过程中有遇到什么难题？怎么解决的？

* 你正在改进的多人管理是怎么设计的？

* 你当时学vue的时候为什么选择做问卷调查这个项目？

* 你c++怎么样？有项目经验吗？

* erp这个项目中你主要做了什么？

* 前端技术HTML5，CSS3，JS中你最擅长的是哪一个？框架方面接触过Vue和Node。

* 三个箱子，里面分别放着苹果、梨、苹果和梨，标签也是一样，但是标签和箱子不对应，你只可以打开其中一个箱子，而且不可以看里面，拿出里面一个水果看是什么，然后迅速判断三个箱子装着什么？应该是挑贴着苹果和梨的箱子。不管是挑贴着苹果或梨的箱子答案是一样的，都不可以唯一确定。

* 你有什么问题问我吗？

## 2017-03-01 乐视金融

* jquery获取父元素：parent获取直接父元素，parents获取祖先元素

* jquery绑定事件：on、bind、live

* jquery中empty和remove的区别：empty移除元素文本，remove移除dom结点

* 原生js遇到的兼容问题：我说了绑定事件

* 原生js移除一个结点：removeChild

* 列举CSS hack：我说-webkit,-moz。下划线是哪个浏览器特有的？
面试官说：CSS3新属性有些浏览器不支持就加浏览器私有属性。而CSShack解决兼容问题是：在IE下实现1像素高度，可以使用IE下特有的hack下划线‘_’,然后font-size:0。

* CSS3实现动画几种方式：transition、animation，两者区别。

* 做过HTML5移动端页面吗？@media媒体查询，[rem](http://www.alloyteam.com/2016/03/mobile-web-adaptation-tool-rem/#prettyPhoto)，百分比，弹性盒子。

* 前端的构建工具：webpack，列举几个loader，json-loader,css-loader

* 列举node的系统模块：http，fs(I/O操作)，system(管理与运行环境相关的属性)

* mysql和mongoDB的区别。数据库怎么选择。

* 介绍你写的爬虫系统。批量爬取被封ip怎么解决？


## 2017-02-24 爱奇艺一面

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

## 2017-02-14 粉笔网

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


