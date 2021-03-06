This directory contains source code that is not part of the Apache
Commons RNG library.  It contains syntactically correct and working
examples of use.

In order to run one of the applications (a class that must contain a
"main" method), you would type (in a shell console) a command similar
to the following:
 $ mvn -q exec:java \
   -Dexec.mainClass=org.apache.commons.rng.userguide.RandomStressTester \
   -Dexec.args="[args]"

Alternatively, a "standalone" JAR can be created with the following
command:
 $ mvn -Dmainclass=org.apache.commons.rng.userguide.RandomStressTester \
       -Djarbasename=RandomStressTester \
       clean compile assembly:single
where the value of the "mainclass" argument is the fully-qualified name
of the class whose "main" method will be the program's entry point, and
the "jarbasename" argument is the basename of the JAR file to be created.
Then, the application can be run with the following command:
 $ java -jar RandomStressTester [args]
where "[args]" is the list of arguments passed to the "main" method.
