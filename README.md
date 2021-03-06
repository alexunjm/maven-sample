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

5. clean workspace

## commands

mvn clean

6. clean workspace and generate again target folder with package (multiple goals)

## commands

mvn clean package

7. install package as caché on ~/.m2

## commands

mvn clean install

ls -la ~/.m2/repository/com/sample/example/1.0/

8. java 1.8 compiler

## pom.xml
<code>
  <build>
    <plugins>
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-compiler-plugin</artifactId>
        <version>3.7.0</version>
        <configuration>
          <source>1.8</source>
          <target>1.8</target>
        </configuration>
      </plugin>
    </plugins>
  </build>
</code>

9. adding dependencies

## search maven center

[search.maven.org] (https://search.maven.org/#search%7Cga%7C1%7Ccommons-lang3)

### dependency information

<code>
  <dependencies>
    <dependency>
      <groupId>org.apache.commons</groupId>
      <artifactId>commons-lang3</artifactId>
      <version>3.7</version>
    </dependency>
  </dependencies>
</code>

10. validate dependency list

## commands

mvn dependency:tree

mvn dependency:tree > dependency-list.txt

11. junit

search junit

### add to dependency scope test

<code>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>4.12</version>
      <scope>test</scope>
    </dependency>
</code>

## commands

mvn test

mvn clean install

  run test too