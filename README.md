<p align="center">
<img alt="AndroidInterviewQuestions" src="https://raw.githubusercontent.com/MindorksOpenSource/android-interview-questions/master/assets/android_interview_questions.png">
</p>


# Android Interview Questions
[![Mindorks](https://img.shields.io/badge/mindorks-opensource-blue.svg)](https://mindorks.com/open-source-projects)
[![Mindorks Community](https://img.shields.io/badge/join-community-blue.svg)](https://mindorks.com/join-community)
[![Mindorks Android Store](https://img.shields.io/badge/Mindorks%20Android%20Store-Android%20Interview%20Questions-blue.svg?style=flat)](https://mindorks.com/android/store)

> Android Interview Questions - Your Cheat Sheet For Android Interview

## We will be adding answers to the more questions on our [Mindorks website](https://mindorks.com).

## Prepared and maintained by [Amit Shekhar](https://github.com/amitshekhariitbhu) who is having experience of taking interviews of many Android developers and cracking interviews of top companies.

## Contents

* [Data Structures And Algorithms](#data-structures-and-algorithms)

* [Core Java](#core-java)

* [Core Android](#core-android)

* [Architecture](#architecture)

* [Design Problem](#design-problem)

* [Tools And Technologies](#tools-and-technologies)

* [Android Test Driven Development](#android-test-driven-development)

* [Others](#others)


### Data Structures And Algorithms

> The level of questions asked on the topic of Data Structures And Algorithms totally depends on the company for which you are applying.

* Array
    - An Array consists of a group of elements of the same data type. It is stored contiguously in memory and by using its' index, you can find the underlying data. Arrays can be one dimensional and multi-dimensional. One dimensional array is the simplest data structure, and also most commonly used. It is worth noting that in Java language multi-dimensional array are implemented as arrays of arrays. For example, `int[10][5]` is actually one array with its' cells pointing to ten 5-element arrays.    

        | Algorithm | Average | Worst Case |
        |:---------:|:-------:|:----------:|
        | Space     | Θ(n)    | O(n)       |    
        | Search    | Θ(n)    | O(n)       |
        | Insert    | Θ(n)    | O(n)       |
        | Delete    | Θ(n)    | O(n)       |

* LinkedList
    - A LinkedList, just like a tree and unlike an array, consists of a group of nodes which 
    together represent a sequence. Each node contains data and a pointer. The data in a node can be 
    anything, but the pointer is a reference to the next item in the LinkedList. A LinkedList 
    contains both a head and a tail. The "Head" is the first item in the LinkedList, while the "Tail" is 
    the last item. It is not a circular data structure, therefore the tail does not have its' 
    pointer pointing at the Head - the pointer is just `null`. The run time complexity for each of 
    the base methods are as follows:

        | Algorithm | Average | Worst Case |
        |:---------:|:-------:|:----------:|
        | Space     | Θ(n)    | O(n)       |
        | Search    | Θ(n)    | O(n)       |
        | Insert    | Θ(1)    | O(1)       |
        | Delete    | Θ(1)    | O(1)       |

* DoublyLinkedList
   - A DoublyLinkedList is based on a LinkedList, but there is two pointers in each node, "previous" pointer holds reference to the previous node and "next" pointer holds reference to the next node. It also has a Head node, head node's next pointer references the first node in this DoublyLinkedList. The last node's "next" reference points to `null`, but if last node's next pointer points to the first node, such DoublyLinkedList is called "Circular DoublyLinkedList". This data structure is very convenient if you need to be able to traverse stored elements in both directions. 
  
       ![DoublyLinkedList](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Doubly-linked-list.svg/610px-Doubly-linked-list.svg.png)
            
        | Algorithm | Average | Worst Case |
        |:---------:|:-------:|:----------:|
        | Space     | Θ(n)    | O(n)       |
        | Search    | Θ(n)    | O(n)       |
        | Insert    | Θ(1)    | O(1)       |
        | Delete    | Θ(1)    | O(1)       |

* Stack
   - A Stack is a basic data structure with a "Last-in-First-out" (LIFO) semantics. This means that 
    the last item that was added to the stack is the first item that comes out of the stack. A 
    Stack is like a stack of books in that in order to get to the first book that was added in the stack 
    (the bottom book), all of the books that were added after need to be removed first. Adding to a 
    Stack is called "Push", removing from a stack is called "Pop", and getting the last item 
    inserted into the stack without removing it is called "Top". The most common way to implement a
     stack is by using a LinkedList, but there is also StackArray (implemented with an array) 
     which does not replace null entries, and there is also a Vector implementation that does 
     replace `null` entries. [Wikipedia](https://en.wikibooks.org/wiki/Data_Structures/Stacks_and_Queues#Performance_Analysis)
        <table>
            <tr>
                <th>Algorithm</th>
                <th>Average</th>
                <th>Worst Case</th>
                <th>Image representation</th>
            </tr>
            <tr>
                <td>Space</td>
                <td>Θ(n)</td>
                <td>O(n)</td>
                <td rowspan="5">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/29/Data_stack.svg/250px-Data_stack.svg.png"/>
                </td>
            </tr>
            <tr>
                <td>Search</td>
                <td>Θ(n)</td>
                <td>O(n)</td>
            </tr>
            <tr>
                <td>Insert (Push)</td>
                <td>Θ(1)</td>
                <td>O(1)</td>
            </tr>
            <tr>
                <td>Delete (Pop)</td>
                <td>Θ(1)</td>
                <td>O(1)</td>
            </tr>
            <tr>
              <td>Top</td>
              <td>Θ(1)</td>
              <td>O(1)</td>
            </tr>
        </table>

* Queue

* PriorityQueue

* Binary Tree [Wikipedia](https://en.wikipedia.org/wiki/Binary_tree?oldformat=true)

* Binary Search Tree

* Hash Table or Hash Map

* Sorting Algorithms [Wikipedia](https://en.wikipedia.org/wiki/Sorting_algorithm?oldformat=true)
    - Using the most efficient sorting algorithm (and correct data structures that implement it) is vital for any program, because data manipulation can be one of the most significant bottlenecks in case of performance and the main purpose of spending time, determining the best algorithm for the job, is to drastically improve said performance. The efficiency of an algorithm is measured in its' "Big O" ([StackOverflow](https://stackoverflow.com/questions/487258/what-is-a-plain-english-explanation-of-big-o-notation)) score. Really good algorithms perform important actions in O(n log n) or even O(log n) time and some of them can even perform certain actions in O(1) time (HashTable insertion, for example). But there is always a trade-off - if some algorithm is really good at adding a new element to a data structure, it is, most certainly, much worse at data access than some other algorithm. If you are proficient with math, you may notice that "Big O" notation has many similarities with "limits", and you would be right - it measures best, worst and average performances of an algorithm in question, by looking at its' function limit. It should be noted that, when we are speaking about O(1) - constant time - we are not saying that this algorithm performs an action in one operation, rather that it can perform this action with the same number of operations (roughly), regrardless of the amount of elements it has to take into account. Thankfully, a lot of "Big O" scores have been already calculated, so you don't have to guess, which algorithm or data structure will perform better in your project. ["Big O" cheat sheet](http://bigocheatsheet.com/)
    - Bubble sort [Wikipedia](https://en.wikipedia.org/wiki/Bubble_sort?oldformat=true) 
        - Bubble sort is one of the simplest sorting algorithms. It just compares neighbouring elements and if the one that precedes the other is smaller - it changes their places. So over one iteration over the data list, it is guaranteed that **at least** one element will be in its' correct place (the biggest/smallest one - depending on the direction of sorting). This is not a very efficient algorithm, as highly unordered arrays will require a lot of reordering (upto O(n^2)), but one of the advantages of this algorithm is its' space complexity - only two elements are compared at once and there is no need to allocate more memory, than those two will occupy. 
            <table>
                <tr>
                    <th colspan="3" align="center">Time Complexity</th>
                    <th align="center">Space Complexity</th>
                </tr>
                <tr>
                    <th align="center">Best</th>
                    <th align="center">Average</th>
                    <th align="center">Worst</th>
                    <th align="center">Worst</th>
                </tr>
                <tr>
                    <td align="center">Ω(n)</td>
                    <td align="center">Θ(n^2)</td>
                    <td align="center">O(n^2)</td>
                    <td align="center">O(1)</td>
                </tr>
            </table>
    - Selection sort [Wikipedia](https://www.wikiwand.com/en/Selection_sort) 
        - Firstly, selection sort assumes that the first element of the array to be sorted is the smallest, but to confirm this, it iterates over all other elements to check, and if it finds one, it gets defined as the smallest one. When the data ends, the element, that is currently found to be the smallest, is put in the beginning of the array. This sorting algorithm is quite straightforward, but still not that efficient on larger data sets, because to assign just one element to its' place, it needs to go over all data.
            <table>
            <tr>
                <th colspan="3" align="center">Time Complexity</th>
                <th align="center">Space Complexity</th>
            </tr>
            <tr>
                <th align="center">Best</th>
                <th align="center">Average</th>
                <th align="center">Worst</th>
                <th align="center">Worst</th>
            </tr>
            <tr>
                <td align="center">Ω(n^2)</td>
                <td align="center">Θ(n^2)</td>
                <td align="center">O(n^2)</td>
                <td align="center">O(1)</td>
            </tr>
            </table>
    - Insertion sort [Wikipedia](https://en.wikipedia.org/wiki/Insertion_sort?oldformat=true)
        - Insertion sort is another example of an algorithm, that is not that difficult to implement, but is also not that efficient. To do its' job, it "grows" sorted portion of data, by "inserting" new encountered elements into already (innerly) sorted part of the array, which consists of previously encountered elements. This means that in best case (data is already sorted) it can confirm that its' job is done in Ω(n) operations, while, if all encountered elements are not in their required order as many as O(n^2) operations may be needed.
            <table>
            <tr>
                <th colspan="3" align="center">Time Complexity</th>
                <th align="center">Space Complexity</th>
            </tr>
            <tr>
                <th align="center">Best</th>
                <th align="center">Average</th>
                <th align="center">Worst</th>
                <th align="center">Worst</th>
            </tr>
            <tr>
                <td align="center">Ω(n)</td>
                <td align="center">Θ(n^2)</td>
                <td align="center">O(n^2)</td>
                <td align="center">O(1)</td>
            </tr>
            </table>
    - Merge sort [Wikipedia](https://en.wikipedia.org/wiki/Merge_sort?oldformat=true)
        - This is a "divide and conquer" algorithm, meaning it recursively "divides" given array in to smaller parts (up to 1 element) and then sorts those parts, combining them with each other. This approach allows merge sort to achieve very high speed, while  doubling required space, of course, but today memory space is more available than it was a couple of years ago, so this trade-off is considered acceptable.   
                <table>
            <tr>
                <th colspan="3" align="center">Time Complexity</th>
                <th align="center">Space Complexity</th>
            </tr>
            <tr>
                <th align="center">Best</th>
                <th align="center">Average</th>
                <th align="center">Worst</th>
                <th align="center">Worst</th>
            </tr>
            <tr>
                <td align="center">Ω(n log(n))</td>
                <td align="center">Θ(n log(n))</td>
                <td align="center">O(n log(n))</td>
                <td align="center">O(n)</td>
            </tr>
            </table>
    - Quicksort [Wikipedia](https://en.wikipedia.org/wiki/Quicksort?oldformat=true)
        - Quicksort is considered, well, quite quick. When implemented correctly, it can be a significant number of times faster than its' main competitors. This algorithm is also of "divide and conquer" family and its' first step is to choose a "pivot" element (choosing it randomly, statistically, minimizes the chance to get the worst performance), then by comparing elements to this pivot, moving it closer and closer to its' final place. During this process, the elements that are bigger are moved to the right side of it and smaller elements to the left. After this is done, quicksort repeats this process for subarrays on each side of placed pivot (does first step recursively), until the array is sorted.
                <table>
                <tr>
                    <th colspan="3" align="center">Time Complexity</th>
                    <th align="center">Space Complexity</th>
                </tr>
                <tr>
                    <th align="center">Best</th>
                    <th align="center">Average</th>
                    <th align="center">Worst</th>
                    <th align="center">Worst</th>
                </tr>
                <tr>
                    <td align="center">Ω(n log(n))</td>
                    <td align="center">Θ(n log(n))</td>
                    <td align="center">O(n^2)</td>
                    <td align="center">O(1)</td>
                </tr>
                </table>  
    - There are, of course, more sorting algorithms and their modifications. We strongly recommend all readers to familiarize themselves with a couple more, because knowing algorithms is very important quality of a candidate, applying for a job and it shows understanding of what is happening "under the hood".

* Dynamic Programming

* Greedy Algorithm

* String Manipulation

* Pathfinding algorithms [Wikipedia](https://en.wikipedia.org/wiki/Greedy_algorithm?oldformat=true)
    - Dijkstra algorithm
    - A* algorithm
    - Breadth First Search
    - Depth First Search

### Core Java

#### OOP

* Explain OOP Concepts.
    - Object-Oriented Programming is a methodology of designing a program using classes, objects, 
    [inheritance](https://en.wikipedia.org/wiki/Inheritance_(object-oriented_programming)),
    [polymorphism](https://en.wikipedia.org/wiki/Polymorphism_(computer_science)),
    [abstraction](https://en.wikipedia.org/wiki/Abstraction_(software_engineering)), and
    [encapsulation](https://en.wikipedia.org/wiki/Encapsulation_(computer_programming)).

* Differences between abstract classes and interfaces? [GitHub](https://arjun-sna.github.io/java/2017/02/02/abstractvsinterface/)
    - An abstract class, is a class that contains both concrete and abstract methods 
    (methods without implementations). An abstract method must be implemented by the abstract class
     sub-classes. Abstract classes cannot be instantiated and need to be extended to be used.
    - An interface is like a blueprint/contract of a class (or it may be thought of as a class with methods, but without their implementation). It contains empty methods that 
    represent, what all of its subclasses should have in common. The subclasses provide the 
    implementation for each of these methods. Interfaces are implemented.

* What is the difference between iterator and enumeration in java?

* Do you agree we use composition over inheritance? [Composition vs Inheritance](https://www.journaldev.com/12086/composition-vs-inheritance)

* Difference between method overloading and overriding.
        <p align="center">
        <img alt="Overloading and Overriding" src="https://github.com/codeshef/android-interview-questions/blob/master/assets/overloading-vs-overriding.png">
        </p>
    - Overloading happens at compile-time while Overriding happens at runtime: The binding of overloaded method call to its definition has happens at compile-time however binding of overridden method call to its definition happens at runtime.
    More info on static vs. dynamic binding: [StackOverflow](https://stackoverflow.com/questions/19017258/static-vs-dynamic-binding-in-java).
    - Static methods can be overloaded which means a class can have more than one static method of same name. Static methods cannot be overridden, even if you declare a same static method in child class it has nothing to do with the same method of parent class as overridden static methods are chosen by the reference class and not by the class of the object.

        So, for example:
        ```java
        public class Animal {
            public static void testClassMethod() {
                System.out.println("The static method in Animal");
            }

            public void testInstanceMethod() {
                System.out.println("The instance method in Animal");
            }
        }

        public class Cat extends Animal {
            public static void testClassMethod() {
                System.out.println("The static method in Cat");
            }

            public void testInstanceMethod() {
                System.out.println("The instance method in Cat");
            }

            public static void main(String[] args) {
                Cat myCat = new Cat();
                myCat.testClassMethod();
                Animal myAnimal = myCat;
                myAnimal.testClassMethod();
                myAnimal.testInstanceMethod();
            }
        }
        ```
        Will output:
        ```java
        The static method in Cat    // testClassMethod() is called from "Cat" reference

        The static method in Animal // testClassMethod() is called from "Animal" reference,
                                    // ignoring actual object inside it (Cat)

        The instance method in Cat  // testInstanceMethod() is called from "Animal" reference,
                                    // but from "Cat" object underneath
        ```

        The most basic difference is that overloading is being done in the same class while for overriding base and child classes are required. Overriding is all about giving a specific implementation to the inherited method of parent class.

        Static binding is being used for overloaded methods and dynamic binding is being used for overridden/overriding methods.
        Performance: Overloading gives better performance compared to overriding. The reason is that the binding of overridden methods is being done at runtime.

        Private and final methods can be overloaded but they cannot be overridden. It means a class can have more than one private/final methods of same name but a child class cannot override the private/final methods of their base class.

        Return type of method does not matter in case of method overloading, it can be same or different. However in case of method overriding the overriding method can have more specific return type (meaning if, for example, base method returns an instance of Number class, all overriding methods can return any class that is extended from Number, but not a class that is higher in the hierarchy, like, for example, Object is in this particular case).

        Argument list should be different while doing method overloading. Argument list should be same in method Overriding.
It is also a good practice to annotate overridden methods with `@Override` to make the compiler be able to notify you if child is, indeed, overriding parent's class method during compile-time.

* What are the access modifiers you know? What does each one do? <br>
   - There are four access modifiers in Java language (from strictest to the most lenient):
        1. `private` *variables*, *methods*, *constructors* or *inner classes* are only visible to its' containing class and its' methods. This modifier is most commonly used, for example, to allow variable access only through getters and setters or to hide underlying implementation of classes that should not be used by user and therefore maintain encapsulation. Singleton constructor is also marked `private` to avoid unwanted instantiation from outside.
        2. `protected` can be used on *variables*, *methods* and *constructors* therefore allowing access only to subclasses and classes that are inside the same package as protected members' class.
        3. Default (no keyword is used) this modifier can be applied to *classes*, *variables*, *constructors* and *methods* and allows access from classes and methods inside the same package.
        4. `public` modifier is widely-used on *classes*, *variables*, *constructors* and *methods* to grant access from any class and method anywhere. It should not be used everywhere as it implies that data marked with `public` is not sensitive and can not be used to harm the program.

* Can an Interface implement another Interface?
  - Yes, an interface can implement another interface (and more than one), but it needs to use `extends`, rather than `implements` keyword. And while you can not remove methods from parent interface, you can add new ones freely to your subinterface.

* What is Polymorphism? What about Inheritance?
  - Polymorphism in Java has two types: Compile time polymorphism (static binding) and Runtime polymorphism (dynamic binding). Method overloading is an example of static polymorphism, while method overriding is an example of dynamic polymorphism.

	An important example of polymorphism is how a parent class refers to a child class object.  In fact, any object that satisfies more than one IS-A relationship is polymorphic in nature.

	For instance, let’s consider a class `Animal` and let `Cat` be a subclass of `Animal`. So, any cat IS animal. Here, Cat satisfies the IS-A relationship for its own type as well as its super class Animal.
  - Inheritance can be defined as the process where one class acquires the properties (methods and fields) of another. With the use of inheritance the information is made manageable in a hierarchical order.

	The class which inherits the properties of other is known as subclass (derived class, child class) and the class whose properties are inherited is known as superclass (base class, parent class).

	Inheritance uses the keyword `extends` to inherit the properties of a class. Following is the syntax of extends keyword.
	```java
	class Super {
	   .....
	   .....
	}
	class Sub extends Super {
	   .....
	   .....
	}
	```

* Multiple inheritance in Classes and Interfaces in java [Blog](http://codeinventions.blogspot.in/2014/07/can-interface-extend-multiple.html)

* What are the design patterns? [GitHub](https://github.com/iluwatar/java-design-patterns)
    - Creational patterns
        - Builder [Wikipedia](https://en.wikipedia.org/wiki/Builder_pattern?oldformat=true)

        - Factory [Wikipedia](https://en.wikipedia.org/wiki/Factory_method_pattern?oldformat=true)

        - Singleton [Wikipedia](https://en.wikipedia.org/wiki/Singleton_pattern)
          A singleton is a class that can only be instantiated once. This singleton pattern restricts the instantiation of a class to one object. This is useful when exactly one object is needed to coordinate actions across the system. The concept is sometimes generalized to systems that operate more efficiently when only one object exists, or that restrict the instantiation to a certain number of objects.

    - Structural patterns
        - Adapter [Wikipedia](https://en.wikipedia.org/wiki/Adapter_pattern?oldformat=true)
        - Decorator [Wikipedia](https://en.wikipedia.org/wiki/Decorator_pattern?oldformat=true)
        - Facade [Wikipedia](https://en.wikipedia.org/wiki/Facade_pattern?oldformat=true)
    - Behavioural patterns
        - Chain of responsibility [Wikipedia](https://en.wikipedia.org/wiki/Chain-of-responsibility_pattern?oldformat=true)
        - Iterator [Wikipedia](https://en.wikipedia.org/wiki/Iterator_pattern?oldformat=true)
        - Strategy [Wikipedia](https://en.wikipedia.org/wiki/Strategy_pattern?oldformat=true)

#### Collections and Generics

* `Arrays` vs `ArrayLists`.

* `HashSet` vs `TreeSet`.

* Explain Generics in Java?
    - Generics were included in Java language to provide stronger type checks, by allowing the programmer to define, which classes can be used with other classes
        > In a nutshell, generics enable types (classes and interfaces) to be parameters when defining classes, interfaces and methods. Much like the more familiar formal parameters used in method declarations, type parameters provide a way for you to re-use the same code with different inputs. The difference is that the inputs to formal parameters are values, while the inputs to type parameters are types. ([Official Java Documentation](https://docs.oracle.com/javase/tutorial/java/generics/why.html))

    - This means that, for example, you can define:
        ```java
        List<Integer> list = new ArrayList<>();
        ```
        And let the compiler take care of noticing, if you put some object, of type other than `Integer` into this list and warn you.
    - It should be noted that standard class hierarchy *does not* apply to generic types. It means that `Integer` in `List<Integer>` is not inherited from `<Number>` - it is actually inherited directly from `<Object>`. You can still put some constraints on what classes can be passed as a parameter into a generic by using [wildcards](https://docs.oracle.com/javase/tutorial/extra/generics/wildcards.html) like `<?>`, `<? extends MyCustomClass>` or `<? super Number>`.
    - While generics are very useful, late inclusion into Java language has put some restraints on their implementation - backward compatibility required them to remain just "syntactic sugar" - they are erased ([type erasure](https://docs.oracle.com/javase/tutorial/java/generics/erasure.html)) during compile-time and replaced with `object` class.

* What is Java `PriorityQueue`?

#### Objects and Primitives

#### String

* How is `String` class implemented? Why was it made immutable?
  - There is no primitive variant of `String` class in Java language - all strings are just wrappers around underlying array of characters, which is declared `final`. This means that, once a `String` object is instantiated, it cannot be changed through normal tools of the language (Reflection still can mess things up horribly, because in Java no object is truly immutable). This is why `String` variables in classes are the first candidates to be used, when you want to override `hashCode()` and `equals()` of your class - you can be sure, that all their required contracts will be satisfied.
    > Note: The String class is immutable, so that once it is created a String object cannot be changed. The String class  has a number of methods, some of which will be discussed below, that appear to modify strings. Since strings are  immutable, what these methods really do is create and return a new string that contains the result of the operation. ([Official Java Documentation](https://docs.oracle.com/javase/tutorial/java/data/strings.html))

    This class is also unique in a sense, that, when you create an instance like this:
    ```java
    String helloWorld = "Hello, World!";
    ```
    `"Hello, World!"` is called a *literal* and compiler creates a `String` object with its' value. So
    ```java
    String capital = "Hello, World!".toUpperCase();
    ```
    is a valid statement, that, firstly, will create an object with literal value "Hello, World!" and then will create and return another object with value "HELLO, WORLD!"
  - `String` was made immutable to prevent malicious manipulation of data, when, for example, user login or other sensitive data is being send to a server.

* What does it means to say that a `String` is immutable?
    - It means that once created, `String` object's `char[]` (its' containing value) is declared `final` and, therefore, it can not be changed during runtime.

* What is `String.intern()`? When and why should it be used?

* Can you list 8 primitive types in java?

* What is the difference between an Integer and int?
  - `int` is a primitive data type (with `boolean`, `byte`, `char`, `short`, `long`, `float` and `double`), while `Integer` (with `Boolean`, `Byte`, `Character`, `Short`,`Long`, `Float` and `Double`) is a [wrapper](https://docs.oracle.com/javase/tutorial/java/data/numberclasses.html) class that encapsulates primitive data type, while providing useful methods to perform different tasks with it.

* What is Autoboxing and Unboxing?
  - Autoboxing and Unboxing is the process of automatic wrapping (putting in a box) and unwrapping (getting the value out) of primitive data types, that have "wrapper" classes. So `int` and `Integer` can (almost always) be used interchangeably in Java language, meaning a method `void giveMeInt(int i) { ... }` can take `int` as well as `Integer` as a parameter.

* Typecast in Java.
    - In Java, you can use casts to polymorph one class into another, compatible one. For example:
        ```java
            long i = 10l;
            int j = (int) i;
            long k = j;
        ```
        Here we see, that, while narrowing (`long i` -> `int j`) requires an explicit cast to make sure the programmer realizes, that there may be some data or precision loss, widening (`int j` -> `long k`) does not require an explicit cast, because there can be no data loss (`long` can take larger numbers than `int` allows).

* Do objects get passed by reference or value in Java? Elaborate on that.
    - In Java all primitives and objects are passed by value, meaning that their copy will be manipulated in the receiving method. But there is a caveat - when you pass an object reference into a method, a *copy of this reference* is made, so it still points to the same object. This means, that any changes that you make to the insides of this object are retained, when the method exits.
        ```java
        public class Pointer {

            int innerField;

            public Pointer(int a) {
                this.innerField = a;
            }
        }
        ```
        ```java
            public class ValueAndReference {

            public static void main(String[] args) {

                Pointer a = new Pointer(0);
                int b = 1;

                print("Before:");
                print("b = " + b);
                print("a.innerField = " + a.innerField);
                exampleMethod(a, b);
                print("After:");
                print("b = " + b);
                print("a.innerField = " + a.innerField);
            }

            static void exampleMethod(Pointer a, int b) {
                a.innerField = 2;
                b = 10;
            }

            static void print(String text) {
                System.out.println(text);
            }
        }
        ```
        Will output:
        ```java
            Before:

            b = 1

            a.innerField = 0

            After:

            b = 1        // a new local int variable was created and operated on, so "b" didn't change

            a.innerField = 2 // Pointer a got its' innerField variable changed
                             //  from 0 to 2, because method was operating on
                             //  the same reference to an instance
        ```

* What is the difference between instantiation and initialization of an object?
    - Initialization is the process of the memory allocation, when a new variable is created. Variables should be explicitly given a value, otherwise they may contain a random value that remained from the previous variable that was using the same memory space. To avoid this problem, Java language assigns default (right after initialization) values to some data types:
        * `boolean` defaults to `false`;
        * `byte` defaults to `0`;
        * `short` defaults to `0`;
        * `int` defaults to `0`;
        * `long` defaults to `0L`;
        * `char` defaults to `\u0000`;
        * `float` defaults to `0.0f`;
        * `double` defaults to `0.0d`;
        * `object` defaults to `null`.
    - Instantiation is the process of explicitly assigning definitive value to a declared variable:
        ```java
            int j;  // Initialized variable (int defaults to 0 right after)
            j = 10; // Instantiated variable
        ```

* What the difference between local, instance and class variables?
  - Local variables exist only in methods that created them, they are stored separately in their respected Thread Stack (for more information, see question about Java Memory Model) and cannot have their reference passed outside of the method scope. That also means that they cannot be assigned any access modifier or made `static` - because they only exist during enclosing method's execution and those modifiers just do not make sense, since no other outside method can get them anyway.
  - Instance variables are the ones, that are declared in classes and their value can be different from one instance of the class to another, but they always require that class' instance to exist.
  - Class variables are those, that are marked with `static` keyword in their class' body. They can only have one value across all instances of that class (changing it in one place will change it in their class and, therefore, in all instances) and can even be retrieved without that class' instance (if their access modifier allows it).

#### Java Memory Model and Garbage Collector

* What is garbage collector? How does it work?
  - All objects are allocated on the heap area managed by the JVM.
  As long as an object is being referenced, the JVM considers it alive.
  Once an object is no longer referenced and therefore is not reachable by the application code,
  the garbage collector removes it and reclaims the unused memory.

* What is Java Memory Model? What contracts does it guarantee? How are its' Heap and Stack organized? [Jenkov](http://tutorials.jenkov.com/java-concurrency/java-memory-model.html)

* What is memory leak and how does Java handle it?

* What are strong, soft, weak and phantom references in Java?

#### Concurrency

* What does the keyword `synchronized` mean? [Link](https://stackoverflow.com/a/1085745/2621950)

* What is a `ThreadPoolExecutor`? [Mindorks](https://blog.mindorks.com/threadpoolexecutor-in-android-8e9d22330ee3)

* What is `volatile` modifier? [Jenkov](http://tutorials.jenkov.com/java-concurrency/volatile.html)

#### Exceptions

* How does the `try{} catch{} finally{}` works? [Link](http://tutorials.jenkov.com/java-exception-handling/basic-try-catch-finally.html)

#### Others

* What is serialization? How do you implement it?
    - Serialization is the process of converting an object into a stream of bytes in order to store
    an object into memory, so that it can be recreated at a later time, while still keeping the
    object's original state and data. In Android you may use either the Serializable, Externalizable (implements Serializable) or Parcelable interfaces.
    - While Serializable is the easiest to implement, Externalizable may be used if you need to insert custom logic into the process of serialization (although it is almost never used nowadays as it is considered a relic from early versions of Java). But it is highly recommended to use Parcelable in Android instead, as Parcelable was created exclusively for Android and it performs about 10x faster than Serializable, because Serializable uses reflection, which is a slow process and tends to create a lot of temporary objects and it may cause garbage collection to occur more often.
    - To use Serializable all you have to do is implement the interface:

        ```java
        /**
        *  Implementing the Serializeable interface is all that is required
        */
        public class User implements Serializable {

            private String name;
            private String email;

                public User() {
                }

                public String getName() {
                    return name;
                }

                public void setName(final String name) {
                    this.name = name;
                }

                public String getEmail() {
                    return email;
                }

                public void setEmail(final String email) {
                    this.email = email;
                }
            }
        ```
    - Parcelable requires a bit more work:
        ```java
            public class User implements Parcelable {

                private String name;
                private String email;

                /**
                 * Interface that must be implemented and provided as a public CREATOR field
                 * that generates instances of your Parcelable class from a Parcel.
                 */
                public static final Creator<User> CREATOR = new Creator<User>() {

                    /**
                     * Creates a new USer object from the Parcel. This is the reason why
                     * the constructor that takes a Parcel is needed.
                     */
                    @Override
                    public User createFromParcel(Parcel in) {
                        return new User(in);
                    }

                    /**
                     * Create a new array of the Parcelable class.
                     * @return an array of the Parcelable class,
                     * with every entry initialized to null.
                     */
                    @Override
                    public User[] newArray(int size) {
                        return new User[size];
                    }
                };

                public User() {
                }

                /**
                 * Parcel overloaded constructor required for
                 * Parcelable implementation used in the CREATOR
                 */
                private User(Parcel in) {
                    name = in.readString();
                    email = in.readString();
                }

                public String getName() {
                    return name;
                }

                public void setName(final String name) {
                    this.name = name;
                }

                public String getEmail() {
                    return email;
                }

                public void setEmail(final String email) {
                    this.email = email;
                }

                @Override
                public int describeContents() {
                    return 0;
                }

                /**
                 * This is where the parcel is performed.
                 */
                @Override
                public void writeToParcel(final Parcel parcel, final int i) {
                    parcel.writeString(name);
                    parcel.writeString(email);
                }
            }
        ```
        Note: For a full explanation of the <b>describeContents()</b> method see [StackOverflow](https://stackoverflow.com/questions/4076946/parcelable-where-when-is-describecontents-used/4914799#4914799).
        In Android Studio, you can have all of the parcelable code auto generated for you, but like with everything else, it is always a good thing to try and understand everything that is happening.

* What is `transient` modifier? [JavaTPoint](https://www.javatpoint.com/transient-keyword) `transient` is a Java keyword which marks a member variable not to be serialized when it is persisted to streams of bytes. When an object is transferred through the network, the object needs to be 'serialized'. Serialization converts the object state to serial bytes.

* What are anonymous classes?[OracleDoc](https://docs.oracle.com/javase/tutorial/java/javaOO/anonymousclasses.html) It is an inner class without a name and for which only a single object is created. An anonymous inner class can be useful when making an instance of an object with certain “extras” such as overloading methods of a class or interface, without having to actually subclass a class.

* What is the difference between using `==` and `.equals` on an object?[GeeksForGeeks](http://www.geeksforgeeks.org/difference-equals-method-java/) Main difference between .equals() method and == operator is that one is method and other is operator. We can use == operators for reference comparison (address comparison) and .equals() method for content comparison. In simple words, == checks if both objects point to the same memory location whereas .equals() evaluates to the comparison of values in the objects. If a class does not override the equals method, then by default it uses equals(Object o) method of the closest parent class that has overridden this method.

* What is the `hashCode()` and `equals()` used for? In java equals() method is used to compare equality of two Objects. The equality can be compared in two ways:

  - Shallow comparison: The default implementation of equals method is defined in Java.lang.Object class which simply checks if two Object references (say x and y) refer to the same Object. i.e. It checks if x == y. Since Object class has no data members that define its state, it is also known as shallow comparison.
  - Deep Comparison: Suppose a class provides its own implementation of equals() method in order to compare the Objects of that class w.r.t state of the Objects. That means data members (i.e. fields) of Objects are to be compared with one another. Such Comparison based on data members is known as deep comparison.

* Why would you not call abstract method in constructor? Constructors must not invoke overridable methods, directly or indirectly. If you violate this rule, program failure will result. The superclass constructor runs before the subclass constructor, so the overriding method in the subclass will be invoked before the subclass constructor has run. If the overriding method depends on any initialization performed by the subclass constructor, the method will not behave as expected.

* What are anonymous classes?[OracleDoc](https://docs.oracle.com/javase/tutorial/java/javaOO/anonymousclasses.html)

* Can you list 8 primitive types in java?

* When would you make an object value `final`? 

* What are these `final`, `finally` and `finalize` keywords?
  - `final` is a keyword in the java language. It is used to apply restrictions on class, method and variable. Final class can't be inherited, final method can't be overridden and final variable value can't be changed.
	```java
	class FinalExample {
		public static void main(String[] args) {
			final int x=100;
			x=200;//Compile Time Error because x is final
		}
	}
	```
  - `finally` is a code block and is used to place important code, it will be executed whether exception is handled or not.
	```java
	class FinallyExample {
		public static void main(String[] args) {
			try {
				int x=300;
			}catch(Exception e) {
				System.out.println(e);
			}
			finally {
				System.out.println("finally block is executed");
			}
		}
	}
	```
  - `Finalize` is a method used to perform clean up processing just before object is garbage collected.
	```java
	class FinalizeExample {
		public void finalize() {
			System.out.println("finalize called");
		}

		public static void main(String[] args) {
			FinalizeExample f1=new FinalizeExample();
			FinalizeExample f2=new FinalizeExample();
			f1=null;
			f2=null;
			System.gc();
		}
	}
	```


* What does the `static` word mean in Java?
    - In case of `static` variable it means that this variable (its' value or the object it references) spans across all instances of enclosing class (changing it in one instance affects all others), while in case of `static` methods it means that these methods can be invoked without an instance of their enclosing class. It is useful, for example, when you create util classes that need not be instantiated every time you want to use them.

* Can a `static` method be overridden in Java?
  - While child class can override a static method with another static method with the same signature (return type can be downcasted), it is not truly overridden - it becomes "hidden", but both methods can still be accessed under right circumstances (see question about overloading/overriding above).

* When is a `static` block run?
    - Code inside static block is executed only once: the first time you make an object of that class or the first time you access a static member of that class (even if you never make an object of that class).

* What is reflection? [Jenkov](http://tutorials.jenkov.com/java-reflection/index.html) 
    - Java Reflection makes it possible to inspect classes, interfaces, fields and methods at runtime, without knowing the names of the classes, methods etc. at compile time. It is also possible to instantiate new objects, invoke methods and get/set field values using reflection.

    - Java Reflection is quite powerful and can be very useful. For instance, Java Reflection can be used to map properties in JSON files to getter / setter methods in Java objects, like Jackson, GSON, Boon etc. does. Or, Reflection can be used to map the column names of a JDBC ResultSet to getter / setter methods in a Java object.

* What is Dependency Injection?  Can you name few libraries? Have you used any?
  - Dependency injection is a very powerful technique, where you relay the task of providing object with its' dependencies on instances of other objects (OOP Composition, [Wikipedia](https://en.wikipedia.org/wiki/Object_composition?oldformat=true)) to a separate class. This allows for fewer constructors, setters, factories and builders as all those functions are taken care of by the DI framework that you use. Also, and it may seem as a minor advantage, but if you use DI framework you need not worry about going through the project and changing all of (example names) `YourCustomInterface customInterfaceObject = new YourCustomClass();` to a new implementaion, as long as your new class (in place of `YourCustomClass`) still implements `CustomInterface` - you can just tweak the DI factory class to produce new class and voila - this new class will be automatically instantiated throughout your code. This allows for better maintenence and control over the program. Another example of DI usage is unit-testing - it allows to conveniently inject all needed dependencies and keep the amount of written code at a lower level.
    - One of the most popular libraries for DI for Android is Dagger 2. [Mindorks](https://blog.mindorks.com/a-complete-guide-to-learn-dagger-2-b4c7a570d99c)

* How is a `StringBuilder` implemented to avoid the immutable string allocation problem?

* Difference between `StringBuffer` and `StringBuilder`? [Link](http://www.journaldev.com/137/stringbuffer-vs-stringbuilder)
    1. StringBuffer is the thread safe utility class to perform several operations on Strings. It contains append() and insert() methods that are widely used to perform operation on Strings in a multi-thread environment. If you will check the source code, most of its functions are synchronized for thread safety. Since most of the String operations, for example concatenation happens in a single thread environment, Java 1.5 introduced another utility class StringBuilder to perform similar operations but doesn’t provide thread safety. If you will look into its source code, all the methods are unsynchronized. This is the most important point for StringBuffer vs StringBuilder.
    2. StringBuffer has some extra methods such as substring, length, capacity, trimToSize etc. However these are not required since you have all these present in String too. That’s why these methods were never implemented in StringBuilder class.
	3. StringBuffer was introduced in Java 1.0 whereas StringBuilder class was introduced in Java 1.5 after looking at shortcomings of StringBuffer
    4. StringBuilder is faster than StringBuffer because of no synchronization.

* What’s the difference between an `Enumeration` and an `Iterator`? [Link](http://javaconceptoftheday.com/differences-between-enumeration-vs-iterator-in-java/)
	- Enumeration and Iterator are two interfaces in java.util package which are used to traverse over the elements of a Collection object. Though they perform the same function i.e traversing the Collection object, there are some differences exist between them. Using Enumeration, you can only traverse the Collection object. But using Iterator, you can also remove an element while traversing the Collection. This is the one major difference between Enumeration and Iterator in java. You can say Iterator is some what advanced version of Enumeration. In this post, we will see the differences between Enumeration Vs Iterator In Java.

* What is the difference between fail-fast and fail-safe iterators in Java?
	- Typically, weak consistency (fail-safe) means that if a collection is modified concurrently with an iteration, the guarantees of what the iteration sees are weaker. 
	- "Fail fast" means: it may fail ... and the failure condition is checked aggressively so that the failure condition is (where possible1) detected before damage can be done. In Java, a fail-fast iterator fails by throwing a `ConcurrentModificationException`.

* What is Java NIO? [Link](http://tutorials.jenkov.com/java-nio/index.html)

### Core Android

#### Base

* Tell all the Android application components. [Android Official](https://developer.android.com/guide/components/fundamentals.html#Components) 
	- App components are the essential building blocks of an Android app. Each component is an entry point through which the system or a user can enter your app. Some components depend on others. There are four different types of app components:
		- Activities
		- Services
		- Broadcast receivers
		- Content providers
	- Each type serves a distinct purpose and has a distinct lifecycle that defines how the component is created and destroyed. The following sections describe the four types of app components.

* What is the structure of an Android Application?
<table class="tablecontent"><tbody><tr><th>Folder Name</th><th>Description</th></tr><tr><td>src</td><td>The 'src' stands for <b>Source Code.</b> It contains the Java Source files.</td></tr><tr><td>gen</td><td>The 'gen' stands for <b>Generated Java Library.</b> This library is for Android internal use only.</td></tr><tr><td>Android 2.2</td><td>The Android Framework Library is stored here.</td></tr><tr><td>assets</td><td>It is used to store raw asset files.</td></tr><tr><td>libs</td><td>It contains private libraries.</td></tr><tr><td>res</td><td>The 'res' stands for <b>Resource file.</b> It can store resource files such as pictures, XML files, etc. It contains some additional folders such as Drawable, Layout and Values.<br><br><b>anim: </b>It is used for XML files that are compiled into animation objects.<br><b>color:</b> It is used for XML files that describe colors.<br><b>drawable:</b> It is used to store various graphics files. In Android project structure,<br><br><b>there are three types of drawable folders,</b><br>1. drawable-mdpi<br>2. drawable-hdpi<br>3. drawable-ldpi<br><br>The above drawable folders are required in order to adapt to different screen resolutions.<br><br><b>layout:</b> It is used for placing the XML layout files, which defines how various Android objects such as textbox, buttons, etc. are organized on the screen.<br><br><b>menu:</b> It is used for defining the XML files in the application menu.<br><br><b>raw:</b> The 'raw' stands for <b>Raw Asset Files.</b> These files are referenced from the application using a resource identifier in the R class.<br><b>For example,</b> good place for media is MP3 or Ogg files.<br><br><b>values:</b> It is used for XML files which stores various string values, such as titles, labels, etc.<br><br><b>xml:</b> It is used for configuring the application components.</td></tr><tr><td>AndroidManifest.xml</td><td>This file indicates the Android definition file. This file contains the information about the Android application such as minimum Android version, permission to access Android device capabilities such as Internet access permission, phone permission etc.</td></tr><tr><td>default.properties</td><td>This file contains the project settings, such as build the target. Do not edit this file manually. It should be maintained in a Source Revision Control System.</td></tr><tr><td>Proguard.cfg</td><td>This file defines how ProGuard optimizes and makes your code unclear.</td></tr><tr><td>MainLayout.xml</td><td>This file describes the layout of the page. So all the components such as textboxes, labels, radio buttons, etc. are displaying on the application screen.</td></tr><tr><td>Activity class</td><td>The application occupies the entire device screen which needs at least one class inherits from the Activity class. OnCreate() method initiates the application and loads the layout page.</td></tr></tbody></table>

* What is `Context`? How is it used? [Medium](https://medium.com/p/understanding-context-in-android-application-330913e32514)
	- It's the context of current state of the application/object. It lets newly-created objects understand what has been going on. Typically you call it to get information regarding another part of your program (activity and package/application). You can get the context by invoking getApplicationContext(), getContext(), getBaseContext() or this (when in a class that extends from Context, such as the Application, Activity, Service and IntentService classes).

* What is `AndroidManifest.xml`?
	- Every application must have an AndroidManifest.xml file (with precisely that name) in its root directory. The manifest presents essential information about the application to the Android system, information the system must have before it can run any of the application's code.

* What is `Application` class?
	- The Application class in Android is the base class within an Android app that contains all other components such as activities and services. The Application class, or any subclass of the Application class, is instantiated before any other class when the process for your application/package is created.

#### Activity

* What is `Activity`? 
	- An activity represents a single screen with a user interface just like window or frame of Java.Android activity is the subclass of ContextThemeWrapper class. 

* Explain `Activity` and `Fragment` lifecycle. (Complete diagram [GitHub](https://github.com/xxv/android-lifecycle), simplified diagram for [Activity](https://developer.android.com/guide/components/activities/activity-lifecycle.html#alc), [Fragment](https://developer.android.com/guide/components/fragments.html#Lifecycle))

![ActivityFragmentLifeCycle](https://i.stack.imgur.com/1llRw.png)

* What are "launch modes"? [Mindorks](https://blog.mindorks.com/android-activity-launchmode-explained-cbc6cf996802)
	- There are four launch modes for activity. They are:
		1. standard. This is the default launch mode of an activity (If not specified). It creates a new instance of an activity in the task from which it was started. Multiple instances of the activity can be created and multiple instances can be added to the same or different tasks. In other words you can create the same activity multiple times in the same task as well as in different tasks.
		2. singleTop. In this launch mode if an instance of activity already exists at the top of the current task, a new instance will not be created and Android system will route the intent information through onNewIntent(). If an instance is not present on top of task then new instance will be created. Using this launch mode you can create multiple instance of the same activity in the same task or in different tasks only if the same instance does not already exist at the top of stack.
		3. singleTask. In this launch mode a new task will always be created and a new instance will be pushed to the task as the root one. If an instance of activity exists on the separate task, a new instance will not be created and Android system routes the intent information through onNewIntent() method. At a time only one instance of activity will exist.
		4. singleInstance. This is very special launch mode and only used in the applications that has only one activity. It is similar to singleTask except that no other activities will be created in the same task. Any other activity started from here will create in a new task.

#### Fragments

* What is `Fragment`?
	- A Fragment represents a behavior or a portion of user interface in a FragmentActivity. You can combine multiple fragments in a single activity to build a multi-pane UI and reuse a fragment in multiple activities. You can think of a fragment as a modular section of an activity, which has its own lifecycle, receives its own input events, and which you can add or remove while the activity is running (sort of like a "sub activity" that you can reuse in different activities). A fragment must always be hosted in an activity and the fragment's lifecycle is directly affected by the host activity's lifecycle.

* What is the difference between a `Fragment` and an `Activity`? Explain the relationship between the two.
	- A fragment has its own layout and its own behavior with its own lifecycle callbacks. You can add or remove fragments in an activity while the activity is running. You can combine multiple fragments in a single activity to build a multi-pane UI. A fragment can implement a behavior that has no user interface component.

* Why is it recommended to use only the default constructor to create a `Fragment`? [StackOverflow](https://stackoverflow.com/a/16042750/2809326)
	- The reason why you should be passing parameters through bundle is because when the system restores a fragment (e.g on config change), it will automatically restore your bundle.

	- The callbacks like onCreate or onCreateView should read the parameters from the bundle - this way you are guaranteed to restore the state of the fragment correctly to the same state the fragment was initialised with (note this state can be different from the onSaveInstanceState bundle that is passed to the onCreate/onCreateView)

	- The recommendation of using the static newInstance() method is just a recommendation. You can use a non default constructor but make sure you populate the initialisation parameters in the bundle inside the body of that constructor. And read those parameters in the onCreate() or onCreateView() methods.

* How would you communicate between two Fragments? [Android Official](https://developer.android.com/training/basics/fragments/communicating.html)

* What is retained `Fragment`? [AndroidDesignPatterns](https://www.androiddesignpatterns.com/2013/04/retaining-objects-across-config-changes.html)
	-  All Fragment-to-Fragment communication is done either through a shared ViewModel or through the associated Activity. Two Fragments should never communicate directly.
	-  ViewModel objects are designed to outlive specific instantiations of views or LifecycleOwners. This design also means you can write tests to cover a ViewModel more easily as it doesn't know about view and Lifecycle objects. ViewModel objects can contain LifecycleObservers, such as LiveData objects. However ViewModel objects must never observe changes to lifecycle-aware observables, such as LiveData objects. If the ViewModel needs the Application context, for example to find a system service, it can extend the AndroidViewModel class and have a constructor that receives the Application in the constructor, since Application class extends Context.

![ViewModelLifeCycle](https://developer.android.com/images/topic/libraries/architecture/viewmodel-lifecycle.png)

#### Views and ViewGroups

* What is `View` in Android?
	- View is a basic building block of UI (User Interface) in android. A view is a small rectangular box which responds to user inputs. Eg: EditText , Button , CheckBox , etc.. ViewGroup is a invisible container of other views (child views) and other viewgroups.

* Difference between `View.GONE` and `View.INVISIBLE`?
	- `View.INVISIBLE` This view is invisible, but it still takes up space for layout purposes. `View.GONE` This view is invisible, and it doesn't take any space for layout purposes.

* Can you create custom views? How?
	- If you only need to make small adjustments to an existing widget or layout, you can simply subclass the widget or layout and override its methods. Creating your own View subclasses gives you precise control over the appearance and function of a screen element.

* What are ViewGroups and how they are different from the Views?
	- A ViewGroup is a special view that can contain other views (called children.) The view group is the base class for layouts and views containers. This class also defines the ViewGroup.LayoutParams class which serves as the base class for layouts parameters.

	- View class represents the basic building block for user interface components. A View occupies a rectangular area on the screen and is responsible for drawing and event handling. View is the base class for widgets, which are used to create interactive UI components (buttons, text fields, etc.).

* What is a canvas?
	- The Canvas class holds the "draw" calls. To draw something, you need 4 basic components: A Bitmap to hold the pixels, a Canvas to host the draw calls (writing into the bitmap), a drawing primitive (e.g. Rect, Path, text, Bitmap), and a paint (to describe the colors and styles for the drawing).

* What is a `SurfaceView`?
	- When you create a custom view and override its onDraw() method, all drawing happens on the UI thread. Drawing on the UI thread puts an upper limit on how long or complex your drawing operations can be, because your app has to complete all its work for every screen refresh. One option is to move some of the drawing work to a different thread using a SurfaceView. 
		- All the views in your view hierarchy are rendered onto one Surface in the UI thread.
		- In the context of the Android framework, Surface refers to a lower-level drawing surface whose contents are eventually displayed on the user's screen.
		- A SurfaceView is a view in your view hierarchy that has its own separate Surface, as shown in the diagram below. You can draw to it in a separate thread.
		- To draw, start a thread, lock the SurfaceView's canvas, do your drawing, and post it to the Surface.

* Relative Layout vs Linear Layout.
	- `LinearLayout` adds view linearly either vertical or horizontal by the orientation set by you. It will add views one after another which will depend on the requirement of the design. And `RelativeLayout` adds view related with each other, there is no need to declare orientation in `RelativeLayout`.

* Tell about Constraint Layout [Mindorks](https://blog.mindorks.com/using-constraint-layout-in-android-531e68019cd)
	- Intention of `ConstraintLayout` is to optimize and flatten the view hierarchy of your layouts by applying some rules to each view to avoid nesting. Rules remind you of `RelativeLayout`, for example setting the left to the left of some other view.
```
app:layout_constraintBottom_toBottomOf="@+id/view1"
```
	- Unlike `RelativeLayout`, `ConstraintLayout` offers bias value that is used to position a view in terms of 0% and 100% horizontal and vertical offset relative to the handles (marked with circle). These percentages (and fractions) offer seamless positioning of the view across different screen densities and sizes.
   ```java
	app:layout_constraintHorizontal_bias="0.33" <!-- from 0.0 to 1.0 -->
	app:layout_constraintVertical_bias="0.53" <!-- from 0.0 to 1.0 -->
   ```
	- Baseline handle (long pipe with rounded corners, below the circle handle) is used to align content of the view with another view reference. Square handles (on each corner of the view) are used to resize the view in dps.

* Do you know what is the view tree? How can you optimize its depth?

#### Displaying Lists of Content

* What is the difference between `ListView` and `RecyclerView`?
	- The RecyclerView is much more powerful, flexible and a major enhancement over ListView
		1. ViewHolder Pattern. In a ListView, it was recommended to use the ViewHolder pattern but it was never a compulsion. In case of RecyclerView, this is mandatory using the RecyclerView.ViewHolder class. This is one of the major differences between the ListView and the RecyclerView. It makes things a bit more complex in RecyclerView but a lot of problems that we faced in the ListView are solved efficiently.
		2. LayoutManager. This is another massive enhancement brought to the RecyclerView. In a ListView, the only type of view available is the vertical ListView. There is no official way to even implement a horizontal ListView.
		3. Item Animator. ListViews are lacking in support of good animations, but the RecyclerView brings a whole new dimension to it. Using the RecyclerView.ItemAnimator class, animating the views becomes so much easy and intuitive.
		4. Item Decoration. In case of ListViews, dynamically decorating items like adding borders or dividers was never easy. But in case of RecyclerView, the RecyclerView.ItemDecorator class gives huge control to the developers but makes things a bit more time consuming and complex.
		5. OnItemTouchListener. Intercepting item clicks on a ListView was simple, thanks to its AdapterView.OnItemClickListener interface. But the RecyclerView gives much more power and control to its developers by the RecyclerView.OnItemTouchListener but it complicates things a bit for the developer.

	- In simple words, the RecyclerView is much more customizable than the ListView and gives a lot of control and power to its developers.

* What is the ViewHolder pattern? Why should we use it?
	- The ViewHolder design pattern enables you to access each list item view without the need for the look up, saving valuable processor cycles. Specifically, it avoids frequent call of findViewById() during ListView scrolling, and that will make it smooth.

* What is `SnapHelper`? [Mindorks](https://blog.mindorks.com/using-snaphelper-in-recyclerview-fc616b6833e8)
	- SnapHelper is a helper class that helps in snapping any child view of the RecyclerView. For example, you can snap the firstVisibleItem of the RecyclerView as you must have seen in the play store application that the firstVisibleItem will be always completely visible when scrolling comes to the idle position.

#### Dialogs and Toasts

* What is `Dialog` in Android?
	- A dialog is a small window that prompts the user to make a decision or enter additional information. A dialog does not fill the screen and is normally used for modal events that require users to take an action before they can proceed.

* What is `Toast` in Android?
	- A toast provides simple feedback about an operation in a small popup. It only fills the amount of space required for the message and the current activity remains visible and interactive. Toasts automatically disappear after a timeout.

* What the difference between `Dialog` and `Dialog Fragment`?
	- A DialogFragment is a fragment that displays a dialog window, floating on top of its activity's window. This fragment contains a Dialog object, which it displays as appropriate based on the fragment's state. Control of the dialog (deciding when to show, hide, dismiss it) should be done through the API, not with direct calls on the dialog.

#### Intents and Broadcasting

* What is `Intent`? [StackOverflow](https://stackoverflow.com/questions/6578051/what-is-an-intent-in-android)
	- An Intent is basically a message to say you did or want something to happen. Depending on the intent, apps or the OS might be listening for it and will react accordingly. Think of it as a blast email to a bunch of friends, in which you tell your friend John to do something, or to friends who can do X ("intent filters"), to do X. The other folks will ignore the email, but John (or friends who can do X) will react to it.

* What is an Implicit `Intent`?
	- Is something which is sent from one activity to inbuilt android activity in android. When we work with implicit intents, we generally specify the action which we want to perform and optionally some data required for that action. Data is typically expressed as a Uri which can represent an image in the gallery or person in the contacts database. Implicit Intents do not directly specify the Android components which should be called , it only specifies action to be performed.An Uri can be used with the implicit intent to specify data type.

	```java
	Intent intent = new Intent(ACTION_VIEW,Uri.parse("http://www.google.com");
	```

* What is an Explicit `Intent`?
	- Explicit intents are used in the application itself wherein one activity can switch to other activty.

	```java
	Intent intent = new Intent(this,Target.class); 
	```
	
	- this causes switching of activity from current context to the target activity. Explicit Intents can also be used to pass data to other activity using putExtra method and retrieved by target activity by getIntent().getExtras() methods.

* What is a `BroadcastReceiver`? [StackOverflow](https://stackoverflow.com/questions/5296987/what-is-broadcastreceiver-and-when-we-use-it)
	- A broadcast receiver is a component that responds to system-wide broadcast announcements. Many broadcasts originate from the system—for example, a broadcast announcing that the screen has turned off, the battery is low, or a picture was captured. Applications can also initiate broadcasts—for example, to let other applications know that some data has been downloaded to the device and is available for them to use. Although broadcast receivers don't display a user interface, they may create a status bar notification to alert the user when a broadcast event occurs.

* What is a `LocalBroadcastManager`? [Developer Android](https://developer.android.com/reference/android/support/v4/content/LocalBroadcastManager.html)
	- Helper to register for and send broadcasts of Intents to local objects within your process. This has a number of advantages over sending global broadcasts with sendBroadcast(Intent):
		- You know that the data you are broadcasting won't leave your app, so don't need to worry about leaking private data.
		- It is not possible for other applications to send these broadcasts to your app, so you don't need to worry about having security holes they can exploit.
		- It is more efficient than sending a global broadcast through the system.

* What is the function of an `IntentFilter`?
	- An intent filter is an expression in an app's manifest file that specifies the type of intents that the component would like to receive. `IntentFilter` objects are often created in XML as part of a package's `AndroidManifest.xml` file, using `intent-filter` tags.

	```java
	<intent-filter>
	    <data android:mimeType="image/*" />
	    ...
	</intent-filter>
	```
* What is a Sticky `Intent`? [AndroidInterview](http://www.androidinterview.com/what-is-a-sticky-intent/)
	- Sticky Intent is also a type of Intent which allows a communication between function and a service sendStickyBroadcast() performs a sendBroadcast(Inent) know as sticky,the Intent your are sending stays around after the broadcast is complete, so that others can quickly retrieve that data through the return value of registerReceiver(BroadcastReceiver, IntentFilter). In all other ways, this behaves the same as sendBroadcast(Intent).

* Describe how broadcasts and intents work to be able to pass messages around your app?
	- When a broadcast intent is created, it must include an action string in addition to optional data and a category string. As with standard intents, data is added to a broadcast intent using key-value pairs in conjunction with the putExtra() method of the intent object. The optional category string may be assigned to a broadcast intent via a call to the addCategory() method.

	- The action string, which identifies the broadcast event, must be unique and typically uses the application’s Java package name syntax. For example, the following code fragment creates and sends a broadcast intent including a unique action string and data:

	```java
	Intent intent = new Intent();
	intent.setAction("com.example.Broadcast");
	intent.putExtra("HighScore", 1000);
	sendBroadcast(intent);
	```
	- The above code would successfully launch the corresponding broadcast receiver on a device running an Android version earlier than 3.0. On more recent versions of Android, however, the intent would not be received by the broadcast receiver. This is because Android 3.0 introduced a launch control security measure that prevents components of stopped applications from being launched via an intent. An application is considered to be in a stopped state if the application has either just been installed and not previously launched, or been manually stopped by the user using the application manager on the device. To get around this, however, a flag can be added to the intent before it is sent to indicate that the intent is to be allowed to start a component of a stopped application. This flag is FLAG_INCLUDE_STOPPED_PACKAGES and would be used as outlined in the following adaptation of the previous code fragment:

	```java
	Intent intent = new Intent();
	intent.addFlags(Intent.FLAG_INCLUDE_STOPPED_PACKAGES);
	intent.setAction("com.example.Broadcast");
	intent.putExtra("HighScore", 1000);
	sendBroadcast(intent);
	```

* What is a `PendingIntent`?
	- A PendingIntent is a token that you give to a foreign application (e.g. NotificationManager, AlarmManager, Home Screen AppWidgetManager, or other 3rd party applications), which allows the foreign application to use your application's permissions to execute a predefined piece of code.

	- If you give the foreign application an Intent, it will execute your Intent with its own permissions. But if you give the foreign application a PendingIntent, that application will execute your Intent using your application's permission.

* What are the different types of Broadcasts?
	- Normal broadcasts:-Normal broadcasts (sent with Context.sendBroadcast) are completely asynchronous. All receivers of the broadcast are run in an undefined order, often at the same time. This is more efficient, but means that receivers cannot use the result or abort APIs included here.

	- Ordered broadcasts :- Ordered Broadcast is the type of broadcast which is sent in a synchronous manner i.e. one by one to each listener. Android sendOrderedBroadcast method falls in Context class of Android, the purpose of this method is to broadcast to listening receivers in a serialized manner and receive the result back to the calling activity. 

	- Sticky broadcasts:- A Sticky Broadcast is a Broadcast that stays around following the moment it is announced to the system. Most Broadcasts are sent, processed within the system and become quickly inaccessible. However, Sticky Broadcasts announce information that remains accessible beyond the point at which they are processed. A typical example is the battery level Broadcast. Unlike most Broadcasts, the battery level can be retrieved within applications beyond the point at which it was sent through the system. This means that apps can find out whatever the last battery level broadcast was.

#### Services

* What is `Service`?
	- A Service is an application component that can perform long-running operations in the background, and it doesn't provide a user interface. Another application component can start a service, and it continues to run in the background even if the user switches to another application. Additionally, a component can bind to a service to interact with it and even perform interprocess communication (IPC). For example, a service can handle network transactions, play music, perform file I/O, or interact with a content provider, all from the background.

* `Service` vs `IntentService`. [StackOverflow](https://stackoverflow.com/a/15772151/5153275)
	- `Service` is a base class of service implementation. `Service` class is run in the application’s main thread which may reduce the application performance. Thus, `IntentService`, which is a direct subclass of `Service` is borned to make things easier. The `IntentService` is used to perform a certain task in the background. Once done, the instance of `IntentService` terminate itself automatically. Examples for its usage would be to download a certain resources from the Internet.
	- A `Service` is a broader implementation for the developer to set up background operations, while an `IntentService` is useful for “fire and forget” operations, taking care of background Thread creation and cleanup.

* What is a `JobScheduler`? [Vogella](http://www.vogella.com/tutorials/AndroidTaskScheduling/article.html)
	- JobScheduler is the Android framework API for scheduling tasks or work. It first became available in Android 5.0 (API level 21), and remains under active development. Notably, Android 7.0 (API level 24) added the ability to trigger jobs based on ContentProvider changes.

	- JobScheduler is implemented in the platform, which allows it to collect information about jobs that need to run across all apps. This information is used to schedule jobs to run at, or around, the same time. Batching job execution in this fashion allows the device to enter and stay in sleep states longer, preserving battery life.

	- You use JobScheduler by registering jobs, specifying their requirements for network and timing. The system then gracefully schedules the jobs to execute at the appropriate times. At the same time, it also defers job execution as necessary to comply with Doze and App Standby restrictions. JobScheduler provides many methods to define job-execution conditions.

#### Inter-process Communication

* How can two distinct Android apps interact?
	- An Intent can be explicit in order to start a specific component (a specific Activity instance) or implicit in order to start any component that can handle the intended action (such as "capture a photo").

* Is it possible to run an Android app in multiple processes? How?
	- You can specify android:process=":remote" in your manifest to have an activity/service run in a seperate process.

	- The "remote" is just the name of the remote process, and you can call it whatever you want. If you want several activities/services to run in the same process, just give it the same name.

```java
<activity android:name=".RemoteActivity" android:label="@string/app_name" android:process=":RemoteActivityProcess"/>
```

* What is AIDL? Enumerate the steps in creating a bounded service through AIDL.
	- On Android, one process cannot normally access the memory of another process. So to talk, they need to decompose their objects into primitives that the operating system can understand, and marshall the objects across that boundary for you. The code to do that marshalling is tedious to write, so Android handles it for you with AIDL. To create a bounded service using AIDL, follow these steps:

		1. Create the .aidl file. This file defines the programming interface with method signatures.
		2. Implement the interface. The Android SDK tools generate an interface in the Java programming language, based on your .aidl file. This interface has an inner abstract class named Stub that extends Binder and implements methods from your AIDL interface. You must extend the Stub class and implement the methods.
		3. Expose the interface to clients. Implement a Service and override onBind() to return your implementation of the Stub class.

* What can you use for background processing in Android?

* What is a `ContentProvider` and what is it typically used for?
	- A ContentProvider manages access to a structured set of data. It encapsulates the data and provide mechanisms for defining data security. ContentProvider is the standard interface that connects data in one process with code running in another process.


#### Long-running Operations

* How would you perform a long-running operation in an application?

* Why should you avoid to run non-ui code on the main thread?

* What is ANR? How can the ANR be prevented?

* What is an `AsyncTask`?

* What are the problems in asynctask?

* When would you use java thread instead of an asynctask?

* What is a `Loader`?

* What is the relationship between the life cycle of an `AsyncTask` and an `Activity`? What problems can this result in? How can these problems be avoided?

* Explain `Looper`, `Handler` and `HandlerThread`. [Mindorks](https://blog.mindorks.com/android-core-looper-handler-and-handlerthread-bd54d69fe91a)

#### Working With Multimedia Content

* How do you handle bitmaps in Android as it takes too much memory?

* What is the difference between a regular `Bitmap` and a nine-patch image?

* Tell about the `Bitmap` pool. [Mindorks](https://blog.mindorks.com/how-to-use-bitmap-pool-in-android-56c71a55533c)

* How to play sounds in Android? [Vogella](http://www.vogella.com/tutorials/AndroidMedia/article.html)

#### Data Saving

* How to persist data in an Android app?

* What is ORM? How does it work?

* How would you preserve `Activity` state during a screen rotation? [StackOverflow](https://stackoverflow.com/questions/3915952/how-to-save-state-during-orientation-change-in-android-if-the-state-is-made-of-m)

* What are different ways to store data in your Android app?

#### Look and Feel

* What is a `Spannable`?

#### Memory Optimizations

* What is the `onTrimMemory()` method?

* How does the OutOfMemory happens?

* How do you find memory leaks in Android applications? [Mindorks](https://mindorks.com/blog/detecting-and-fixing-memory-leaks-in-android)

#### Battery Life Optimizations

* How to reduce battery usage in an android application? [Mindorks](https://blog.mindorks.com/battery-optimization-for-android-apps-f4ef6170ff70)

* What is Doze? What about App Standby?

* What is `overdraw`? [Developer Android](https://developer.android.com/topic/performance/rendering/overdraw.html)

#### Supporting Different Screen Sizes

* How did you support different types of resolutions?

#### Permissions

* What are the different protection levels in permission?

#### Native Programming

* What is the NDK and why is it useful?

* What is renderscript? [Mindorks](https://blog.mindorks.com/comparing-android-ndk-and-renderscript-1a718c01f6fe)

#### Android System Internal

* What is the Dalvik Virtual Machine?

* What is the difference JVM, DVM and ART?

* What are the differences between Dalvik and ART?

* What is DEX?

* Can you manually call the Garbage collector?

#### Debugging and Programming Tools

* What is ADB?

* What is DDMS and what can you do with it?

* What is the StrictMode? [Mindorks](https://blog.mindorks.com/use-strictmode-to-find-things-you-did-by-accident-in-android-development-4cf0e7c8d997)

* What is Lint? What is it used for?

#### Others

* Why Bundle class is used for data passing and why cannot we use simple Map data structure

* How do you troubleshoot a crashing application?

* Explain Android notification system?

* What is the difference between Serializable and Parcelable? Which is the best approach in Android?

* Have you developed widgets? Describe. [Mindorks](https://blog.mindorks.com/android-widgets-ad3d166458d3)

* What is AAPT?

* What is the best way to update the screen periodically?

* FlatBuffers vs JSON. [Mindorks](https://blog.mindorks.com/why-consider-flatbuffer-over-json-2e4aa8d4ed07)

* `HashMap`, `ArrayMap` and `SparseArray` [Mindorks](https://blog.mindorks.com/android-app-optimization-using-arraymap-and-sparsearray-f2b4e2e3dc47)

* What are Annotations? [Mindorks](https://blog.mindorks.com/creating-custom-annotations-in-android-a855c5b43ed9), [Link](https://blog.mindorks.com/improve-your-android-coding-through-annotations-26b3273c137a)

* How to handle multi-touch in android [GitHub](https://arjun-sna.github.io/android/2016/07/20/multi-touch-android/)

* How to implement XML namespaces?

* What is the support library? Why was it introduced?[MartianCraft](http://martiancraft.com/blog/2015/06/android-support-library/)

* What is Android Data Binding? [Developer Android](https://developer.android.com/topic/libraries/data-binding/index.html)

* What are Android Architecture Components? [Developer Android](https://developer.android.com/topic/libraries/architecture/index.html)

* How to implement search using RxJava operators? [Mindorks](https://blog.mindorks.com/implement-search-using-rxjava-operators-c8882b64fe1d)


### Architecture

* Describe the architecture of your last app.

* Describe MVP. [Mindorks](https://mindorks.com/course/android-mvp-introduction)

* What is presenter?

* What is model?

* Describe MVC.

* What is controller?

* Describe MVVM. [GitHub](https://github.com/MindorksOpenSource/android-mvvm-architecture)

* Tell something about clean code [Mindorks](https://blog.mindorks.com/every-programmer-should-read-this-book-6755dedec78d)


### Design Problem

* Design Uber App.

* Design Facebook App.

* Design Facebook Near-By Friends App.

* Design WhatsApp.

* Design SnapChat.

* Design problems based on location based app.


### Tools And Technologies

* Git. [GitHub](https://github.com/git-tips/tips)

* RxJava. [Mindorks](https://blog.mindorks.com/a-complete-guide-to-learn-rxjava-b55c0cea3631)

* Dagger 2. [Mindorks](https://blog.mindorks.com/a-complete-guide-to-learn-dagger-2-b4c7a570d99c)

* Android Development Useful Tools. [Mindorks](https://blog.mindorks.com/android-development-useful-tools-fd73283e82e3)

* Firebase. [Firebase.google.com](https://firebase.google.com/)


### Android Test Driven Development

* What is Espresso? [Developer Android](https://developer.android.com/training/testing/ui-testing/espresso-testing.html)

* What is Robolectric? [Robolectric](http://robolectric.org/)

* What is UI-Automator? [Developer Android](https://developer.android.com/training/testing/ui-testing/uiautomator-testing.html)

* Explain unit test.

* Explain instrumented test.

* Have you done unit testing or automatic testing?

* Why Mockito is used? [Official site](http://site.mockito.org/)

* Describe JUnit test.


### Others

* Describe how REST APIs work.

* Describe SQLite.

* Describe database.

* Project Management tool - trello, basecamp, kanban, jira, asana.

* About build System - gradle, maven, ant, buck.

* About multiple apk for android application. [Mindorks](https://mindorks.com/blog/how-to-create-multiple-apk-files-for-android-application)

* Reverse Engineering an APK.

* What is proguard used for?

* What is obfuscation? What is it used for? What about minification?

* How do you build your apps for release?

* How do you control the application version update to specific number of users?

* Can we identify users who have uninstalled our application?

* Implement Search Using RxJava Operators. [Mindorks](https://blog.mindorks.com/implement-search-using-rxjava-operators-c8882b64fe1d)

* APK Size Reduction. [Mindorks](https://blog.mindorks.com/how-to-reduce-apk-size-in-android-2f3713d2d662)

* Android Development Best Practices. [Mindorks](https://blog.mindorks.com/android-development-best-practices-83c94b027fd3)

* Android Code Style And Guidelines. [Mindorks](https://blog.mindorks.com/android-code-style-and-guidelines-d5f80453d5c7)

* Have you tried Kotlin? [Medium](https://medium.com/p/why-you-must-try-kotlin-for-android-development-e14d00c8084b)

* What are the metrics that you should measure continuously while android application development? [Mindorks](https://blog.mindorks.com/android-app-performance-metrics-a1176334186e)


### Found this project useful :heart:

* Support by clicking the :star: button on the upper right of this page. :v:

[Check out Mindorks awesome open source projects here](https://mindorks.com/open-source-projects)


### License
```
   Copyright (C) 2017 MINDORKS NEXTGEN PRIVATE LIMITED

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
```

### Contributing to Android Interview Questions
Just make pull request. You are in!
