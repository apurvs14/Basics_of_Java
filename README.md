# Basics_of_Java

Part 1 : Java Platform

#1.Why is Java so Popular?
Java is popular beacuse of the following reasons-
1.Java is a Platform Independent language.
2. OOP(Object oriented programming) paradigm.
3.Java has backward compatibility i.e. older java code can easily run new versions java without any significant changes.

#2.What is Platform Independence?
In easy words, when we build one application which can be run on different operating systems we achieve platform independence.
when we compile a java code(.java file) the output is in the form of JAR file(.class file) which contains internal java 
representation called bytecode. This Jar file can be read by any operating system where JVM is installed.Every JVM is configured 
differently for each operating system but irrespective of OS, JVM can understand Bytecode and converts it into an executable 
set of instructions(or code).

#3.What is ByteCode?
The .class file has set of instructions(which are executed by JVM) for JVM called ByteCode.
BytesCode helps in establishing platform independency for java code.

#4.Compare JDK vs JVM VS JRE.
These three are the components of java programming.
JVM-
*JVM stans for java virtual machine
*it provides runtime enviornment to run java bytecode.
*it makes java platform Independent.

JRE-
*JRE stands for Java Runtime Environment.
*it indcludes JVM, Java libraries and other files required to run Java applications.
*it is used for running the application rather than compiling or building it.
*usually it is installed in end users machine to run the application.


JDK-
*JDK stands for Java development kit.
*It includes the Java Compiler, Java Runtime Environment (JRE),
Java libraries, and other tools required for Java programming.
*it is used to create, compile, and debug Java applications.


#5. what is the role of class loader?
class loader is a component of JVM,it is responsible for loading java classes into jvm during runtime.
---------------------------------------------------------------------------------------------------------
Part 2 - Wrapper Classes

#1.What are wrapper classes?
Wrapper classes are part of java.lang package which are used to represent primitive data types as 
Objects.

#2.Why do we need Wrapper Classes in Java?
Wrapper classes are used to wrap primitive data types into objects so that they can be used in Object-
oriented paradigm where objects are required.

#3.What are the different ways of creating Wrapper Class Instances?
There are two ways of creating a wrapper class instance,
1.Using wrapper class constructor.
2.using valueOf methods.

#4.What is Auto Boxing?
Auto boxing is the conversion of primitive data type to the respective wrapper class.
for example Interger to int, etc.

#5.What are the advantages of Auto Boxing?
Auto Boxing saves memory by reusing already created Wrapper objects.It is also covienient for coders.
also makes code more readable and removes the boiler plate code of manually casting the primitive data
type into object type.


#6.What is Casting?
Casting is a process of converting one data type into another.there are two types of casting
1.Explicit casting- done manually by the coder 
2.Implicit casting- achieved by the compiler


#7.What is Implicit Casting?
Implicit casting is when the compiler automatically converts value of smaller data type to
a larger data type. It is done by the compiler without any external help.for example
int num = 56;
double num2 = num;


#8.What is Explicit Casting?
In explicit casting you need to specify the required data type in paranthesis.It is used when you want to
convert larger data type into smaller data type.This sometimes lead to loss of data.
double num = 5.16;
int num2 = (int) num;


----------------------------------------------------------------------------------------------------------
Part 3 - Strings 

#1.Are all String’s immutable?
Yes. Once a string is created it cannot be modified.


#2.Where are string values stored in memory?
The memory location depends upon how the string is created,
if string is created WITHOUT using "new" keyword then it will be stored in string constant pool inside
heap memory,compiler will check if the same string is present inside the pool if it does the same string will
be reused.
Whereas by using new keyword everytime a new string will be created inside the heap memory and 
it will not be reused.


#3.Why should you be careful about String Concatenation(+) operator in Loops?
As we know,in java strings are immutable hence everytime we concatinate a new string will be created
and allocated to memory which will lead to performance issues and inefficiency.It will increase the time
complexity and it will put extra burden on the memory.


#4.How do you solve above problem?
We can use the StringBuffer class to solve this problem.StringBuffer was created to solve
this inefficiency and it makes string mutable, which allows in-place modification and does not create 
unnecessary obvjects which improves efficiency and saves memory. rather than using concatination 
it requires to use append() to implement this.

#5.What are differences between String and StringBuffer?
1.strings are immutable whereas stringbuffer is mutable.
2.Stringbuffer yields better performance where string is being modified many times.
3.Both String and StringBuffer are thread safe but string is thread safe inherently since it is immutable
wheread StrinBuffer is specifically designed to be thread safe.
4.StringBuffer has all the methods of string as well as some additional methods used to modify the string.


