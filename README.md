Java TPC-C for InterSystems Caché
==========

This project is a Java implementation of the TPC-C benchmark for InterSystems Caché.

=========
Install JAVA And Maven
=========
yum install java

yum install maven


=========
Compiling
=========

Use this command to compile the code and produce a fat jar.

```
mvn package assembly:single
```

========
Config Database Database
========

modify file tpcc.properties, change the database connection info , like the follows: 
![image](https://github.com/user-attachments/assets/91d3b0b2-f7de-4ef7-9bba-61bd14d3fe3f)


=====
Generating and loading TPC-C data
====


In `tpcc.properties` set the MODE to JDBC.

To run the load process:

```
java -classpath target/tpcc-1.0.0-SNAPSHOT-jar-with-dependencies.jar com.codefutures.tpcc.TpccLoad
```


====
Running the TPC-C Benchmark
====

change the TPC-C settings in `tpcc.properties` of connections and duration(according by your environment) , then run this command To run the tpcc benchmarks:

![image](https://github.com/user-attachments/assets/be4c943c-eda6-4169-b99c-b0df85de7924)


```
java -classpath target/tpcc-1.0.0-SNAPSHOT-jar-with-dependencies.jar com.codefutures.tpcc.Tpcc
```

![image](https://github.com/user-attachments/assets/95a436ff-94fd-4014-992b-cfb7458565f1)



Bugs can be issue to me.
