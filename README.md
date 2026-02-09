## Setup of basic gradle using cli:

```bash
gradle init --use-defaults --type java-application
```
The above command will setup a basic gradle project
```bash
./gradlew build
```
To prepare a jar which is executable, you need to setup manifest property in build.gradle to identify what is the main 
class to execute
```bash
jar {
    manifest {
        attributes(
            'Main-Class': 'org.example.Main'
        )
    }
}
```
The above command can build your project
```bash
./gradlew jar
```
The above command creates a new jar files in build/libs folder
```bash
java -jar build/libs/filename.jar
```
The above command will execute your code
