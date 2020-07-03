### synchronized 锁/同步

在Java中，synchronized关键字是用来控制线程同步的，就是在多线程的环境下，用synchronized来控制代码段不被多个线程同时执行。synchronized既可以加在一段代码上，也可以加在方法上。那么synchronized同步的是方法还是对象呢？

```
synchronized(?){
	...
}
```

synchronized锁的是括号中的对象，如果另外一个线程能影响到该对象，则会锁住该代码块

如果括号中是静态对象或类的Class对象,因为静态对象跟Class都是属于类，所以synchronized会锁住类的代码块，任何该类型的对象调用都会被synchronized同步

如果括号中是普通对象，则锁住的是能影响到该对象的线程



