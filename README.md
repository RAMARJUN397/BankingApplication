# BankingApplication

server.portnumber = 2510 <br />

Sonar Properties <br />
--------------------------------------- <br />
sonar.host.url=http://3.109.199.80:9000/ <br />
sonar.projectKey=siri <br />
sonar.projectName=siri <br />
sonar.sourceEncoding=UTF-8 <br />
sonar.language=java <br />
sonar.java.source=1.7 <br />
sonar.java.target=1.7 <br />
sonar.projectVersion=1.0 <br />
sonar.sources=src/main/java <br />
sonar.java.binaries=. <br />

maven Goal ---- sonar:sonar -Dsonar.host.url=http://localhost:9000/ -Dsonar.user=admin -Dsonar.token=squ_711a87c4f69ed4f9710a9db9b7d8b4c8e14deba8  -Dsonar.projectKey=mywebapplication  -Dsonar.projectName=mywebapplication -Dsonar.sourceEncoding=UTF-8 -Dsonar.language=java -Dsonar.java.source=1.7 -Dsonar.java.target=1.7 -Dsonar.projectVersion=1.0 -Dsonar.sources=src/main/java -Dsonar.java.binaries=.

maven Plugin
------------

<plugin>
        <groupId>org.sonarsource.scanner.maven</groupId>
        <artifactId>sonar-maven-plugin</artifactId>
        <version>3.7.0.1746</version>
      </plugin>


-------------------------------------------DockerFile------------------------ <br />
FROM eclipse-temurin:17-jdk-alpine <br />
MAINTAINER "Arjun DevOps World"  <br />
VOLUME /tmp <br />
 COPY target/*.jar BankingApplication.jar <br />
ENTRYPOINT ["java","-jar","/BankingApplication.jar"]
