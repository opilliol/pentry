# Gradle

## Define configuration
to work with java:

```
apply plugin: 'java'
```

Define the java version involved

```
java {
    toolchain {
        languageVersion = JavaLanguageVersion.of(25)
    }
}
```

Define the version of Gradle to use

```
wrapper {
    gradleVersion = "9.2.1"
    distributionType = Wrapper.DistributionType.ALL
}
```

Define the tasks

```
tasks.register('distclean') {
    doLast {
        println 'Dist Cleaning'
    }
}

tasks.register('package') {
    doLast {
        println 'Packaging'
    }
}
```

## Generate the wrapper
```bash
gradle wrapper
```
