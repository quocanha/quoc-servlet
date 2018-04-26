# About
An educational, experimental implementation of a Java servlet using the Apache 
Tomcat implementation.

The content contains paraphrasing of the official Tomcat docs as a way to 
remember the content better.

# Author
By Quoc An Ha.

## Problems
When running `ant install`, I'm getting the following error:
```
INFO: Manager: install: Installing web application '/test' from 'file:///path/to/quoc-servlet/build'
      jsvc.exec[584]: java.io.FileNotFoundException: /path/to/quoc-servlet/build (Permission denied)
``` 
Which is explained here:

https://stackoverflow.com/questions/3579626/ant-install-to-deploy-tomcat-webapp-failing-with-permission-problem

But I'm unsure about what normal behaviour would be, since changing the 
${build.home} persmissions to 777 does not work, even though I would think
that would allow Tomcat to access the build folder.

Deploying the war file manually within the Tomcat manager works as intended 
though.