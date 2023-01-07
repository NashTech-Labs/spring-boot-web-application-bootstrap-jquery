<!---
Current Directory : /knoldus/git/spring-boot-examples/spring-boot-web-application-bootstrap-jquery
-->

## Example Code

### /pom.xml

```xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>
  <parent>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-parent</artifactId>
    <version>3.0.0-M4</version>
    <relativePath/> <!-- lookup parent from repository -->
  </parent>

  <groupId>com.knoldus.springboot.web.application</groupId>
  <artifactId>spring-boot-web-application-bootstrap-jquery</artifactId>
  <version>0.0.1-SNAPSHOT</version>
  <packaging>jar</packaging>

  <name>spring-boot-web-application-bootstrap-jquery</name>
  <description>Spring Boot Tutorial - Adding Bootstrap and JQuery to Web Application</description>

  <properties>
    <java.version>17</java.version>
  </properties>

  <dependencies>
    <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-web</artifactId>
    </dependency>

    <dependency>
      <groupId>org.webjars</groupId>
      <artifactId>bootstrap</artifactId>
      <version>5.2.0</version>
    </dependency>

    <dependency>
      <groupId>org.webjars</groupId>
      <artifactId>bootstrap-datepicker</artifactId>
      <version>1.9.0</version>
    </dependency>

    <dependency>
      <groupId>org.webjars</groupId>
      <artifactId>jquery</artifactId>
      <version>3.6.1</version>
    </dependency>

    <dependency>
      <groupId>org.apache.tomcat.embed</groupId>
      <artifactId>tomcat-embed-jasper</artifactId>
      <scope>provided</scope>
    </dependency>

    <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-devtools</artifactId>
      <scope>runtime</scope>
    </dependency>

    <dependency>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-starter-test</artifactId>
      <scope>test</scope>
    </dependency>
  </dependencies>

  <build>
    <plugins>
      <plugin>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-maven-plugin</artifactId>
      </plugin>
    </plugins>
  </build>

  <repositories>
    <repository>
      <id>spring-milestones</id>
      <name>Spring Milestones</name>
      <url>https://repo.spring.io/milestone</url>
      <snapshots>
        <enabled>false</enabled>
      </snapshots>
    </repository>
  </repositories>

  <pluginRepositories>
    <pluginRepository>
      <id>spring-milestones</id>
      <name>Spring Milestones</name>
      <url>https://repo.spring.io/milestone</url>
      <snapshots>
        <enabled>false</enabled>
      </snapshots>
    </pluginRepository>
  </pluginRepositories>


</project>
```

---

### /src/main/java/com/knoldus/springboot/application/configuration/SpringBootWebApplicationBootstrapJqueryApplication.java

```java
package com.knoldus.springboot.tutorial.basics.application.configuration;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class SpringBootWebApplicationBootstrapJqueryApplication {

  public static void main(String[] args) {
    SpringApplication.run(SpringBootWebApplicationBootstrapJqueryApplication.class, args);
  }
}
```

---

### /src/main/java/com/in28minutes/springboot/tutorial/basics/application/configuration/WelcomeController.java

```java
package com.in28minutes.springboot.tutorial.basics.application.configuration;

import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class WelcomeController {

  @RequestMapping("/welcome")
  public String loginMessage() {
    return "welcome";
  }
}
```

---

### /src/main/resources/application.properties

```properties
spring.mvc.view.prefix=/WEB-INF/jsp/
spring.mvc.view.suffix=.jsp
logging.level.org.springframework.web=INFO
```

---

### /src/main/resources/static/css/custom.css

```css
body {
    background-color: lightblue;
}
```

---

### /src/main/resources/static/js/custom.js

```js
alert("I'm active");
```

---


```

---
