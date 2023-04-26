Java 8 Features
1. Lambda Expression
2. Method References
3. Functional interfaces
4. Optional class
5. Stream API
6. Default methods
7. Static methods in interface
8. Base64 Encode Decode
9. Collectors class
10. ForEach() method
11. Parallel Array Sorting
12. IO Enhancements
13. Concurrency Enhancements
14. Collection API Improvements
Java 9 Features
1. Platform Module System (Project Jigsaw)
2. Interface Private Methods
3. Try-With Resources
4. Anonymous Classes
5. @SafeVarargs Annotation
6. Collection Factory Methods
7. Stream API Improvement
Java 10 Features
1. Local Variable Type Inference
2. New APIs & Options
Java 11 Features
Some of the important Java 11 features are:
1. Running Java File with single command
2. New utility methods in String class
3. Local-Variable Syntax for Lambda Parameters
4. Nested Based Access Control
5. Flight Recorder
6. Reading/Writing Strings to and from the Files
7. Not Predicate
8. HTTP Client
9. File APIs
10. Optional Class
Java 12 Features
Some of the important Java 12 features are;
1. Switch Expressions
2. File mismatch() Method
3. Compact Number Formatting
4. Teeing Collectors in Stream API
5. Java Strings New Methods - indent(), transform(), describeConstable(), and
resolveConstantDesc().
6. Pattern Matching for instanceof
Java 13 Features
1. Text Blocks
2. New Methods in String Class for Text Blocks
3. Switch Expressions Enhancements
4. Reimplement the Legacy Socket API
1. Lambda Expressions
Lambda expression helps us to write our code in functional style. It provides a clear and
concise way to implement SAM interface (Single Abstract Method) by using an expression.
It is very useful in collection library in which it helps to iterate, filter and extract data.
Why use Lambda Expression
1. To provide the implementation of Functional interface.
2. Less coding.
Java Lambda Expression Syntax
1. (Argument-list) -> {body}
Java lambda expression is consisted of three components.
1) Argument-list: It can be empty or non-empty as well.
2) Arrow-token: It is used to link arguments-list and body of expression.
3) Body: It contains expressions and statements for lambda expression.
Examples:
Runnable r1 = () -> {
System.out.println("My Runnable");
};

2.Method References
A method reference is the shorthand syntax for a lambda expression that
executes just ONE method. Here's the general syntax of a method reference:
Object :: methodName
Types of Method References
There are following types of method references in java:
1. Reference to a static method.
2. Reference to an instance method.
3. Reference to a constructor.
2.1) Reference to a Static Method
You can refer to static method defined in the class. Following is the syntax and example
which describe the process of referring static method in Java.
Syntax
1. ContainingClass::staticMethodName

2.2) Reference to an Instance Method
like static methods, you can refer instance methods also. In the following example, we are
describing the process of referring the instance method.
Syntax
1. containingObject::instanceMethodName
Example 1
In the following example, we are referring instance (non-static) method. Runnable
interface contains only one abstract method. So, we can use it as functional interface.
Example 2
In the following example, we are using BiFunction interface. It is a predefined interface
and contains a functional method apply(). Here, we are referring add method to apply
method.
2.3) Reference to a Constructor
You can refer a constructor by using the new keyword. Here, we are referring constructor
with the help of functional interface.
Syntax
1. ClassName::new
Functional Interface
An Interface that contains only one abstract method is known as functional interface. It
can have any number of default and static methods. It can also declare methods of object
class.
Functional interfaces are also known as Single Abstract Method Interfaces (SAM
Interfaces). We don’t need to use @FunctionalInterface annotation to mark an interface
as a Functional Interface.
@FunctionalInterface annotation is a facility to avoid the accidental addition of abstract
methods in the functional interfaces. You can think of it like @Override annotation and
its best practice to use it. java.lang.Runnable with a single abstract method run() is a
great example of a functional interface. One of the major benefits of the functional
interface is the possibility to use lambda expressions to instantiate them.



Optional
Java introduced a new class Optional in Java 8. It is a public final class which is used to
deal with NullPointerException in Java application. We must import java.util package to
use this class. It provides methods to check the presence of value for particular variable.



