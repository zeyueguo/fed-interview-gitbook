# 继承的方法有几种，可以简单说一些吗

### JavaScript 继承方式

### 原型链

```js
function Parent() {
  this.property = true
}
Parent.prototype.getParentValue = function () {
  return this.property
}
function Child() {
  this.Childproperty = false
}
Child.prototype = new Parent()
Child.prototype.getChildValue = function () {
  return this.Childproperty
}
var instance = new Child()
console.log(instance.getParentValue()) // true
```

### 构造函数

```js
function Parent() {
  this.colors = [‘red’, ‘blue’, ‘green’]
}
function Child() {
  // 继承Parent
  Parent.call(this)
}
var instance1 = new Child()
var instance2 = new Child()
instance1.colors.push(‘black’)
console.log(instance1.colors)  // [“red”, “blue”, “green”, “black”]
console.log(instance2.colors) // [“red”, “blue”, “green”]
```

### Object.create\(\)方法

```js
var person = {
  name: ‘Jiang’,
  friends: [‘Shelby’, ‘Court’]
}
var anotherPerson = Object.create(person)
console.log(anotherPerson.friends)  // [‘Shelby’, ‘Court’]
```

### Object.setPrototypeOf

```js
Object.setPrototypeOf(Child.prototype, Parent.prototype)
console.log(Child.prototype.constructor === Child) // true
```



## 参考

[JavaScript六种继承方式](https://xxxgitone.github.io/2017/06/12/JavaScript%E5%85%AD%E7%A7%8D%E7%BB%A7%E6%89%BF%E6%96%B9%E5%BC%8F/)

