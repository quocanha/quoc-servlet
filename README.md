# About
An educational, experimental implementation of a Java servlet using the Apache 
Tomcat implementation, with Ant as the build system.

The content contains paraphrasing of the links issued below, since those have
been taken for reference.

By Quoc An Ha.

# Usage
Make sure both Tomcat and Ant are installed. Include the jar under 
`${CATALINA_HOME}/lib/servlet-api.jar` into the classpath (this file is normally 
part of Java EE).

## Ant command
To clean

```
ant clean
```

To build

```
ant compile
```

To clean & build

```
ant all
```

To deploy

```
ant install
```

To undeploy

```
ant undeploy
```

To reload

```
ant reload
```

Refer to the `build.xml` file for more information.

# Links
- https://tomcat.apache.org/tomcat-9.0-doc/index.html
- https://www.ntu.edu.sg/home/ehchua/programming/java/JavaServlets.html

## Problems
### Ant install with Tomcat provided build.xml
When running `ant install`, I'm getting the following error:
```
INFO: Manager: install: Installing web application '/test' from 'file:///path/to/quoc-servlet/build'
      jsvc.exec[584]: java.io.FileNotFoundException: /path/to/quoc-servlet/build (Permission denied)
``` 
Which is explained here:

https://stackoverflow.com/questions/3579626/ant-install-to-deploy-tomcat-webapp-failing-with-permission-problem

But I'm unsure about what normal behaviour would be, since changing the 
${build.home} permissions to 777 does not work, even though I would think
that would allow Tomcat to access the build folder.

Deploying the war file manually within the Tomcat manager works as intended 
though.

### Ant install does not work
I posted a stackoverflow question regarding this.