Stream API
Java 8 java.util.stream package consists of classes, interfaces and an enum to allow
functional-style operations on the elements. It performs lazy computation. So, it executes
only when it requires.
Stream provides following features:
o Stream does not store elements. It simply conveys elements from a source such as
a data structure, an array, or an I/O channel, through a pipeline of computational
operations.
o Stream is functional in nature. Operations performed on a stream does not modify
its source. For example, filtering a Stream obtained from a collection produces a
new Stream without the filtered elements, rather than removing elements from the
source collection.
o Stream is lazy and evaluates code only when required.
o The elements of a stream are only visited once during the life of a stream. Like an
Iterator, a new stream must be generated to revisit the same elements of the
source.
You can use stream to filter, collect, print, and convert from one data structure to other
etc. In the following examples, we have applied various operations with the help of stream.


For more examples, visit below provided link
https://www.javatpoint.com/java-8-stream
Default Methods
Java provides a facility to create default methods inside the interface. Methods which are
defined inside the interface and tagged with default keyword are known as default
methods. These methods are non-abstract methods and can have method body.
Java Default Method Example
In the following example, Sayable is a functional interface that contains a default and an
abstract method. The concept of default method is used to define a method with default
implementation. You can override default method also to provide more specific
implementation for the method.
Let's see a simple
Static Methods inside Java 8 Interface
You can also define static methods inside the interface. Static methods are used to define
utility methods. The following example explain, how to implement static method in
interface?
Abstract Class vs Java 8 Interface
After having default and static methods inside the interface, we think about the need of
abstract class in Java. An interface and an abstract class are almost similar except that you
can create constructor in the abstract class whereas you can't do this in interface.
Java Base64 Encoding and Decoding
Java provides a class Base64 to deal with encryption and decryption. You need to import
java.util.Base64 class in your source file to use its methods.
This class provides three different encoders and decoders to encrypt information at each
level.
Basic Encoding and Decoding
It uses the Base64 alphabet specified by Java in RFC 4648 and RFC 2045 for encoding and
decoding operations. The encoder does not add any line separator character. The decoder
rejects data that contains characters outside the base64 alphabet.
URL and Filename Encoding and Decoding
It uses the Base64 alphabet specified by Java in RFC 4648 for encoding and decoding
operations. The encoder does not add any line separator character. The decoder rejects
data that contains characters outside the base64 alphabet.
MIME
It uses the Base64 alphabet as specified in RFC 2045 for encoding and decoding
operations. The encoded output must be represented in lines of no more than 76
characters each and uses a carriage return '\r' followed immediately by a linefeed '\n' as
the line separator. No line separator is added to the end of the encoded output. All line
separators or other characters not found in the base64 alphabet table are ignored in
decoding operation.


Java Collectors
Collectors is a final class that extends Object class. It provides reduction operations, such
as accumulating elements into collections, summarizing elements according to various
criteria, etc.
Java Collectors class provides various methods to deal with elements


forEach
Java provides a new method forEach() to iterate the elements. It is defined in Iterable and
Stream interfaces.
It is a default method defined in the Iterable interface. Collection classes which extends
Iterable interface can use forEach() method to iterate elements.
This method takes a single parameter which is a functional interface. So, you can pass
lambda expression as an argument.


Java Parallel Array Sorting
Java provides a new additional feature in Array class which is used to sort array elements
parallel. New methods has added to java.util.Arrays package that use the JSR 166
Fork/Join parallelism common pool to provide sorting of arrays in parallel. The methods
are called parallelSort() and are overloaded for all the primitive data types and
Comparable objects.
The following table contains Arrays overloaded sorting methods.

