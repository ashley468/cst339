# Activity 6 Agenda - 1

- Date: *2025-3-21*
- Author: **Ashley Barron**

## Grand Canyon University Note
- This code will not execute correctly, since the code utilized is not available
- GCU will update this course in a future date
- Parts 1 and 4, I have alternative examples that will work, see the Agendas for details
- Parts 2 and 3, don't waste your time on those assignments.  Post a note below under Agendas, as shown below

## Introduction
- This activity will provide the following:
    - Configure an application to use Spring Security framework to secure a web application
    - Configure an application to use Spring Security framework to secure a REST API
    - Design and develop a secure web application using Spring framework
    - Design and develop a secure REST API using the Spring framework

## Securing a Web Application Using an In-Memory Datastore
- Update pom.xml

```
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-security</artifactId>
</dependency>
<dependency>
	<groupId>org.thymeleaf.extras</groupId>
	<artifactId>thymeleaf-extras-springsecurity5</artifactId>
</dependency>
```

## Create SecurityConfig.java
- There is an issue with the obsolete / missing Class WebSecurityConfigurerAdapter
- org.springframework.security.config.annotation.web.configuration.WebSecurityConfigurerAdapter
- Use this example to bypass in the mean time

```
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.context.annotation.Configuration;
import org.springframework.security.config.annotation.authentication.builders.AuthenticationManagerBuilder;

@Configuration
public class SecurityConfig {

	@Autowired
	public void configure(AuthenticationManagerBuilder auth) throws Exception {
		auth.inMemoryAuthentication().withUser("test").password("{noop}test").roles("USER");
	}
}
```

### Follow the instructions in the Activity Guide for the following:
- Create new controller/HomeController.java
- Update controller/LoginController.java
- Create new controller/OrdersController.java
- Remove data/mapper/LoginModel.java
- Update resources/templates/layouts/login.html
- Update resources/templates/layouts/common.html

## resources/templates/home.html
- Replace this file adding the link to the orders/display

```
<html xmlns:th="http://www.thymeleaf.org">
  <body>
	<a th:href="@{/orders/display}">Go to /orders/display</a>
  </body>
</html>
```

# Postman Setup
*check out links!!!
- GET: http://localhost:8080/service/getjson
- GET: http://localhost:8080/service/getxml
- Auth Type:  Basic Auth

# Execute Application in Browser
- https://localhost:8080/login
- Shown below the login page

![loginPage](loginPage.png)

- Enter Username:  test
- Enter Password:  test
- Press:  Sign in
- Shown below the Orders Display Link

[Go to /orders/display](http://localhost:8080/orders/display)

- Once pressed the Orders Page appears as shown below
![OrdersPage](ordersPage4.png)

- Press Logout to return to Login Page

## Logout Page
- You have been signed out page
![SignedOut](signedoutPage.png)

## Invalid Input
- Enter invalid user
![InvalidUser](invalidUser.png)

- Bad Credentials Return
![BadCredentials](badCredentials.png)

## Postman
- Postman Get JSON
***pic!!!!

- Postman Get XML
***pic!!!!

## Research Questions
### Research Questions: For traditional ground students, answer the following questions in a Microsoft Word document:

1. Research the Forms Based authentication scheme. Describe how this works. Why it is important to use the Spring Security framework versus developing your own custom security framework?

2. Research the Basic HTTP authentication schema. Describe how this works. How does this technology help secure a REST API endpoint?

### Research Answers
1. **
2. **

# Conclusion
- **