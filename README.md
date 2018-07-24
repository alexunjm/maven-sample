# maven-sample
playing with maven

1. adding minimal POM file to project

## commands
mvn compile (after create pom.xml)

2. folder structure

## commands
mkdir -p src/main/java
mkdir -p src/main/resources

mkdir -p src/test/java
mkdir -p src/test/resources

## adding empty files to keep folders in place
touch src/main/java/.gitkeep
touch src/main/resources/.gitkeep

touch src/test/java/.gitkeep
touch src/test/resources/.gitkeep

3. java files and packages

## commands
cd src/main/java
mkdir -p com/sample/training

code Application.java
### root folder
mvn package

4. execute class from package

## commands
cd target
java -cp example-1.0.jar com.sample.training.Application
