jalleg Runtime Package
======================

This repository builds a JAR with the pre-built Windows 64-bit Allegro monolith
library in the layout expected for JNA auto-loading. To use this with jalleg,
just include the JAR as a dependency and it will be automatically loaded when
running on 64-bit JVM in Windows.

A 32-bit version is easily possible, and can be included if there are any
requests.

Currently, it is not expected that there can be a version to load on Linux
platforms as there is no known static build of Allegro for Linux (i.e. only
that links dynamically only to glibc), but if one exists it can easily be
packaged as well.

The current version of Allegro included is 5.2.1. The library is downloaded
from http://download.gna.org/allegro/allegro-bin/5.2.1/allegro-mingw-gcc5.3.0-x64-5.2.1.zip

The latest release on Maven Central is 0.1, which actually corresponds to Allegro 5.2.0.
Future versions will match Allegro's version. To use the currently released version:

Maven:
```xml
<dependency>
  <groupId>org.gillius</groupId>
  <artifactId>jalleg-rt-win32-x86-64</artifactId>
  <version>0.1</version>
</dependency>
```

Gradle:
```groovy
dependencies {
    compile 'org.gillius:jalleg-rt-win32-x86-64:0.1'
}
```