#6.What are differences between StringBuilder and StringBuffer?
both are almost same except StringBuilder is not thread safe whereas stringbuffer is thread safe.


#7.Can you give examples of different utility methods in String class?
There are many methods in string class.
charAt(int param)-returns the character at particular index.
length()-returns the length of string.
toString()- returns a string represntation of an object.

---------------------------------------------------------------------------------------------------------
Part 4 - OOP’s 

#1.What is a class?
Class is usually called a blueprint or template of that defines structure and behavior of any object.
it has fields and methhods which define characterstic and behavior of an object created to the
corresponding class.

#2.What is state of an Object?
State of the class refers to the current value of fields of an object.A class can have many objects which 
might hold different values or state. we can change or get the state of an object using getter setter 
methods.

#3.What is behavior of an Object?
Behavior is the methods supported by that object,it refers to the methods or operations an object can
perform.An object can perform methods or behavior defined in its respective class.

#4.What is the super class of every class in Java?
Every java class is a sub class of object class,it inherits all methods of object class.

#5.explain about toString method ?
toString() is method of  object class,is used to convert an object into string representation.
but in order to achieve string representation, we need to override the toString() method of object class
inside the corresponding class of object and give it a representation. Otherwise it will return hashcode
of the object by default.

#6.What is the use of equals method in Java ?
it is a method of object class. It is used when we need to compare the content of two objects,the default implementation of this method
will compare the location of two objects or if they are pointing to the same object.In order to compare
the content we need to override this metthod inside corresponding java class.after overiding if the content
or fields of two objects are same the it will return true.

#7.What are the important things to consider when implementing equals method?
1.if the state of object is same, equals method should always return true until the state is changed.
2.Order of comparision should not matter,both objects when compared in any order should return the same result.


#8.What is the hashCode method used for in Java?
hashCode method is used to generate the hashcode of an object,which is numeric representation of the
state of an object.

#9.Explain inheritance.
Inheritance allows any class to have feilds and behaviors of another class,the class that inherits the methods
and fields is called the child class whereas the class that is being inherited from is called parent
class. inheritance is the ekey feature of Object oriented programming.it helps in maintaining code in a
better way and allows code reusablity.We can use extends keyword to inherit a class.


#10.What is Method Overloading?
When two methods with same name but different parameters exist inside a class or gets inherited is called
method overloading.


#11.What is Method Overriding?
When we create a method inside the child-class using same name and parameters as parent class with 
different implentation is called method overriding.

#12.Can super class reference variable can hold an object of sub class?
Yes, it is also known as polymorphism which is a key feature of Object oriented proggramming.


#13.Can super class reference variable can hold an object of sub class?
No,multiple inheritance creates a lot of complexities hence it is not allowed in java.

#14.What is an Interface ?
An interface is a collection of abstract methods which can be implemented by a class.If a class implements an
interface it needs to have implementation of all abstract methods.It is a contract.

#15.How do you define an Interface?
An interface can be defined by using Interface keyword.

#16.How do you implement an interface?
if we want a class to implement an interface ,we need to use "implements" keyword.

#17.Can you explain a few tricky things about interfaces?
1.Variables in an interface cannot be private,they are always public,static or final.
2.Interface methods are by default public and abstract.They cannot have implementations.


#18.Can you extend an interface?
An interface can extend another interface.But a class always implements an interface.

#19.Can a class implement multiple interfaces?
Yes,a class can implement multiple interfaces.it should implement all the methods in every interface 
being implemented.

#20.What is an Abstract Class ?
an abstract class is a class that cannot be instantiated and is meant to be extended by other classes.
It can contain abstract methods as well as regular methods with implementations, fields, constructors,
and other class members. 

#21.What is a Constructor?
A constructor is a method that is called when we need to create a new object.We call this method with new 
keyword.it has the same name as class and does not have a return type.

#22.What is a Default Constructor?
A default Constructer is a constructor without any parameters. it is used when dont want to initialize 
the state or set the default value of the fields while creating an object.It is provided by the compiler.
if we create a parameterized constructor, we will have to explixitly create default constructor as well.


#23.Will this code compile?
Yes,This code will compile but the default value of the field name will be "Default name".


#24.How do you call a Super Class Constructor from a Constructor?
we can call it by using super() keyword.

