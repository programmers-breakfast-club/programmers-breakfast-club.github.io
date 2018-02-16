---
layout: single
title: What is... Java? 
permalink: /articles/what-is-java
excerpt: "Java is considered the most popular programming language, but, what is it?"
share: false
---
[Java](https://java.com) is considered the most popular programming language by more than a few metrics.  It's an open source language used everywhere from laptops, to datacenters, to game consoles, to cell phones.

It was developed at Sun Microsystems by James Gosling and first released in 1995. 

The Java programming language is just one part of what is considered the Java platform.  The other major component is the Java Virtual Machine which is what actually runs and executes compiled Java code, or Java bytecode.  The key point of this platform is that any combination of hardware and operating system that has an implementation of the JVM can run Java code.

### Who uses Java?
Because of how widely Java is used, almost all sorts of programmers might use Java.  Game developers, hardware developers, and it's used in almost all parts of the industry.  Wikipedia cites that Java is in use by over 9 million developers.

### How is Java code written?
#### HelloWorld.java
```java
    public class HelloWorld {
      public static void main(String[] args) {
        System.out.println("Hello, World");
      }
    }
```


### Sample Java Code demonstrating Interfaces by Adrian David
```java
import static java.lang.System.out;

@FunctionalInterface
interface ITest {
    public abstract double doMath (double x, double y);
    static void doStat() { out.println("This is a Static Interface Method.\n");}
    default void doDefault() { out.println("This is a Default Interface Method."); doPrivate(); }
    private void doPrivate () { out.println("This is a Private Interface Method (Java 9+)."); }
}

public class Test {
    public static void main (String ... args) {
        Double[] operands = new Double[2];
        try { 
            operands[0] = Double.parseDouble(args[0]);
            operands[1] = Double.parseDouble(args[1]);
        } 
        catch (ArrayIndexOutOfBoundsException ne) 
        { out.println("You have not specified enough operands."); return; }

        catch(Exception e) 
        { out.println("Something has gone wrong.\n" + e + "."); return;}

        ITest it = new ITest() { public double doMath(double x, double y) { out.println(); return Math.pow(x,y); }; };
        out.println("This is an Anonymous Class implementing an Interface.\n" +
                    "This is the Arg I to power of Arg II:\t" + it.doMath(operands[0], operands[1]) + "\n");
        it.doDefault();
        ITest.doStat();

        ITest add = (x,y) ->  x + y;
        out.println("Lambda Addition:\t" + add.doMath(operands[0], operands[1]) );

        ITest divide = (x,y) ->  x / y;
        out.println("Lambda Division:\t" + divide.doMath(operands[0], operands[1]) );

        ITest subtract = (x,y) ->  x - y;
        out.println("Lambda Subtratcion:\t" + subtract.doMath(operands[0], operands[1]) );

        ITest multiply = (x,y) ->  x * y;
        out.println("Lambda Multiplication:\t" + multiply.doMath(operands[0], operands[1]) );
    }
}
```

### Why Java?
There's as many reasons to use Java as there are platforms that support it.   It's mature, been around and is well passed the usual hype train that boosts a language and then leaves it behind.  There's lots of resources, both free and paid for learning Java and there's typically lots of job opportunities if that's something you're after.

### Where can read more or learn more about Java?


#### Wikipedia
* [Java](https://en.wikipedia.org/wiki/Java_(programming_language))
* [Java Virtual Machine](https://en.wikipedia.org/wiki/Java_virtual_machine)


#### Books
* [Learn Java Programming with examples](https://beginnersbook.com/java-tutorial-for-beginners-with-examples/)
* [Head First Java](https://www.amazon.com/Head-First-Java-Kathy-Sierra/dp/0596009208)
* [Head First Design Patterns](https://www.amazon.com/Head-First-Design-Patterns-Brain-Friendly/dp/0596007124)

#### Awesome Java
* <https://java.libhunt.com/>
* <http://java-lang.github.io/awesome-java/>
* <https://github.com/wtsxDev/Amazing-Java-List>
* <https://github.com/pditommaso/awesome-java>
* <https://github.com/uhub/awesome-java>
* <https://github.com/akullpp/awesome-java>

#### Exercism
* [exercism - java](http://exercism.io/languages/java/about)

#### Places to Learn
* [Learn X in Y Minutes](https://learnxinyminutes.com/docs/java/)
* [SoloLearn](https://www.sololearn.com/Course/Java/)

#### Relevant subreddits
* [/r/java](https://www.reddit.com/r/java/)
* [/r/learnjava](https://www.reddit.com/r/learnjava/)

#### Oracle Resources and Java API Documentation
* <http://www.oracle.com/technetwork/topics/newtojava/overview/index.html>
* <http://www.oracle.com/technetwork/java/api-141528.html>
* <https://docs.oracle.com/javase/9/>

#### Podcasts
* [Java Pub House](http://javapubhouse.libsyn.com/)

