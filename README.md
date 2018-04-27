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

Then simply run (`ant all`,) `ant dist`, `ant install`.

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
None left!

# Todo
- Read up on JavaServer Page (JSP).
- Read up on ServletContext.
- Read up on ServletConfig.
- Implement a Front Controller Pattern Servlet.
    - http://www.baeldung.com/java-front-controller-pattern