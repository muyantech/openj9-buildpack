# OpenJ9 Buildpack

This is a custom buildpack used by [LCDP.ai low code development platform](https://lcdp.ai)

It has much lower memory footprint compared to the default Heroku OpenJDK buildpack.

This is a custom buildpack of [AdoptOpenJDK Buildpack](https://github.com/jkutner/adoptopenjdk-buildpack) which installs the [Eclipse OpenJ9 VM](https://www.eclipse.org/openj9) [AdoptOpenJDK11](https://adoptopenjdk.net/?variant=openjdk11&jvmVariant=openj9).

# Usage
Replace the default Heroku Java buildpack

```
$ heroku buildpacks:set https://github.com/maatuss/openj9-buildpack.git 
$ heroku buildpacks:add heroku/java  
$ git push heroku master
```

# Customizing

Create a file
**system.properties**
at the root of your project

```
adoptopenjdk.version=<version>  
adoptopenjdk.release=<release>
```  

# License
MIT
