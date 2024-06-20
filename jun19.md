philosophy: read everything, only take notes on things i’m not familiar with

practice a lot, answer a lot of questions

**chapter 1: welcome to java**

intro

1. Java Development Kit (JDK) 
    1. contains min software for java development
2. Compiler (javac)
    1. converts .java files to .class files
3. Launcher java
    1. creates virtual machine, executes program
4. Others?
    1. Archiver (jar) + API documentation (javadoc) for generating documentation
5. javac generates instructions called bytecode (.class) which can then be run by the JVM
6. JRE: used to be subset of JDK (only for compiling). No longer exists

benefits of java

1. OOP, encapsulation, platform independent, robust (no memory leaks + java garbage collection), simpler (no pointers + operator overloading), secure (code only runs in jvm), multithreaded, backwards compatible (usually)

class structure

1. object = runtime instance of class, aka instance
2. reference = variable that points towards a class
3. members = methods + fields (aka variables)
4. you can put two classes in the same file, at most one is allowed to be public. public classes much match file name.

```jsx
public class ZOO {
	public static void main(String[] args){
			// the rest of your code
	}
}
```

1. run the above code with javac [Zoo.java](http://Zoo.java) (to compile it), followed by java Zoo (to run it)

```jsx
String[] args is most common, but 
String args[] and
String... args

are all allowed.
```

1. summary: jdk contains a compiler, java class files run on JVM (run on any machine with java, not just the compiled machine)
2. one-line compilation with java [Zoo.java](http://Zoo.java) compiles the program in memory, and only worksfor programs with one file.

packages

1. packages are like a mailbox, tell jvm where to grab your imports
2. java.lang.System and java.lang are automatically imported.
3. package comes before import. package → import → class → variable

options

`javac`

1. -cp <classpath> or classpath<classpath> or `--class-path` <classpath> (location of classes needed to compile program)
2. -d <dir> (directory to place generated class files)

`java`

1. -cp <classpath> or classpath<classpath> or `--class-path` <classpath> (location of classes needed to **run** program)

`jar`

1. -c or `--create` creates a new jar file
2. -v or `--verbose` prints jar file details
3. -f <filename> or `--file` <fileName> (JAR filename)
4. -C <directory> (directory containing files to be used to create the JAR)

**chapter 2: java building blocks**

- constructors have the same name of the class, and they make objects (which are an instance of the class)
- they have no return type:

```java
public class Chick {
	public void Chick(){} // not a constructor
	public Chick(){} // constructor
}
```

- instance initializers: code blocks that appear outside of a method
- running order:
    1. fields and instance initalizers
    2. constructor
    3. main method
- Eight primitive types: boolean, byte (-128 to 127), short, int, long, float, double, char
    - not strin
    - float has f at end (123.45f), long has L at end (12345L)
    - char and short are intechangeable, but there are restrictions. chars can’t be negative number.
- numeric literals:
    
    ```java
    long max = 3123456789 // does not compile
    long max = 3123456789L // compiles
    ```
    
- you can add underscores to literals!

```java
int million1 = 1000000;
int million2 = 1_000_000;
double notAtStart = _1000.00 // does not compile
double notAtEnd = 1000.00_
```