Java 8 I/O Enhancements
In Java 8, there are several improvements to the java.nio.charset.Charset and extended
charset implementations. It includes the following:
o A New SelectorProvider which may improve performance or scalability for server.
The /dev/poll SelectorProvider continues to be the default. To use the Solaris event
port mechanism, run with the system property java.nio.channels.spi.Selector set to
the value sun.nio.ch.EventPortSelectorProvider.
o The size of <JDK_HOME>/jre/lib/charsets.jar file is decreased.
o Performance has been improvement for the java.lang.String(byte[], ∗) constructor
and the java.lang.String.getBytes() method.
Java 8 Concurrency Enhancements
The java.util.concurrent package added two new interfaces and four new classes.
Java.util.concurrent Interfaces
New Methods in java.util.concurrent.ConcurrentHashMap class
ConcurrentHashMap class introduces several new methods in its latest release. It includes
various forEach methods (forEach, forEachKey, forEachValue, and forEachEntry), search
methods (search, searchKeys, searchValues, and searchEntries) and a large number of
reduction methods (reduce, reduceToDouble, reduceToLong etc.). Other miscellaneous
methods (mappingCount and newKeySet) have been added as well.
New classes in java.util.concurrent.atomic
Latest release introduces scalable, updatable, variable support through a small set of new
classes DoubleAccumulator, DoubleAdder, LongAccumulator andLongAdder. It internally
employ contention-reduction techniques that provide huge throughput improvements as
compared to Atomic variables.
Collection API improvements
We have already seen forEach() method and Stream API for collections. Some new
methods added in Collection API are:
• Iterator default method forEachRemaining(Consumer action) to perform the given
action for each remaining element until all elements have been processed or the
action throws an exception.
• Collection default method removeIf(Predicate filter) to remove all of the elements
of this collection that satisfy the given predicate.
• Collection spliterator() method returning Spliterator instance that can be used to
traverse elements sequentially or parallel.
• Map replaceAll(), compute(), merge() methods.
• Performance Improvement for HashMap class with Key Collisions
Java 9 Module System
Java Module System is a major change in Java 9 version. Java added this feature to
collect Java packages and code into a single unit called module.
In earlier versions of Java, there was no concept of module to create modular Java
applications, that why size of application increased and difficult to move around. Even
JDK itself was too heavy in size, in Java 8, rt.jar file size is around 64MB.
To deal with situation, Java 9 restructured JDK into set of modules so that we can use
only required module for our project. Apart from JDK, Java also allows us to create our
own modules so that we can develop module-based application.
The module system includes various tools and options that are given below.
o Includes various options to the Java tools javac, jlink and java where we can specify
module paths that locates to the location of module.
o Modular JAR file is introduced. This JAR contains module-info.class file in its root folder.
o JMOD format is introduced, which is a packaging format similar to JAR except it can
include native code and configuration files.
o The JDK and JRE both are reconstructed to accommodate modules. It improves
performance, security and maintainability.
o Java defines a new URI scheme for naming modules, classes and resources.
Java 9 Module
Module is a collection of Java programs or software’s. To describe a module, a Java
file module-info.java is required. This file also known as module descriptor and defines
the following
o Module name
o What does it export
o What does it require
Module Name
It is a name of module and should follow the reverse-domain-pattern. Like we name
packages, e.g., com.javatpoint.
How to create Java module
Creating Java module required the following steps.
o Create a directory structure
o Create a module declarator
o Java source code
Create a Directory Structure
To create module, it is recommended to follow given directory structure, it is same as
reverse-domain-pattern, we do to create packages / project-structure in Java.
Note: The name of the directory containing a module's sources should be equal to the
name of the module, e.g. com.javatpoint.
Create a file module-info.java, inside this file, declare a module by
using module identifier and provide module name same as the directory name that
contains it. In our case, our directory name is com.javatpoint.
module com.javatpoint {
}
Leave module body empty, if it does not have any module dependency. Save this file
inside src/com.javatpoint with module-info.java name.
Java Source Code
Now, create a Java file to compile and execute module. In our example, we have
a Hello.java file that contains the following code.
class Hello {
public static void main(String[] args) {
System.out.println("Hello from the Java module");
}
}
Save this file inside src/com.javatpoint/com/javatpoint/ with Hello.java name.
Compile Java Module
To compile the module, use the following command.
1. javac -d mods --module-source-path src/ --module com.javatpoint
After compiling, it will create a new directory that contains the following structure.
Now, we have a compiled module that can be just run.
Run Module
To run the compiled module, use the following command.
1. java --module-path mods/ --module com.javatpoint/com.javatpoint.Hello
Output:
Hello from the Java module
Well, we have successfully created, compiled and executed Java module.
Look inside compiled Module Descriptor
To see the compiled module descriptor, use the following command.
1. javap mods/com.javatpoint/module-info.class
This command will show the following code to the console.
Compiled from "module-info.java"
module com.javatpoint {
 requires java.base;
}
See, we created an empty module but it contains a java.base module. Why? Because all Java
modules are linked to java.base module and it is default module.
Java 9 Private Interface Methods
In Java 9, we can create private methods inside an interface. Interface allows us to declare
private methods that help to share common code between non-abstract methods.
Before Java 9, creating private methods inside an interface cause a compile time error.
The following example is compiled using Java 8 compiler and throws a compile time error.
Note: To implement private interface methods, compile source code using Java 9 or
higher versions only.
Now, lets execute the above code by using Java 9. See the output, it executes fine.
Java 9 Try With Resource Enhancement
Java introduced try-with-resource feature in Java 7 that helps to close resource
automatically after being used.
In other words, we can say that we don't need to close resources (file, connection, network
etc.) explicitly, try-with-resource close that automatically by using AutoClosable interface.
In Java 7, try-with-resources has a limitation that requires resource to declare locally within
its block.
Example Java 7 Resource Declared within resource block
This code executes fine with Java 7 and even with Java 9 because Java maintains its legacy.
But the below program would not work with Java 7 because we can't put resource
declared outside the try-with-resource.
Java 7 Resource declared outside the resource block
If we do like the following code in Java 7, compiler generates an error message.
To deal with this error, try-with-resource is improved in Java 9 and now we can use
reference of the resource that is not declared locally.
In this case, if we execute the above program using Java 9 compiler, it will execute
nicely without any compile error.
Java 9 Anonymous Inner Classes Improvement
Java 9 introduced a new feature that allows us to use diamond operator with anonymous
classes. Using the diamond with anonymous classes was not allowed in Java 7.
In Java 9, as long as the inferred type is denotable, we can use the diamond operator
when we create an anonymous inner class.
Data types that can be written in Java program like int, String etc are called denotable
types. Java 9 compiler is enough smart and now can infer type.
Note: This feature is included to Java 9, to add type inference in anonymous inner
classes.
Let's see an example, in which we are using diamond operator with inner class without
specifying type.
Although we can specify type in diamond operator explicitly and compiler does not
produce any error message. See, the following example, type is specified explicitly.
 ABCD<String> a = new ABCD<String>() // diamond operator is not empty
