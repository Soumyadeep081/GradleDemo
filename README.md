## Setup of basic gradle using CLI

```bash
gradle init --use-defaults --type java-application
The above command will set up a basic Gradle project.

bash
Copy code
./gradlew build
To prepare a JAR which is executable, you need to set up the manifest property in build.gradle to identify what is the main class to execute.

groovy
Copy code
jar {
    manifest {
        attributes(
            'Main-Class': 'org.example.Main'
        )
    }
}
The above configuration allows Gradle to build an executable JAR.

bash
Copy code
./gradlew jar
The above command creates a new JAR file in the build/libs folder.

bash
Copy code
java -jar build/libs/filename.jar
The above command will execute your code.

yaml
Copy code
