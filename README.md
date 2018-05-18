There are some useful scripts for java-based application running on Linux system.

## show-busiest-java-threads
The script can find the highest cpu consumed threads in java processus by using combination of **ps** and **jstack** command.
Usage:
./show-busiest-java-threads -p ${pid} －c ${number_of_line}
```
Ex:
sh show-busiest-java-threads.sh -p 7579 -c 2
The stack of busy(%) thread(7587/0x1da3) of java process(7579) of user ():
"C2 CompilerThread0" daemon prio=10 tid=0x00007f0fac09b800 nid=0x1da3 waiting on condition [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

The stack of busy(%) thread(7588/0x1da4) of java process(7579) of user ():
"C2 CompilerThread1" daemon prio=10 tid=0x00007f0fac09d800 nid=0x1da4 waiting on condition [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE
```

## find-in-jar
The script can look for .class files in jar files.
```
Ex:
sh find-in-jar.sh Strings
./guava-18.0.jar
     3986  08-25-2014 14:48   com/google/common/base/Strings.class
./javax.servlet-api-3.0.1.jar
     2799  07-12-2011 13:10   javax/servlet/LocalStrings_fr.properties
     3401  07-12-2011 13:10   javax/servlet/http/LocalStrings_es.properties
     3360  07-12-2011 13:10   javax/servlet/http/LocalStrings_fr.properties
     4062  07-12-2011 13:10   javax/servlet/http/LocalStrings_ja.properties
     3514  07-12-2011 13:10   javax/servlet/http/LocalStrings.properties
     2834  07-12-2011 13:10   javax/servlet/LocalStrings_ja.properties
     2864  07-12-2011 13:10   javax/servlet/LocalStrings.properties
./thirdparty-combined.jar
      345  01-11-2002 21:34   org/apache/struts/action/LocalStrings.properties
      687  01-11-2002 21:34   org/apache/struts/actions/LocalStrings.properties
     1488  01-11-2002 21:34   org/apache/struts/taglib/LocalStrings.properties
      958  01-11-2002 21:34   org/apache/struts/taglib/bean/LocalStrings.properties
     2234  01-11-2002 21:34   org/apache/struts/taglib/html/LocalStrings.properties
      811  01-11-2002 21:34   org/apache/struts/taglib/logic/LocalStrings.properties
      731  01-11-2002 21:34   org/apache/struts/util/LocalStrings.properties
     1135  08-31-2009 14:05   org/apache/xalan/lib/ExsltStrings$DocumentHolder.class
     4265  08-31-2009 14:05   org/apache/xalan/lib/ExsltStrings.class

```
