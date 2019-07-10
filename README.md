# Maven WildFly Profiles Issue

This project documents an issue that happens when you try to use the Maven WildFly plugin and provide the WildFly directory with property files.

Our goal is to make `mvn wildfly:run` work and correctly launch the WildFly server specified in the `local.properties` file. 

The issue is that this value will not get picked up with `mvn wildfly:run` but will get picked up with `mvn package wildfly:run`. 

You can see the WildFly instance the build uses by looking at the value of `JBOSS_HOME` in the terminal output.
- What We Want: `/Users/snowyCoderGirl/IdeaProjects/maven-wildfly-profiles-issue/wildfly-8.2.0.Final`
- What We Are Getting: `/Users/snowyCoderGirl/IdeaProjects/maven-wildfly-profiles-issue/target/wildfly-17.0.1.Final`