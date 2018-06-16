This repository is part of a [series of Java tutorials for a Rational class](https://ucsb-cs56-pconrad.github.io/tutorials/rational/) written by [Phill Conrad](https://www.cs.ucsb.edu/~pconrad) for [CMPSC 56](ucsb-cs56-pconrad.github.io), a Java course taught in the [Dept. of Computer Science](https://www.cs.ucsb.edu) at [UC Santa Barbara](https://www.ucsb.edu).

# For detailed instructions, see:

* https://ucsb-cs56-pconrad.github.io/tutorials/rational/
* https://ucsb-cs56-pconrad.github.io/tutorials/rational_ex02/

# Quick start

Once you clone this repo, these commands show how to compile and run the code inside.

In the previous lessson, [ex01](https://ucsb-cs56-pconrad.github.io/tutorials/rational_ex01/), we used simple Java `javac` and `java` commands to compile and run.   In this lesson, we use a tool called [`ant`](http://ucsb-cs56-pconrad.github.io/topics/ant/).    

* If you are using [CSIL](https://ucsb-cs56-pconrad.github.io/topics/csil/), then `ant` should already be installed.
* If you are using your own computer system, you may need to install `ant`.  Refer to the article on [`ant`](http://ucsb-cs56-pconrad.github.io/topics/ant/) for more information.

Here are example commands to compile and run the code in this repo:

Run `ant compile` to compile the code:

```
-bash-4.3$ ls
build.xml  Main.java  Rational.java  README.md
-bash-4.3$ ant compile
Buildfile: /cs/faculty/pconrad/github/cs56-rational-example/ex02/build.xml

compile:
    [javac] Compiling 2 source files to /cs/faculty/pconrad/github/cs56-rational-example/ex02

BUILD SUCCESSFUL
Total time: 0 seconds
-bash-4.3$ ls
build.xml  Main.class  Main.java  Rational.class  Rational.java  README.md
-bash-4.3$
```

Run `ant run` to run the main from the Rational class (that's what we specified in the target):

```
-bash-4.3$ ant run
Buildfile: /cs/faculty/pconrad/github/cs56-rational-example/ex02/build.xml

run:
     [java] r.getNumerator()=5
     [java] r.getDenominator()=7

BUILD SUCCESSFUL
Total time: 0 seconds
-bash-4.3$
```

To run the other `main`, since it takes command line parameters, it is
better to run it interactively the "old fashioned way".  

```
-bash-4.3$ java Main
Usage: java Main int denom
  int and denom should be integers; denom may not be zero.
  -bash-4.3$ java Main 2 7
  r1 = 1/1
  r2 = 2/7
  -bash-4.3$
```

To clean up, we type `ant clean`

```
-bash-4.3$ ls
build.xml  Main.class  Main.java  Rational.class  Rational.java  README.md
-bash-4.3$ ant clean
Buildfile: /cs/faculty/pconrad/github/cs56-rational-example/ex02/build.xml

clean:

BUILD SUCCESSFUL
Total time: 0 seconds
-bash-4.3$ ls
build.xml  Main.java  Rational.java  README.md
-bash-4.3$
```
