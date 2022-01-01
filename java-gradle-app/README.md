##### build the project

    ./gradlew build

##### build Docker image called java-app. Execute from root

    docker build -t java-app .
    
##### push image to repo 

    docker tag java-app demo-app:java-1.0
    

### Changes
[23.Aug.2021]

Gradle wrapper version upgraded from version 6.x to 7.0 
        
###### This will change the version in wrapper.settings

     ./gradlew wrapper --gradle-version 7.0

###### This will update the complete wrapper and download version 7.0 jar

     ./gradlew wrapper --gradle-version 7.0

In build.gradle file, replace:
- compile with implementation 
- testCompile with testImplementation

Because, version 7.0 removed compile and testCompile configurations.
Source: https://docs.gradle.org/current/userguide/upgrading_version_6.html#sec:configuration_removal