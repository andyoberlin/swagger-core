# Swagger Playframework Sample App

## Overview
This is a scala project to build a stand-alone server which implements the Swagger spec.  You can find out 
more about both the spec and the framework at http://swagger.wordnik.com.  For more information 
about Wordnik's APIs, please visit http://developer.wordnik.com.  There is an online version of this
server at http://petstore.swagger.wordnik.com/api/resources.json

### To build from source
Please follow instructions to build the top-level [swagger-core project](https://github.com/wordnik/swagger-core)

### To run
The swagger-play2 module lives in maven central:

```scala
  val appDependencies: Seq[sbt.ModuleID] = Seq(
    /* your other dependencies */
    "com.wordnik" %% "swagger-play2" % "1.2.0")

  val main = PlayProject(appName, appVersion, appDependencies, mainLang = JAVA).settings(
    "sonatype-releases" at "https://oss.sonatype.org/content/repositories/releases",
    /* your other resolvers */
    )
}
```

then you can build the sample app:

````
play run
````

The application will listen on port 9000 and respond to `http://localhost:9000/api-docs.json`
