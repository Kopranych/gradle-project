gradle init
    base
    groovy

gradle tasks

files
    build.gradle - build script
    gradlew - for linux macOs how to install application
    gradlew.bat - for windows
    .gitignore - ignore files and folders for git

main components
    projects - container of everything knows about project
    build scripts - tell gradle information about application and how build them
    tasks - individual build actions run command line
    plugins - run tasks with automate mode
        java plugin - automately to compile, test, and package application

groovy language for writing build scripts for gradle

building java application
    gradle expect java classes on
        src/main/java

add java plugin to build script 
``
plugins {
    id 'java' //добавили плагин java для сборки java приложения
}
``
gradle build

add
```
jar {
    manifest {
        attributes 'Main-Class': 'com.kopranych.GradleProject'
    }
}
```

gradle build

java -jar build/libs/gradle-project.jar

testing

add dependencies

```
dependencies {
    testImplementation group: 'junit', name: 'junit', version: '4.13.2'
}
```

gradle build