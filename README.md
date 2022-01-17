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
     +--------+                               +---------------+
     |        |--(A)- Authorization Request ->|   Resource    |
     |        |                               |     Owner     |
     |        |<-(B)-- Authorization Grant ---|               |
     |        |                               +---------------+
     |        |
     |        |                               +---------------+
     |        |--(C)-- Authorization Grant -->| Authorization |
     | Client |                               |     Server    |
     |        |<-(D)----- Access Token -------|               |
     |        |                               +---------------+
     |        |
     |        |                               +---------------+
     |        |--(E)----- Access Token ------>|    Resource   |
     |        |                               |     Server    |
     |        |<-(F)--- Protected Resource ---|               |
     +--------+                               +---------------+
