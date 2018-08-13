![hl_default_quilt](https://user-images.githubusercontent.com/36883383/44053792-5e3789f8-9f5e-11e8-97e9-4f1c21409d8c.png)


# Hyperledger Quilt

Quilt is an implementation of the Interledger.Quilt is the most recent Hyperledger project and is a Java implementation of the Interledger protocol. It offers interoperability between ledger systems by executing the Interledger convention, which is basically a payment protocol and is intended to exchange an incentive crosswise over frameworks – both kind of ledgers, distributed and non-distributed. Below is the complete guide for sample setup of the hyperledger quilt.

## Modules

The quilt project is organised as a Maven multi-module project. Each module exists in a subdirectory and has its own
POM and README.



### Prerequisites

1. **JCE**:
In order to properly build this project, you must download and install Java Cryptography Extension (JCE) Unlimited Strength Jurisdiction Policy files. 
For more details, follow the instructions [here](http://www.oracle.com/technetwork/java/javase/downloads/jce8-download-2133166.html). 

2. **Maven**:
This project uses Maven to manage dependencies and other aspects of the build. 
To install Maven, follow the instructions at [https://maven.apache.org/install.html](https://maven.apache.org/install.html).

Modules in this library can be included in your project by first adding a Snapshot Repository to your `pom.xml` file, like this:

```
<repositories>
    ...
    <repository>
        <id>sonatype</id>
        <url>https://oss.sonatype.org/content/repositories/snapshots/</url>
    </repository>
    ...
</repositories>
```
Next, add the following Maven dependency:

```
<dependencies>
  ...
  <dependency>
    <groupId>org.interledger</groupId>
    <artifactId>java-ilp-core</artifactId>
    <version>0.12.1-SNAPSHOT</version>
  </dependency>
  ...
</dependencies>
```

3. **Gradle**:
To import this library into a project that uses gradle, first add the Snapshot Repository to your `gradle.properties` file, like this:

```
repositories {
    mavenCentral()
    maven {
        url "https://oss.sonatype.org/content/repositories/snapshots/"
    }
}
```
Next, import this library as a dependency, like this:

```
dependencies {
    ...
    compile group: 'org.interledger', name: 'java-ilp-core', version: '0.12.1-SNAPSHOT'
    ...
}
```

## Development

To get started, first download the code:

- git clone https://github.com/hyperledger/quilt
- cd quilt


## Build the Project
To build the project, execute the following command:

- $ mvn clean install


## Checkstyle
The project uses checkstyle to keep code style consistent. All Checkstyle checks are run by default during the build, but if you would like to run checkstyle checks, use the following command:


- $ mvn checkstyle:checkstyle

