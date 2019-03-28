 类型 typeof 
 复杂数据类型 object
 Array 是可遍历的对象
 Function 是可运行的对象
 JSON Object对象字面量是可枚举的对象 for(key in)

 type of 半吊子 typeof []无法与json{}区分
 有一个方法可以区分Array JSON Object 

 立即执行函数是闭包的温床

 Object.prototype.toString.call() 这个是判断的一种很好的方法

 1. 用对象字面量来做面对对象 区别于原型式的，他没有被实例化的需要Type，将在
 程序中就做类型检测。
 var Type = {};     组织代码
 2. 使用for循环来一次性加完，同步异步的问题使用闭包来将type作用域封闭起来，立即执行函数，
 同步执行，类型检测函数的定义，因为函数嵌套，形成了闭包，当函数再被调用时（异步）,找到定义时刻的type
 3. Object.prototype.String.call(obj)
 Object 祖先 顶级对象 函数才有prototype属性，原型上有这样的toString方法，解决typeof的尴尬
 "[object Object]"
 [object Array] 方法的执行方式可以被改变
 Object.prototype.toString.call(obj)