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

The current version of Allegro included is 5.2.3. The library is downloaded
from https://github.com/liballeg/allegro5/releases/download/5.2.3.0/allegro-x86_64-w64-mingw32-gcc-7.2.0-posix-seh-static-5.2.3.1.zip
Although the file version is 5.2.3.1, the release tag and documented version on
the website is 5.2.3, so I have called this release 5.2.3.

The latest release on Maven Central is 5.2.3, corresponding to the Allegro release 5.2.3.

Maven:
```xml
<dependency>
  <groupId>org.gillius</groupId>
  <artifactId>jalleg-rt-win32-x86-64</artifactId>
  <version>5.2.3</version>
</dependency>
```

Gradle:
```groovy
dependencies {
    compile 'org.gillius:jalleg-rt-win32-x86-64:5.2.3'
}
```

A previous version 0.1 was published that corresponded to Allegro version 5.2.0.
All future releases will follow the version of Allegro.
