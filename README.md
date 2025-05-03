# ARB Bill of Materials (BOM)

A microservice-based QR code authentication system built with Spring Boot 3.x, designed for secure and efficient user authentication.

## Overview

This project provides a centralized Bill of Materials (BOM) for managing dependencies consistently across multiple projects. By using this BOM, developers can ensure that all modules and services share the same versions of libraries, reducing version conflicts and simplifying dependency management.
## Features

- Centralized version control for dependencies
- Simplifies upgrades and maintenance across projects
- Promotes consistency and stability between modules
- Reduces risk of dependency version conflicts

## Technical Stack

- **Framework**: Maven 
- **Artifactory**: JFrog

## Architecture

### Components

1. **ARB BOM**
    - Centralized version control for dependencies

2. **Infrastructure**
    - JFrog Artifactory

### How to Use

- To be able to microservice follow up the **BOM** you need to add it inside your `pom.xml`

```maven
<dependencyManagement>
  <dependencies>
    <dependency>
      <groupId>com.arb</groupId>
      <artifactId>alrajhi-bom</artifactId>
      <version>${revision}</version>
      <type>pom</type>
      <scope>import</scope>
    </dependency>
  </dependencies>
</dependencyManagement>
```

- If you have any change on the pom.xml you should deploy the change on the artifactory,to do it you can use the following command.

`mvn clean install deploy`