And we get the same result.
Output:
Java9
Java 9 @SafeVarargs Annotation
It is an annotation which applies on a method or constructor that takes varargs
parameters. It is used to ensure that the method does not perform unsafe operations on
its varargs parameters.
It was included in Java7 and can only be applied on
o Final methods
o Static methods
o Constructors
From Java 9, it can also be used with private instance methods.
Note: The @SafeVarargs annotation can be applied only to methods that cannot be
overridden. Applying to the other methods will throw a compile time error.
Let's see some examples, in first example, we are not using @SafeVarargs annotation
and compiling code
This is a compiler generated warning regarding unsafe varargs type.
To avoid it, we should use @SaveVarargs notation to the method, as we did in the
following example.
Note: To apply @SaveVarargs annotation on private instance methods, compile code
using Java 9 or higher versions only.
Java 9 Factory Methods
Java 9 Collection library includes static factory methods for List, Set and Map interface.
These methods are useful to create small number of collection.
Suppose, if we want to create a list of 5 elements, we need to write the following code.
Factory Methods for Collection
Factory methods are special type of static methods that are used to create unmodifiable
instances of collections. It means we can use these methods to create list, set and map
of small number of elements.
It is unmodifiable, so adding new element will
throw java.lang.UnsupportedOperationException
Each interface has its own factory methods, we are listing all the methods in the following
tables.
Java 9 Set Interface
Java Set interface provides a Set.of() static factory method which is used to create
immutable set. The set instance created by this method has the following characteristics.
o It is immutable
o No null elements
o It is serializable if all elements are serializable.
o No duplicate elements.
o The iteration order of set elements is unspecified and is subject to change.
Java 9 Map Interface Factory Methods
In Java 9, Map includes Map.of() and Map.ofEntries() static factory methods that provide
a convenient way to create immutable maps.
Map created by these methods has the following characteristics.
o It is immutable
o It does not allow null keys and values
o It is serializable if all keys and values are serializable
o It rejects duplicate keys at creation time
o The iteration order of mappings is unspecified and is subject to change.
Java 9 Map Interface ofEntries() Method Example
In Java 9, apart from static Map.of() methods, Map interface includes one more static
method Map.ofEntries(). This method is used to create a map of Map.Entry instances.