#25.will this code compile?
No,because super() keyword is not the first statement inside the constructor.

#26.What is the use of this()?
this() is used to invoke one contructor from another constructor inside the same class.

#27.Can a constructor be called directly from a method?
yes,it can be explicitly called from any method except another constructor.

#28.Is a super class constructor called even when there is no explicit call from a sub class constructor ?
If a super class constructor is not explicitly called from a sub class constructor, super class constructor
is automatically invoked from a sub class constructor.

#29.Difference between compile time and run time polymorphism
compile time polymorphism--
In compile time polymorphism, compiler resolves the methods during compilation.It is achieved by method
overloading, method overloading allows a class to have same method name but with different parameters
having different implementations.The decision that which method will be invoked is made upon compile time
based upon number and types of arguments passed while compilation phase.
run time polymorphism--
run time polymorphism occurs when a sub class redefines a method of superclass with new implementation which
is known as method overriding.The decision on which method to call is made at run-time by JVM hence it is 
called runtime polymorphism.

-----------------------------------------------------------------------------------------------------------

Part - 5 : Advanced OOP’s


#1.What is Polymorphism?
Polymorphism usually means "many forms". In java polmorphism is the abilty of objects of different types
to be treated as same type.when a program has different behaviors based on different input, it is reffered
as polymorphism.It allows us to code an interface and have multiple implementation.
It allows code to be written in a more generic way and increases code reusability.


#2.What is the use of instanceof Operator in Java?
instanceof Operator is used to determine if an object belongs to a partical class or is an instance of a 
class or a sub class.It is a comparison operator which returns a boolean.


#3.What is Coupling?
Coupling refers to a measure of how much one component is dependent on another inside a program.
two classes tighly coupled or having high coupling is not effcient for maintaining the code since change
in one class could disrupt the flow of output in another.

#4.What is Cohesion?
Cohesion is a measure of how much the methods of a class are related to each other, high cohesion means 
a better structure and flow of the code.

#5.What is Encapsulation?
It refers to hiding state or internal details of the object from outside world.encapsulation provides 
data-hiding and many other features.It restricts the access to the data and implementation through
well structure interface and abstract methods hiding the complex internal details/implementation of a method
or program.encapsulation is achieved through the use of access modifiers such as private, protected, 
and public, which control the visibility and accessibility of methods and fields.

#6. What is an Inner Class?
the classes which are defined inside a class are called inner classes. Inner classes have access to the members 
of the enclosing class.

#7.What is a Static Inner Class?
An inner class which is declared as static is called static inner class.

#8.Can you create an inner class inside a method?
yes.

#9.What is an Anonymous Class?
 an anonymous class is a type of inner class that does not have a name and is defined in a single statement.
 
 ---------------------------------------------------------------------------------------------------------------

Part - 6 : Modifiers 


#1.What is default class modifier?
Default class is a class which has no access modifier specified, they are visible only to the classes of same 
package.

#2.What is private access modifier?
Private access variables and methods can only be accessed by the same class.even subclasses cannot access
private variables and methods.

#3.What is default or package access modifier?
Default fields and methods can be accessed by the classes from same package,these are also visible in
the subclasses of same package from superclass

#4.What is protected access modifier?
protected fields and methods can be accessed by the classes from same package,these are also visible in
the subclasses of any package from superclass.

#5.What is public access modifier?
public fields and methods can be accessed by any java class,public fields and methods from super class are
all accessed by subclass.

#6.What access types of variables can be accessed from a Class in Same Package?
default can be accessed from a class in same package.

#7.What access types of variables can be accessed from a Class in Different Package?
Public and protected can be accessed from a Class in Different Package.

#8.What access types of variables can be accessed from a Sub Class in Same Package?
default variables can be accessed from a Sub Class in Same Package.

#9.What access types of variables can be accessed from a Sub Class in Different Package?
public and protected variables can be accessed from a Sub Class in Different Package.

#10.What is the use of a final modifier on a class ?
class with final keyword cannot be extended and inherited.it is rarely used as it prevents code reusability.

#11.What is the use of a final modifier on a method ?
A method with final modifier cannot be overridden while inheriting.

#12.What is a Final Variable ?
Once a final variable is initialize, the value of that variable cannot be reassigned.

#13.What is a Final Argument ?
final arguments value cannot be changed or modified.

#14.What is a Static Variable ?
static variables and methods belong to the class rather than the objects,when a variable is declared static
its memory is allocated only once when the class is loaded and its value is retained throughout the 
lifetime of the program.


