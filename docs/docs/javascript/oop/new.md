---
title: 构造函数
date: 2021-02-13
---

## 类和实例和对象的比较

> 类：类型，对具体事物的一个抽象认识，是抽象出来的结果。
>
> 类的说明：类就是一组相关属性和行为定义的集合。
>
> 属性：对于事物特征的描述，一般是名词或者形容词。

- 传统的编程语言：java、C# → class
- ES3.0 和 ES5.0 没有类的概念 ECMAScript → ES
- 构造函数模拟类
- ES6.0 有类概念 → class

> 对象：事物的具体表现。

- 创建对象：new 类名();
- ES3.0 和 ES5.0 ： new 构造函数名();

> 类和实例关系：类是实例的**模板**，实例是类的一个具体的实现。

## 自定义构造函数创建对象

- 自定义构造函数的语法：

  > function 构造函数名(形参…){
  >
  > this.key = value;
  >
  > this.key = value;
  >
  > }

- 创建对象：new 构造函数(实参…);

## new 这个关键字干了什么？

> 1. 在内存中申请了一块空间，存放了一个对象。（看不见）
> 2. 让构造函数内部的 this 指向该空间（看不见）
> 3. 通过 this 向内存中空的对象中添加属性和方法（看的见）
> 4. new 关键字最后将 this 返回给外部变量（看不见）

```js
var temp = {}; // 声明一个空对象
temp.__proto__ = Func.prototype; // 更改temp.__proto__指向
Func.call(temp); // 更改this指向
return temp; // 返回这个新对象
```

## 构造函数和实例对象的关系

- 构造函数：构造函数是对象的模板。
- 实例对象：具体存在的，对象是类的一个实例。

## 构造函数和普通函数的区别

> 相同：都是函数

> 不同：命名规范： +构造函数：帕斯卡 +普通函数：驼峰

> 调用方式：
> \+ 构造函数： new 构造函数();
> \+ 普通函数：普通函数();

- 构造函数：
  - 内置的构造函数：Object、Date、Array
  - 自己定义的：Dog、Cat、Hero