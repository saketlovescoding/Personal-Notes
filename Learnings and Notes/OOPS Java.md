
A class is a template for an object. It is named group of methods and properties.
An object is an instance of a class.
When we create an object of a class it is called its instance

A class is a logical construct, it does not exist in real. Object is an objective reality.
Object occupies space in memory

Object has 3 things:-
- state of the object
- identity of the object
- behavior of the object

(Dot) operator helps to access the instance variables.
Variables inside the object are called *instance variables*.

![[Pasted image 20250819203159.png]]


When we create an object of class, it means we instantiated an object;
By default values of objects is null
Constructors defines what will be the values of the variables when we create an object
Constructor is a special type of function in the class
this keyword is used to refer to the current object

Having different constructers means constructor overloading

We can call one constructor from another constructor

*Note*:- If we have lets say a parameterized constructor, then we Java does not create any default constructor on its own. We have to do it manually


### Wrapper Classes

Integer is a wrapper class of int. Integer is an object, int is a primitive variable

Java is by value.

*Final Keyword* -> Prevents the content from being modified.
Final variables have to be initialized when we declare it.

final can also be used with objects, but it only freezes the reference, not the state.
but we can change the values of it

![[Pasted image 20250819213015.png]]


When a non-primitive is final, we cannot reassign it.


### Garbage Collection


We cannot destroy object manually, but we can decide what happens when the GC removes the object

Finalize method is called when java is doing garbage collection

![[Pasted image 20250819213829.png]]



### Packages

- packages are containers of classes. A package is just a folder. In a package, every class name must be unique 

![[Pasted image 20250820062612.png]]

- There can be multiple top level classes inside a class but only one public class, which should match with the name of the file.
- Generally it is recommended to have .java file for each class.


### static keyword

- We use static keyword when a property is object independent, for example, in a human class the population property is going to be same for every human.
- To use a static property or method we use the class Name to call it.

![[Pasted image 20250820064927.png]]


Main method is a static method, because it is the entry point. So if is the entry point then we should be able to run it without creating any object, that is why we put static in front of it.

- inside static methods, we can only use static methods, or we have to reference their object.

### **Where to use `static`?**

- **Variables** → shared across all objects.
    
- **Methods** → utility methods, no object needed.
    
- **Blocks** → run once for class setup.
    
- **Nested classes** → independent helper classes inside another class.
    
- **Imports** → cleaner code for common static methods/constants.
  

We can have static methods and properties inside a non-static method

Every method at the end has to be run in a static method i.e. main method

We cannot use this keyword inside a static method

- A static block is run only once when the class is loaded

![[Pasted image 20250820071825.png]]

Config will only run once, when we create its first object.


Outside classes cannot be static. Inner classes can be static

![[Pasted image 20250820072843.png]]

the MainHelper class does not depend on Main class, we can use it without creating objects of Main class.

### Singleton Class

- When we want only one instance of an object.

![[Pasted image 20250820075319.png]]

Instance of a singleton class is always static as it is only one and can be used globally.


### Inheritance

Child class has access to members of the base class. 
We use the extends keyword to inherit properties of base class

![[Pasted image 20250820085948.png]]

We use super keyword to call the constructor of the parent class

If you don’t write it explicitly, Java **automatically inserts `super()` (no-args)** as the first line of your constructor — **but only if the parent has a no-arg constructor.**

![[Pasted image 20250820090634.png]]

`super()` must always be the **first statement** in a constructor.

![[Pasted image 20250820091300.png]]

This is wrong, As parent class reference variable cannot access the child class members.

Parent class has no access to the child class members, and the members that can be accessed depends in the type of reference variable and not the actual object

### 🚨 Important Rule

**For Variables:** The reference type determines which variable is accessed, not the object type.

**For Methods:** The object type determines which method is called (polymorphism).


Child class reference variable cannot hold the object of the parent class.


- Multiple inheritance is not supported in java.

There is single, hierarchical inheritance(more than one classes inherit a single class).


### Polymorphism

It means many ways to represent, a single entity or item

