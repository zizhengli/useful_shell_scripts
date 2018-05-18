There are some useful scripts for java-based application running on Linux system.

## show-busiest-java-threads
The script can find the highest cpu consumed threads in java processus by using combination of **ps** and **jstack** command.
Usage:
./show-busiest-java-threads -p java pid －c number of line to display
Ex:
```
[opentext@mshs-w4-dev-cds1 test]$ sh show-busiest-java-threads.sh -p 7579 -c 2
The stack of busy(%) thread(7587/0x1da3) of java process(7579) of user ():
"C2 CompilerThread0" daemon prio=10 tid=0x00007f0fac09b800 nid=0x1da3 waiting on condition [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE

The stack of busy(%) thread(7588/0x1da4) of java process(7579) of user ():
"C2 CompilerThread1" daemon prio=10 tid=0x00007f0fac09d800 nid=0x1da4 waiting on condition [0x0000000000000000]
   java.lang.Thread.State: RUNNABLE
```