Java 9 Stream API Improvement
In Java 9, Stream API has improved and new methods are added to the Stream interface.
These methods are tabled below.
Java Stream takeWhile() Method
Stream takeWhile method takes each element that matches its predicate. It stops when it
get unmatched element. It returns a subset of elements that contains all matched
elements, other part of stream is discarded.
Java Stream takeWhile() Method Example 1
In this example, we have a list of integers and picks up even values by using takewhile
method.
Java Stream dropWhile() Method
Stream dropWhile method returns result on the basis of order of stream elements.
Ordered stream: It returns a stream that contains elements after dropping the elements
that match the given predicate.
Unordered stream: It returns a stream that contains remaining elements of this stream
after dropping a subset of elements that match the given predicate.
Java Stream dropWhile() Method Example
Java 9 Stream ofNullable Method
Stream ofNullable method returns a sequential stream that contains a single element, if
non-null. Otherwise, it returns an empty stream.It helps to handle null stream and
NullPointerException.
Java 9 Stream ofNullable Method Example 1
Java Stream Iterate Method
A new overloaded method iterate is added to the Java 9 stream interface. This method
allows us to iterate stream elements till the specified condition.
It takes three arguments, seed, hasNext and next.
Local Variable Type Inference
Local Variable Type Inference is one of the most evident change to language available
from Java 10 onwards. It allows to define a variable using var and without specifying the
type of it. The compiler infers the type of the variable using the value provided. This type
inference is restricted to local variables.
Old way of declaring local variable.
String name = "Welcome to tutorialspoint.com";
New Way of declaring local variable.
var name = "Welcome to tutorialspoint.com";
Now compiler infers the type of name variable as String by inspecting the value
provided.
Noteworthy points
• No type inference in case of member variable, method parameters, return
values.
• Local variable should be initialized at time of declaration otherwise
compiler will not be infer and will throw error.
• Local variable inference is available inside initialization block of loop
statements.
• No runtime overhead. As compiler infers the type based on value provided,
there is no performance loss.
• No dynamic type change. Once type of local variable is inferred it cannot
be changed.
• Complex boilerplate code can be reduced using local variable type
inference.
Map<Integer, String> mapNames = new HashMap<>();
var mapNames1 = new HashMap<Integer, String>();


