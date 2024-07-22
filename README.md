# Java-Knowledge

## Static Keyword
When you declare a variable or a method as static, it belongs to the class, rather than a specific instance. This means that only one instance of a static member exists, even if you create multiple objects of the class, or if you don’t create any. It will be shared by all objects.

### Static Variables

```java
public class Counter {
  public static int COUNT = 0;
  Counter() {
    COUNT++;
  }
}
```

The COUNT variable will be shared by all objects of that class. When we create objects of our Counter class in main, and access the static variable.

```java
public class MyClass {
  public static void main(String[] args) {
    Counter c1 = new Counter();
    Counter c2 = new Counter();
    System.out.println(Counter.COUNT);
  }
}
// Outputs "2"
```


### Static Methods
It is used for altering static contents of the class. There are some restrictions of static methods :

1. Static method can not use non-static members (variables or functions) of the class.
2. Static method can not use this or super keywords.

```java
public class Counter {
  public static int COUNT = 0;
  Counter() {
    COUNT++;
  }

  public static void increment(){
    COUNT++;
  }
}
```

Static methods can also be called from instance of the class.

```java
public class MyClass {
  public static void main(String[] args) {
    Counter.increment();
    Counter.increment();
    System.out.println(Counter.COUNT);
  }
}
// Outputs "2"
```

### Static Blocks
Static code blocks are used to initialise static variables. These blocks are executed immediately after declaration of static variables.

```java
public class Saturn {
  public static final int MOON_COUNT;

  static {
    MOON_COUNT = 62;
  }
}

public class Main {
  public static void main(String[] args) {
    System.out.println(Saturn.MOON_COUNT);
  }
}
// Outputs "62"
```


### Static Nested Classes
A class can have static nested class which can be accessed by using outer class name.


```java
public class Outer {

  public Outer() {
  }

  public static class Inner {
    public Inner() {
    }
  }
}
```
In above example, class Inner can be directly accessed as a static member of class Outer.

```java
public class Main {
  public static void main(String[] args) {
    Outer.Inner inner = new Outer.Inner();
  }
}
```

One of the use case of static nested classes in Builder Pattern popularly used in java.


## Final Keyword
Final keyword is a non-access modifier used for classes, attributes & methods, which makes them non-changeable (impossible to inherit/reassign/override).

### Classes 
Classes marked as final cannot be extended (inherited).

### Variables
Variables marked as final connot be reassigned.

### Methods
Methods marked as final cannot be overriden.


## Threading
Allows us to do multiple things at once.
When multiple threads are executed at the same time. Then it is called as multi-threading.

### Multitasking in Java
They are of two type:-
1. Processed-bases multitasking: This type is heavy and requires a lot of time. This is because the program takes a lot of time to switch between differenct processes.

2. Thread-based multitasking: These are light-weight and require short time to switch between the processes.

### Thread life-cycle
A thread always remains in one of the few states.
The thread model consists of various states.

1. New: The model is in the new state when the code is not yet running.
2. Running stage or active stage: This is the state when the program is under execution or in ready to execute stage.
3. Suspended Stage: This is the state when the process is paused (temporarily) due to some reasons.
4. Blocked Stage: This is the state when thread is waiting for some resources. In the blocked state, the thread scheduler clears the queue by rejecting unwanted threads which are present.
5. Terminated Stage: This state stops a thread's execution immediately. A terminated thread means that it is dead and is no longer available for use.

## String, StringBuffer, StringBuilder


## Mutable & Immutable
