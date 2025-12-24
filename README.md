Highly opinionated parent POM for my projects.

## Usage
### Requirements

1. Sources are self-documented and small. Read them.
2. You need to copy jvm.config from .mvn/ to your project thanks to brian goetz and maven bug that loses compilation failure messages in certain conditions.

## Build/installation

### Build requirements

- JDK 21
- Maven 3

### Command

`mvn clean install`

## Some configurations documentation

### maven.config property ```extended``` of ```boolean```

Should apply extended profile (add additional libraries)?

Default: true

### ```<properties>``` property ```java.version``` of ```java release version```

Default: 21

### CLI property ```-Drelease``` of ```boolean```

Should enforcer, jacoco and other slow tasks that are not needed with fast
testing cycle run?

Default: true

### ```<properties>``` properties of dependencies (plugins, maven dependencies) versions

Default: latest stable (selected&updated, not LATEST/RELEASE)
