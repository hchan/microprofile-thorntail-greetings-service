# SpringBoot vs MicroProfile-Thorntail

## Spring projects are more extensive
- Spring Data JPA rocks
- Spring CDC is cool
Spring community is huge
I just think the Spring Boot is shorter and easier to read ... 

## Personal humps
Testing with Arquillan was flaky
@RunWith(Arquillian.class) is as mature as SpringRunner ... Random ports?
Had to add
-Dthorntail.arquillian.daemon.port=19999 -Djava.util.logging.manager=org.jboss.logmanager.LogManager -Xbootclasspath/p:C:/Users/Henry/.m2/repository/org/jboss/logmanager/jboss-logmanager/2.1.11.Final/jboss-logmanager-2.1.11.Final.jar
Also had to run Project ... Clean often in Eclipse
Alternatively, I could use Open Liberty
which also brings up the next issue ... which vendor for Microprofile?
Without running tests, the only other way to start microprofile-thorntail 
is java -jar target\*.jar ... not great for debugging
hack:
add a runDummyServer in GreetingServiceTest
 
## Atlernative to Arquillian
 Alternatively without using @RunWith(Arquillian.class) to test Microservices,
 I STRONGLY recommend Postman (black box testing).  Black box is good ... you also offset this work to other developers (i.e. a more junior developer with NodeJS skills)
 Postman / Newman rocks! ... if you wish to migrate to Postman, there is a http://arquillian.org/guides/generator/  Arquillian APE REST Postman
 
 Putting testing aside, there was no "main" method in microprofile for me to put start my debugger in?
 The only way I could run microprofile was by something like:
 
 
Conclusion
I still like Spring Boot more,
Then again, I'm open to giving Microprofile a shot

 
 
 
 