------------------------------------------------------------------------------------------------------------
Part 7 - Collections 

#1.Why do we need Collections in Java?
General arrays in java are not dynamic,once created we cannot alter their size or add new elements to it,
collections solve that problem. with the help of collection we can add, delete and do multiple operations.
collections host different number of collections to choose from for the required use.Collections also make
program optimized and increases reusability of code.

#2.What are the important interfaces in the Collection Hierarchy?
the important interfaces in collection Hierarchy are 
1.Collection
2.list
3.queue
4.map
5.set

#3.What are the important methods that are declared in the Collection Interface?
the important methods that are declared in the Collection Interface are methods to add and remove elements
size() method returns the number of elements in the collection.
There are many other methods as well.

#4.Can you explain briefly about the List Interface?
the List interface in java is part of the Collection hierarchy and extends the Collection interface. Hence
it contains all the methods defined in collection interface.
it is a collection of elements that allows duplicates and adds elements in a sequence.We can also add 
elements at a specific position.

#5.Explain about ArrayList with an example?
ArrayList implements the list interface, hence it has the properties of list. ArrayList have dynamic sizing
which means the size gets increases and decreased based upon the elements added or removed from the list.
List<Integer> array = new ArrayList<Integer>();
this is how an ArrayList is declared



#6.Can an ArrayList have Duplicate elements?
Yes, ArrayList can have duplicate elements.

#7.How do you iterate around an ArrayList using Iterator?
first we need an ArrayList
List<String> animals = new ArrayList<>();
animals.add("Lion");
animals.add("Tiger");
animals.add("cheetah");
animals.add("Elephant");
animals.add("wolf");

now we will create an iterator for arraylist
Iterator<String> iterator = animals.iterator();

no we will iterate over it,we will use hasNext() and next() methods

while(iterator.hasNext()){

System.out.println(iterator.next());

}

this way we can use iterator over an ArrayList.


#8.How do you sort an ArrayList?
we use collections.sort method to sort an ArrayList.

#9.How do you sort elements in an ArrayList using Comparable interface?
in order to use comparable interface for sorting, we need to override compareTo method inside the class
and implement comparable interface while declaring the class.

Class Employee implements  Comparable<Employee>{

  int salary;
		String name;
		public Employee(String name, int salary) {
				super();
				this.name = name;
				this.salary = salary;
		}

		@Override
		public String toString() {
				return name + " " + salary;
		}

		@Override
		public int compareTo(Employee emp) {
				if (this.salary > emp.salary) {
						return 1;
				}
				if (this.salary < emp.salary) {
						return -1;
				}
				return 0;
		}
}

List<Employee> employees = new ArrayList<>();
we will add 5 employee objects
after adding those ojects to the arraylist we will sort using
Collection.sort(employees)
this will sort our employees list based on the overridden compareTo() method.

}


#10.How do you sort elements in an ArrayList using Comparator interface?
in order to use Comparator interface for sorting, we need to override compare method inside the class
and implement Comparator interface while declaring the class.Here we pass two objects as arguments while invoking the method.

#11.What is Vector class? How is it different from an ArrayList?
vector is a class that implements dynamic arrays.Both ArrayList and vector are part of Collections Framework.
despite being similar they ahave a few differences,Vector is thread safe which means it can be sychronized 
adn can be used in a multithreaded environment.Due to the same reason vector is a little slower in performance.

#12.What is LinkedList? What interfaces does it implement? How is it different from an ArrayList?
Linked List extends List and Queue.Other than operations exposed by the Queue interface, LinkedList
has the same operations as an ArrayList. However, the underlying implementation of Linked List is
different from that of an ArrayList.ArrayList uses an Array kind of structure to store elements.
So, inserting and deleting from an ArrayList are expensive operations. However, search of an 
ArrayList is faster than LinkedList.


#13.Can you briefly explain about the Set Interface?
Set interface has almost the same methods that are present in collection interface,The only difference is that
theset does not allow duplicate elements.also there is no specific order.

#14.What are the important interfaces related to the Set Interface?
Set<E>,SortedSet<E> ,NavigableSet<E>  are some important interfaces related to set interface.

#15.What is the difference between Set and SortedSet interfaces?
Set and SortedSet interfaces do not allow duplicate elements.SortedSet Interface extends the Set Interface
the main difference between Set and SortedSet is that Set interface does not guarantee any order,
whereas the sortedset interface maintains elements in sorted manner.

