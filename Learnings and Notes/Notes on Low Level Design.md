
## Design Patterns



There are 3 types of design patterns
- *Creational* - focus on how objects are created
- *Structural* - focus on how classes and objects are composed
- *Behavioral* - Focus on how objects interact with each other.


| **Category**   | **Pattern**                 | **Intent (What it solves)**                  | **Key Idea (How it works)**                                | **Java Example**                          |
| -------------- | --------------------------- | -------------------------------------------- | ---------------------------------------------------------- | ----------------------------------------- |
| **Creational** | **Singleton**               | Ensure only one instance of a class          | Private constructor + static instance                      | `Runtime.getRuntime()`                    |
|                | **Factory Method**          | Let subclasses decide what object to create  | Superclass defines method, subclass decides implementation | `Calendar.getInstance()`                  |
|                | **Abstract Factory**        | Create families of related objects           | "Factory of factories" producing related objects           | `DocumentBuilderFactory`                  |
|                | **Builder**                 | Construct complex objects step by step       | Chain methods, then `build()`                              | `StringBuilder`, `ProcessBuilder`         |
|                | **Prototype**               | Create objects by cloning                    | Implement `clone()` instead of new                         | `Object.clone()`                          |
| **Structural** | **Adapter**                 | Make incompatible interfaces work together   | Wrapper converts interface                                 | `Arrays.asList()`                         |
|                | **Bridge**                  | Separate abstraction from implementation     | Composition over inheritance                               | JDBC drivers                              |
|                | **Composite**               | Treat part-whole hierarchies uniformly       | Tree structure where nodes/leaves share interface          | `Component` in AWT/Swing                  |
|                | **Decorator**               | Add behavior dynamically                     | Wrap object with same interface                            | `BufferedReader` over `Reader`            |
|                | **Facade**                  | Simplify a complex subsystem                 | One entry-point class hides details                        | `javax.faces.context.FacesContext`        |
|                | **Flyweight**               | Share fine-grained objects to save memory    | Cache immutable state                                      | `Integer.valueOf()`                       |
|                | **Proxy**                   | Control access to object                     | Stand-in object with same interface                        | `java.lang.reflect.Proxy`, RMI stubs      |
| **Behavioral** | **Chain of Responsibility** | Pass request along chain until handled       | Linked handlers decide to process or forward               | Servlet Filters                           |
|                | **Command**                 | Encapsulate a request as an object           | Objectify operations with `execute()`                      | `Runnable`, `ActionListener`              |
|                | **Interpreter**             | Define grammar and interpret expressions     | Class per grammar rule                                     | `Pattern`/`Matcher` regex                 |
|                | **Iterator**                | Access elements sequentially                 | Standard cursor interface                                  | `Iterator`, `ListIterator`                |
|                | **Mediator**                | Centralize complex communications            | One mediator manages interactions                          | GUI dialog controllers                    |
|                | **Memento**                 | Capture/restore object state                 | Store snapshots without exposing details                   | Undo mechanisms                           |
|                | **Observer**                | Notify dependents on state change            | Publish/subscribe model                                    | `PropertyChangeListener`                  |
|                | **State**                   | Change behavior when state changes           | Encapsulate state objects                                  | TCP connection states                     |
|                | **Strategy**                | Select algorithm at runtime                  | Encapsulate algorithms separately                          | `Comparator` in sorting                   |
|                | **Template Method**         | Skeleton of algorithm, subclasses fill steps | Base class defines steps, subclasses override hooks        | `HttpServlet.service()`                   |
|                | **Visitor**                 | Add new operations without modifying objects | Separate operations from data structure                    | `ElementVisitor` in annotation processing |





