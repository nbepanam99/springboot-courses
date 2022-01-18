# SpringBoot-courses

Initialize Spring application from [Spring Initializr](https://start.spring.io/) 

## Spring Core


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

4. ApplicationSecurityConfig : Class to create for configuration
5. PasswordEncoder : We must encode password with encoder like BCryptPasswordEncoder.
6. Roles base authentification : Hight level view of users. Role have permissions.
7. Permission bases authentification :  

## JPA

|Anotation|Option|Description|
|---|---|---|
|@SequenceGenerator|name, sequenceName, AllocationSize|generate sequence for id|
|@GeneratedValue|strategy GenerationType.[AUTO,SEQUENCE,IDENTITY,TABLE], generator|Mode for generation|
|---|---|---|
|@Transient||not to be persisted in the database|


### Annexe : 

| Extend  | Override | Command | Description |
| ------------- | ------------- | ------------- | ------------- |
| WebSecurityConfigurerAdapter  | configure()  |  |  |
|   | |http.authorizeRequest.antMAtchers("patern")  |  |
|   |  |anyRequest().authentificated  |   |
||userDetailsService()||How we retrieve User from DB|
