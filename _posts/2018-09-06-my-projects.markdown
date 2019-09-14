---
layout: post
title: Maxscript Donet
date: 2019-09-14 17:00:00.000000000 +09:00
---

#### Maxscript 和 Donet 交互

基本上donet的所有功能都可以在maxscript中实现

#### 变量，类的声明

Maxscript中提供了两种声明的方法
* dotnetObject
* dotnetClass

那他们之间又有声明区别呢？

dotnetClass的作用像是声明一个类型

C#写法：
```C#
string.Format("Hello dotnet Class");
```
等同于Maxscript写法：
```Maxscript
string = dotnetClass "System.string"
string.Format "Hello dotnet Class"
```

dotnetObject的作用像是声明一个实例

C#写法：
```C#
string objectExample = "Hello dotnet object";
```
等同于Maxscript写法：
```Maxscript
objectExample = dotnetObject "System.string"
objectExample = "Hello dotnet object"
```

#### 一些坑

之前使用的时候遇到的坑爹问题
* 载入的Dll或者编译的C#代码，除非你关掉Max，否则无法卸载
