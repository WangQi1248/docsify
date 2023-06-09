# 第6章 方法

方法也叫函数，它可以将具有独立功能的代码进行**封装**，从而提高代码的**复用性**。学习方法最重要的就是3点。

- 方法的格式
- 方法的参数
- 方法的返回值

我们最先见到的方法就是main方法，main方法是由JVM自动调用的。除了main方法我们还可以自定义一些方法，然后再自己调用方法。

> **定义方法**

方法需要定义在类的大括号里面，格式如下

```java
public static 返回值类型  方法名(形参列表){
    ...方法体...
    return 返回值;
}
```

```java
- 【方法名】
	给完成此功能的代码片段取个名字，方便阅读
- 【形式参数】
	形参列表本质上是几个暂时没有值变量，把该变量当做未知数在方法中使用。
- 【方法体】
	完成具体功能的代码
- 【return 返回值】
	结束方法，并把返回结果
- 【返回值类型】
	方法执行结果的数据类型，没有结果用返回值类型void表示
```

定义一个求两个整数和的方法。假设两个数分别为x和y，那么方法定义如下

```java
public static int getSum(int x,int y){
    int sum=x+y;
    return sum;
}
```



> **调用方法**

方法定义了是不会自动执行的，需要调用才能执行。方法可以在任意的地方调用，因为程序的入口是主方法，所以我在主方法中来做演示。

```java
public static void main(String[] args){
    //调用getSum方法，求3和4的和。把结果赋值给sum
    int sum=getSum(3,4);
    System.out.println(sum);
    
    //调用getSum方法，求5和8的和。把结果重新赋值给sum
    sum=getSum(5,8);
    System.out.println(sum);
}
```



> **注意事项**

```java
- 方法必须写在类中，一个类中可以写多个方法
- 方法定义没有顺序
- 方法不调用不执行，调用一次执行一次
- 方法可以在任意方法中调用
- 方法有返回值类型，必须写return语句。 
```

