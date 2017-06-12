# What's this?

This is a tiny Java client that is able to query the job status from a Jenkins server and switch a TP-Link HS100/HS110 Wifi plug on or off according to the build status. If at least one build is in the 'failed' state, the plug will be switched on.

# Building

To build you will need Maven 3.x and JDK 1.8

Just run

```
mvn clean package
```
and you should find a self-executable JAR inside the target folder.

# Running

```
java -jar target/tphs100-client.jar [-d|--debug] [-v|--verbose] [--jenkinshost <hostname>] [--jenkinsuser <username>] [--jenkinspwd <password>] <plug IP/hostname> <on|off|info|jenkins>
```

Option         Description           
------         -----------           
-d                                   
--debug        enable debug output   
-h                                   
--help         displays this help    
--jenkinshost  Jenkins username      
--jenkinspwd   Jenkins password      
--jenkinsuser  Jenkins server IP/name
-v                                   
--verbose      enable verbose output
