Highly opinionated parent POM for my projects.

## Usage
### Requirements

1. Sources are self-documented and small. Read them.
2. While maven is an awesome tool, sometimes its declarative approach fails. If you are creating parent POMs that are child to puklapom, you need to declare that they are, in fact, parent, by placing file (content does not matter) .parent in .mvn/ near every your parent POM. Currently, this will disable dependency reduction for maven shade plugin. Reasoning can be found in puklapom-base pom.xml in "parent-itself-settings" profile.

### Build

### System requirements

- JDK 21
- Maven 3

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