There are two types of polymorphism
- compile time polymorphism(static binding) -> method overloading
- runtime polymorphism(dynamic binding) -> method overriding

*Method Overloading* -> same name but arguments, types, return types and ordering can be different. Example- multiple constructors

*Method Overriding* -> when child class has same method as parent class

![[Pasted image 20250820223928.png]]

- **Dynamic method dispatch** is the mechanism in Java (and other OOP languages) that determines **which overridden method gets called at runtime based on the actual object type**, not the reference type.

![[Pasted image 20250820224914.png]]


Every class inherits the object class


### Final keyword

- final keyword can be used to stop method overriding.
- if a method is final it cannot be overridden.

![[Pasted image 20250820225602.png]]


![[Pasted image 20250820225649.png]]

- If we want to stop the class from being inherited, we can use the final keyword.
- **All methods become “effectively final”** in the final class — not because they are explicitly `final`, but because there’s no subclass where you could override them.


### Static methods

- Static methods cannot be overridden in java

![[Pasted image 20250820230801.png]]


![[Pasted image 20250820230833.png]]

- **Static methods → early binding → compile-time resolution**
    
- **Non-static methods → late binding → runtime resolution (true overriding)**


You can inherit but you cannot override a static method


### Encapsulation

Wrapping up the implementation of the data members and methods in a class. 

It hides the data in single entity or unit, from the outside world
- Encapsulation is the implementation stuff.
- Encapsulation works on internal working

Getters and setters are examples of encapsulation


### Abstraction

- Abstraction is hiding implementation details and showing only the essential features to the user.
- Abstraction solves the design level issue
- Abstraction solves what need to be shown externally to the user.

Abstraction uses abstract classes and interfaces



![[Pasted image 20250820233342.png]]




![[Pasted image 20250820233501.png]]


### Access Modifiers

- *default* - when we do not give any access modifier, we cannot access in different package. inside same package we can use it.
- *protected* - we can access the these variables in the same package and subclass (even if they are not part of the same package)
- *private* - only inside the class
- *public* - access is everywhere


### Packages

- User defined and in-built 

|Package Name|Purpose / What it Contains|Examples of Classes|
|---|---|---|
|**`java.lang`**|Core classes (auto-imported)|`String`, `Math`, `Object`, `System`, `Thread`|
|**`java.util`**|Utility classes & data structures|`ArrayList`, `HashMap`, `HashSet`, `Date`, `Collections`, `Scanner`, `Random`|
|**`java.io`**|Input/Output (file handling, streams)|`File`, `BufferedReader`, `InputStream`, `OutputStream`, `PrintWriter`|
|**`java.net`**|Networking (URLs, sockets)|`URL`, `Socket`, `ServerSocket`, `HttpURLConnection`|
|**`java.sql`**|Database access using JDBC|`Connection`, `ResultSet`, `Statement`, `PreparedStatement`|
|**`javax.swing`**|GUI development|`JFrame`, `JButton`, `JLabel`|
|**`javax.servlet`**|Web server components|`HttpServlet`, `ServletRequest`, `ServletResponse`|
|**`javax.xml`**|XML processing|`DocumentBuilder`, `Transformer`|
|**`java.time`**|Date and time API (Java 8+)|`LocalDate`, `LocalTime`, `LocalDateTime`, `Duration`|
|**`java.security`**|Security features|`MessageDigest`, `KeyPair`, `Signature`|

java.lang is automatically imported, we do not need to import

Object class is the top most class. Every class extends the object class indirectly or directly.


### instanceOf

![[Pasted image 20250823102025.png]]


### getClass

![[Pasted image 20250823102126.png]]



### Abstract Classes

- Tell what should be done by the child class, without telling how to do it.

*Note* - If a class has even one abstract method, the class should be abstract as well.

The abstract methods are implemented by overriding them in child class

- We cannot create abstract constructors and abstract static methods in the abstract class.
- We can create normal static methods and static variables though.

And since we cannot directly create objects of abstract class, so it does not make sense to have a constructor for it.

