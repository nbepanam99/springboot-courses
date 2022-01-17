# springboot-courses

Initialize Spring application from [Spring Initializr](https://start.spring.io/) 


## Spring Security
1. Open the file pom.xml.
2. Add dependency :

        	<dependency>
			      <groupId>org.springframework.boot</groupId>
			      <artifactId>spring-boot-starter-security</artifactId>
		      </dependency>

3. Basic Auth.
```
     +--------+                               +---------------+
     |        |--(A)-----  Get Request  ----->| Authorization |
     | Client |                               |     Server    |
     |        |<-(B)---- 401 Unauthorized ----|               |
     |        |                               |               |
     |        |                               |               |
     |        |--(C)---  Get Request          |               |
     |	      |	   B64 username/password  --->|    Resource   |
     |        |                               |     Server    |
     |        |<-(D)---    200 Ok	   ---|               |
     +--------+                               +---------------+
```