Example
Following Program shows the use of Local Variable Type Inference in JAVA 10.
import java.util.List;
public class Tester {
 public static void main(String[] args) {
 var names = List.of("Julie", "Robert", "Chris", "Joseph");
 for (var name : names) {
 System.out.println(name);
 }
 System.out.println("");
 for (var i = 0; i < names.size(); i++) {
 System.out.println(names.get(i));
 }
 }
}
Output
It will print the following output.
Julie
Robert
Chris
Joseph
Julie
Robert
Chris
Joseph
New APIs & Options
APIs to create Unmodifiable Collections
A new method copyOf() is available in List, Set and Map interfaces which can create
new collection instances from existing one. Collector class has new
methods toUnmodifiableList(), toUnmodifiableSet(), and toUnmodifiableMap() to get
elements of a stream into an unmodifiable collection.
Hashed Password
The plain text passwords available in the jmxremote.password file are now being overwritten with their SHA3-512 hash by the JMX agent.
Optional.orElseThrow() Method
A new method orElseThrow() is available in java.util.Optional class which is now a
preferred alternative for get() method.
Java.util.Optional, java.util.OptionalDouble, java.util.OptionalInt
and java.util.OptionalLong each got a new method orElseThrow() which doesn't take any
argument and throws NoSuchElementException if no value is present.
Running Java File with single command
One major change is that you don’t need to compile the java source file with javac tool
first. You can directly run the file with java command and it implicitly compiles.
Java String Methods
isBlank() - This instance method returns a boolean value. Empty Strings and Strings
with only white spaces are treated as blank.
lines() This method returns a stream of strings, which is a collection of all substrings split
by lines.
strip(), stripLeading(), stripTrailing() strip() - Removes the white space from both,
beginning and the end of string.
But we already have trim(). Then what’s the need of strip()? strip() is “Unicodeaware” evolution of trim(). When trim() was introduced, Unicode wasn’t evolved.
Now, the new strip() removes all kinds of whitespaces leading and trailing(check the
method Character.isWhitespace(c) to know if a unicode is whitespace or not).
repeat(int) The repeat method simply repeats the string that many numbers of times as
mentioned in the method in the form of an int.
Local-Variable Syntax for Lambda Parameters
Local-Variable Syntax for Lambda Parameters is the only language feature release in
Java 11. In Java 10, Local Variable Type Inference was introduced. Thus we could infer
the type of the variable from the RHS - var list = new ArrayList<String>(); JEP
323 allows var to be used to declare the formal parameters of an implicitly typed
lambda expression. We can now define :
(var s1, var s2) -> s1 + s2
This was possible in Java 8 too but got removed in Java 10. Now it’s back in Java 11 to
keep things uniform.
But why is this needed when we can just skip the type in the lambda? If you need
to apply an annotation just as @Nullable, you cannot do that without defining the type.
Limitation of this feature - You must specify the type var on all parameters or none.
Things like the following are not possible:
(@NonNull var value1, @Nullable var value2) -> value1 + value2 // Correct one
(var s1, s2) -> s1 + s2 //no skipping allowed
(var s1, String y) -> s1 + y //no mixing allowed
var s1 -> s1 //not allowed. Need parentheses if you use var in lambda.
Nested Based Access Control
Java 11 introduced a concept of nested class where we can declare a class within a class.
This nesting of classes allows to logically group the classes to be used in one place,
making them more readable and maintainable. Nested class can be of four types −
• Static nested classes
• Non-static nested classes
• Local classes
• Anonymous classes
Java 11 also provide the concept of nestmate to allow communication and verification of
nested classes.
Remove the Java EE and CORBA Modules
The modules were already deprecated in Java 9. They are now completely removed.
Following packages are
removed: java.xml.ws, java.xml.bind, java.activation, java.xml.ws.annotation,
java.corba, java.transaction, java.se.ee, jdk.xml.ws, jdk.xml.bind .
Flight Recorder
Flight Recorder which earlier used to be a commercial add-on in Oracle JDK is now
open-sourced since Oracle JDK is itself not free anymore. JFR is a profiling tool used to
gather diagnostics and profiling data from a running Java application. Its performance
overhead is negligible and that’s usually below 1%. Hence it can be used in production
applications.
Reading/Writing Strings to and from the Files
Java 11 strives to make reading and writing of String convenient. It has introduced the
following methods for reading and writing to/from the files:
• readString()
• writeString()
Following code showcases an example of this
Not Predicate
Java 11 introduced new method to Predicate interface as not() to negate an existing
predicate similar to negate method.
HTTP Client
Java 11 standardizes the Http CLient API. The new API supports both HTTP/1.1 and
HTTP/2. It is designed to improve the overall performance of sending requests by a
client and receiving responses from the server. It also natively supports WebSockets.
An enhanced HttpClient API was introduced in Java 9 as an experimental feature. With
Java 11, now HttpClient is a standard. It is recommended to use instead of other HTTP
Client APIs like Apache Http Client API. It is quite feature rich and now Java based
applications can make HTTP requests without using any external dependency.
Steps
Following are the steps to use an HttpClient.
• Create HttpClient instance using HttpClient.newBuilder() instance
• Create HttpRequest instance using HttpRequest.newBuilder() instance
• Make a request using httpClient.send() and get a response object.
File APIs
Java 11 introduced an easy way to read and write files by providing new overloaded
methods without writing much boiler plate code.
Optional Class
Java 11 introduced new method to Optional class as isEmpty() to check if value is
present. isEmpty() returns false if value is present otherwise true.
It can be used as an alternative of isPresent() method which often needs to negate to
check if value is not present.
Consider the following example −
Switch Expressions (Preview)
Java 12 has enhanced Switch expressions for Pattern matching. Introduced as a
preview language feature, the new Syntax is L ->. Following are some things to note
about Switch Expressions:
• The new Syntax removes the need for break statement to prevent fall throughs.
• Switch Expressions don’t fall through anymore.
• Furthermore, we can define multiple constants in the same label.
• default case is now compulsory in Switch Expressions.
• break is used in Switch Expressions to return values from a case itself.
With the new Switch expression, we don’t need to set break everywhere thus prevent logic
errors!
File.mismatch method
Java 12 added the following method to compare two files:
public static long mismatch(Path path, Path path2) throws IOException
This method returns the position of the first mismatch or -1L if there is no mismatch.
Two files can have a mismatch in the following scenarios:
• If the bytes are not identical. In this case, the position of the first mismatching
byte is returned.
• File sizes are not identical. In this case, the size of the smaller file is returned.
Compact Number Formatting
Teeing Collectors
Teeing Collector is the new collector utility introduced in the Streams API. This collector
has three arguments - Two collectors and a Bi-function. All input values are passed to
each collector and the result is available in the Bi-function.
Java Strings New Methods
4 new methods have been introduced in Java 12 which are:
indent(n) method
Adjust the indention of each line of string based on argument passed.
Usage
• n > 0 - insert space at the begining of each line.
• n < 0 - remove space at the begining of each line.
• n < 0 and n < available spaces - remove all leading space of each line.
• n = 0 - no change.
transform(Function<? super String,? extends R> f) method
Transforms a string to give result as R.
Usage
String transformed = text.transform(value -> new StringBuilder(value).reverse().toString());
Optional<String> describeConstable() method
Returns Optional Object containing description of String instance.
Usage
Optional<String> optional = message.describeConstable();
resolveConstantDesc(MethodHandles.Lookup lookup)
method
Returns descriptor instance string of given string.
Usage
String constantDesc = message.resolveConstantDesc(MethodHandles.lookup());
Pattern Matching for instanceof (Preview)
Another Preview Language feature! The old way to typecast a type to another type is:
if (obj instanceof String) {
String s = (String) obj;
// use s in your code from here
}
The new way is :
if (obj instanceof String s) {
 // can use s directly here
}
This saves us some typecasting which were unnecessary.
Text Blocks
This is an example of a preview feature. It makes it simple to construct multiline strings. A
pair of triple-double quotations must surround the multiline string.
There are no additional properties on the string object formed with text blocks. It's a more
convenient approach to make multiline strings. We can't make a single-line string with
text blocks.
A line terminator must follow the initial triple-double quotations.
New Methods in String Class for Text Blocks
The String class now has three additional methods related to the text blocks functionality.
formatted(Object... args) is a function comparable to String format(). It's there to help
with text block formatting.
stripIndent() is a function that removes the white space characters at the start and end
of each line in a text block. The text blocks employ this mechanism to preserve the relative
indentation of the content.
translateEscapes() It returns a string containing the value this string, with escape
sequences translated as if they were in a string literal.
Switch Expressions Enhancements
In the 12 release of Java, switch expressions were added as a trial feature. The only
difference is that "break" has been replaced with "yield" to return a value from the case
statement in Java 13.
Reimplement the Legacy Socket API
The underlying implementation of the java.net.Socket and java.net.ServerSocket APIs
has been updated in Java version 13. NioSocketImpl, the new implementation, is a dropin replacement for PlainSocketImpl.
Instead of synchronized methods, it employs java.util.concurrent locks. Utilize the java
option -Djdk.net.usePlainSocketImpl if we want to use the legacy implementation.