- Abstract class cannot be final as final class cannot be extended, but abstract classes need to be inherited.

Abstract classes do not support multiple inheritance.

![[Pasted image 20250823152649.png]]



### Interfaces

- Interfaces contain only abstract methods.
- Interfaces only have static and final variables, we cannot change those


| Feature / Aspect                 | **Interface**                                                                                                                       | **Abstract Class**                                                                                                       |
| -------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| **Purpose**                      | Defines a **contract** (what to do) without enforcing how.                                                                          | Used for **partial abstraction** — can define both what to do **and** how to do it.                                      |
| **Methods**                      | Can have **abstract**, **default** (Java 8+), **static**, and **private** (Java 9+) methods. All methods are **public** by default. | Can have **abstract** and **concrete** methods. Methods can have any access modifier (`public`, `protected`, `private`). |
| **Variables**                    | All variables are **public static final** (constants).                                                                              | Can have **instance** variables, static variables, and constants.                                                        |
| **Constructors**                 | **Not allowed.** Interfaces cannot be instantiated or have constructors.                                                            | **Allowed.** Can initialize common state for subclasses.                                                                 |
| **Inheritance**                  | A class can **implement multiple interfaces** (supports multiple inheritance of type).                                              | A class can **extend only one abstract class** (single inheritance).                                                     |
| **Access Modifiers for Members** | Methods are implicitly `public`; variables implicitly `public static final`.                                                        | Members can have **any** access modifier.                                                                                |
| **When to use**                  | When you just need to **define capabilities / APIs** that multiple classes can share (no shared code or state).                     | When you want to **share some code / state** while still forcing subclasses to implement certain methods.                |
| **Example Keywords**             | `interface` keyword; implemented using `implements`.                                                                                | `abstract` keyword; extended using `extends`.                                                                            |
| **Java 8+ Enhancements**         | Can contain default and static methods to provide limited implementation.                                                           | No major change — already could have concrete methods.                                                                   |
|                                  |                                                                                                                                     |                                                                                                                          |

![[Pasted image 20250823201628.png]]![[Pasted image 20250823201958.png]]



![[Pasted image 20250823202024.png]]




We can have multiple classes with same interface and then have a reference variable of interface to use the classes.

![[Pasted image 20250823202918.png]]

![[Pasted image 20250823202931.png]]


interfaces can have static methods, but we need to implement it as well.


### Nested Interfaces

![[Pasted image 20250823204402.png]]

![[Pasted image 20250823204448.png]]



### Generics

![[Pasted image 20250824064556.png]]

![[Pasted image 20250824064731.png]]


We cannot create instances of T, so we have to use Object class as a workaround to make instances inside the class.
![[Pasted image 20250824070253.png]]


### Wildcards

![[Pasted image 20250824070913.png]]

![[Pasted image 20250824070924.png]]


### Comparable

`Comparable` in Java is an **interface used to define the natural ordering of objects**, meaning it determines how objects of a class should be compared to each other


![[Pasted image 20250824072705.png]]


![[Pasted image 20250824072927.png]]
![[Pasted image 20250824072927.png]]


### Comparator

Helps to keep the sorting logic outside the class, instead of inside the class like Comparable

![[Pasted image 20250824073544.png]]
![[Pasted image 20250824073613.png]]


|Feature|Comparable|Comparator|
|---|---|---|
|Package|`java.lang`|`java.util`|
|Method|`compareTo()`|`compare()`|
|Sorting logic|Inside the class itself|Outside the class|
|Use case|Single natural order|Multiple/custom orders|



### Lambda Functions


*To be done afterwards*

### Exception Handling

In Java, **both exceptions and errors are subclasses of `Throwable`**


Exceptions are of 2 types
- checked - at compile time
- unchecked - only detected while running the program

![[Pasted image 20250824075100.png]]

![[Pasted image 20250824075301.png]]

![[Pasted image 20250824075318.png]]

### Object Cloning

In Java, **object cloning** is the process of creating an _exact copy_ of an existing object

![[Pasted image 20250824082346.png]]


### Shallow and Deep Copy