#16.Can you give examples of classes that implement the Set Interface?
Set,TreeSet,LinkeHashSet,NavigableSet,SortedSet are some classes that implement the Set Interface.

#17.What is a HashSet?
HashSet is an implementation of Set interface, it represents collection of unordered and unique elements.

#18 question number 18 was not present in the problem statement.

#19.What is a TreeSet? How is different from a HashSet?
TreeSet implements Set,SortedSet and NavigableSet Interface.Treeset is similar to hashset Except it stores
elemnts in a sorted order.

#20.Can you give examples of implementations of NavigableSet?
TreeSet implements NavigableSet interface.Here is an example
TreeSet<Integer> numberTree = new TreeSet<Integer>();
numbersTreeSet.add(55);
numbersTreeSet.add(25);
numbersTreeSet.add(35);
numbersTreeSet.add(5);
numbersTreeSet.add(45);

NavigableSet interface has few methods.

Find the highest number which is lower than 25
System.out.println(numbersTreeSet.lower(25));//5

Find the highest number which is lower than or equal to 25
System.out.println(numbersTreeSet.floor(25));//25

Find the lowest number higher than 25
System.out.println(numbersTreeSet.higher(25));//35

Find the lowest number higher than or equal to 25
System.out.println(numbersTreeSet.ceiling(25));//25


#21.Explain briefly about Queue Interface?
Queue Interface extends Collection interface. Queue Interface is used for implementation of elements in \
order for processing. queue interface has methods like peek() and poll(). peek method return the elelment
at the beggining of the queue, and poll removes the element at head of the queue. 


#22.Can you briefly explain about the Map Interface?
map interface does not extend collection interface, so it does not have any methods of colletion interface
map interface organizes data in form of key value pair. key is a unique identifier for a data and value is
the data for that particular key.A key value pair in a Map interface is called an Entry.


#23.What is difference between Map and SortedMap?
SortedMap interface extends the Map interface. it maintains the key in sorted order.

#24.What is a HashMap?
HashMap implements Map interface.it supports data in form of key value pairs.


#25.What are the different methods in a Hash Map?
Generally used methods in HashMaps are 
1.put(key,value);
put method is used to store a key value pair inside a hashmap.here we need to pass key and value as 
arguments.
2.get()
get(key)
get methods returns the value of respective linked key passed as an argument.if the key is not found
it returns null.


#26.What is a TreeMap? How is different from a HashMap?
TreeMap is similar to HashMap except that it stores keys in sorted order. It implements NavigableMap 
interface and SortedMap interfaces along with the Map interface.

--------------------------------------------------------------------------------------------------------

Part - 8 : Exceptional Handling 

#1.Why is Exception Handling important?
Applications in the industry are large scale and complex.getting errors is inevitable,Whenever any error occurs, 
it is better that the user gets a meaningful message rather than a blue screen and the eroor can be understood 
by the end user as well. also the tecch support should be notified of error with enough information so
that they can identify and resolve the bug.


#3.What is the need for finally block?
Finally block is used when a certain piece of code needs to be executed irrespective of the exception
is thrown or the code inside try block is executed succesfully.The code which needs to be executed is 
written inside the finally block for example we no need to close the connection irrespective of successful execution of
code.

#4.In what scenarios is code in finally not executed?
the code in finally is not executed in two situations,
If exception is thrown in finally.
If JVM Crashes in between like using System.exit().


#5.Will finally be executed in the program below?
yes it will be executed.

#6.Is try without a catch is allowed?
yes it is allowed.

#7.Is try without catch and finally allowed?
No,it will give compilation error.

#8.Can you explain the hierarchy of Exception Handling classes?

Throwable has the highest level of hierarchy in Error Handling classes.

//Pre-defined Java Classes
class Error extends Throwable{}
class Exception extends Throwable{}
class RuntimeException extends Exception{}

#9.What is the difference between Error and Exception?
we call it an error when a programmer cannot do anything about the problem,or when it is not in 
programmers control like stackoverflow etc.
Exceptions can be handled by the programmer.

#10.What is the difference between Checked Exceptions and Unchecked Exceptions?
RuntimeException and classes that extend RuntimeException are called unchecked exceptions. 
For Example RuntimeException,UnCheckedException,UnCheckedException2 are unchecked or RunTime Exceptions.

#15.How do you handle multiple exception types with same exception handling block?
try {

} catch( IOException | SQLException ex ) {

}

this feature was introduced in java 7.
