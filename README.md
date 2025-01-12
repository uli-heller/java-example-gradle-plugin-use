Using Gradle Plugins
====================

Note: This sample project came into existence when
I tried to do some experiments with the plugin ["Nebula Dependency Lock"](https://plugins.gradle.org/plugin/nebula.dependency-lock).
In the meantime, I'm pretty sure that I do NOT need that specific plugin at
all. So the purpose of this sample project is to illustrate different ways to use
plugins within gradle projects.

Use Standard Plugins
--------------------

[Locking Dependency Versions in Gradle](https://jkutner.github.io/2017/03/29/locking-gradle-dependencies.html)

build.gradle:

```
plugins {
  id "nebula.dependency-lock" version "2.2.4"
}
```

This is the recommended way to use a plugin. The plugin has to be available
via the standard plugin portal.

An Updated Version
------------------

[plugins.gradle.org - nebula.dependency-lock](https://plugins.gradle.org/plugin/nebula.dependency-lock)

build.gradle:

```
plugins {
  id("nebula.dependency-lock") version "12.7.1"
}
```

Plugin Hosted On Github - Version 4.+
-------------------------------------

[https://github.com/nebula-plugins/gradle-dependency-lock-plugin - Usage - example](https://github.com/nebula-plugins/gradle-dependency-lock-plugin/wiki/Usage#example)

build.gradle:

```
buildscript {
    repositories {
        mavenLocal()
        jcenter()
    }

    dependencies {
        classpath 'com.netflix.nebula:gradle-dependency-lock-plugin:4.+'
    }
}
apply plugin: 'nebula.dependency-lock'

...
```

Plugin Hosted On Github - Latest Version 15.+
---------------------------------------------

[Github - gradle-dependency-lock-plugin](https://github.com/nebula-plugins/gradle-dependency-lock-plugin)


```
buildscript {
    repositories {
        mavenLocal()
        jcenter()
    }

    dependencies {
        classpath 'com.netflix.nebula:gradle-dependency-lock-plugin:15.+'
    }
}
apply plugin: 'com.netflix.nebula.dependency-lock'
...
```
