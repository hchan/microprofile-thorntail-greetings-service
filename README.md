# SpringBoot vs MicroProfile-Thorntail
See also 
[spring-boot-greetings-service](https://github.com/hchan/spring-boot-greetings-service)

## Spring projects are more extensive
- Spring Data JPA 
- Spring CDC 
- Spring community is huge
- `SpringRunner` ... see below

## Personal feelings ( open to change ;))
- I just think the Spring Boot is shorter and easier to read ... 
- Testing with `SpringRunner` was easier than `Arquillian`
- Does Arquillian support random ports?
- Had to add:
- `-Dthorntail.arquillian.daemon.port=19999 -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Xbootclasspath/p:C:/Users/Henry/.m2/repository/org/jboss/logmanager/jboss-logmanager/2.1.11.Final/jboss-logmanager-2.1.11.Final.jar`
- Also had to run Project ... Clean often in Eclipse
- Alternatively, I could use Open Liberty
- which also brings up the next issue ... which vendor for Microprofile ... will I get into a vendor-lock problem?
- Without running tests, the only other way to start microprofile-thorntail 
- `java -jar target\*.jar` ... not great for debugging
- added a `GreetingServiceTest.runDummyServer` for debugging in interactive mode
 
## Atlernative to Arquillian / SpringRunner
- I believe testing Microservices is part of Integration testing wrt [Martin Fowler's test Pyramid](https://martinfowler.com/articles/practical-test-pyramid.html)
- Java may not be the answer
- I STRONGLY recommend `Postman` (black box testing).  `Newman` can be used in CI
- Black box is good ... you also offset this work to other developers (i.e. a more junior developer with NodeJS skills)
- if you wish to migrate to `Postman` from `Arquillian`, there is a http://arquillian.org/guides/generator/  Arquillian APE REST Postman

 
# Conclusion
I still like Spring Boot more,
Then again, I'm open to giving Microprofile a shot

 
 
 
 
