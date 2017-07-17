# Tsmart-DATE
A dynamic program analysis tool for Java programs.

### Dependency
Make sure Java/JDK (1.7 or later) is installed and $JAVA_HOME environment variable is correctly set.

### Usage
```sh
$ cd Tsmart-DATE
$ java -javaagent:build/jar/rragent.jar -Xbootclasspath/p:classes.jar:jars/java-cup-11a.jar: rr.RRMain -classpath=benchmarks/ -tool=PCT:FT2 -noxml -quiet -stacks account.Account
```

Tsmart-DATE should report a set of data race errors ("FastTrack Error"). The detailed output will be logged into log/log.xml.
To analyze other Java programs, please replace "account.Account" above with the class name.

### Directory Structure
* README.md: this file.
* msetup: a script to set up environment variables.
* benchmarks/: the benchmark directory
* test/: the test directory
