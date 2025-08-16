Highly opinionated parent POM for my projects.

## Usage
While maven is an awesome tool, sometimes its declarative approach fails. If you are creating parent POMs that are child to puklapom, you need to declare that they are, in fact, parent, by placing file (content does not matter) .parent in .mvn/ near every your parent POM. Currently, this will disable dependency reduction for maven shade plugin. Reasoning can be found in puklapom-base pom.xml in "parent-itself-settings" profile.