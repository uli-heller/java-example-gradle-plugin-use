Using Gradle Plugins
====================

Note: This sample project came into existence when
I tried to do some experiments with the plugin ["Nebula Dependency Lock"](https://plugins.gradle.org/plugin/nebula.dependency-lock).
In the meantime, I'm pretty sure that I do NOT need that specific plugin at
all. So the purpose of this sample project is to illustrate different ways to use
plugins within gradle projects.

Use Standard Plugins
--------------------

build.gradle:

```
plugins {
  id "nebula.dependency-lock" version "2.2.4"
}
```

This is the recommended way to use a plugin. The plugin has to be available
via the standard plugin portal.
