# Activity 3

- Date: *2025-2-10*
- Author: **Ashley Barron**

## Introduction
- This activity will provide the following:
    - Configure an application to use the Spring Core framework
    - Design and build Spring Beans using the Spring Core framework
    - Leverage the IoC container in the Spring Framework in support of applying the dependency injection design pattern
    - Design and develop REST API's using the Spring MVC/Spring Data REST and Spring Core frameworks

## Screenshots
### Part 1: Creating Modles, Views, and Controllers Using Spring MVC 
- This is a screenshot of the interface being called
**Screenshot*

- This is a screenshot of the Another Interface being called
**Screenshot*

- This is a screenshot of the Authenticate being called
**Screenshot*

- This is a screenshot of the Orders page
**Screenshot*

### Part 2:  Spring Bean Life Cycle and Scopes
- This is a screenshot of the init method call
**Screenshot*

- This is a screenshot of the @RequestScope annotation
**Screenshot*

- This is a screenshot of the @sessionScope annotation
**Screenshot & link!!!*

### Part 3:  Creating REST Services Using Spring REST Controllers
- This is a screenshot of the JSON response
**Screenshot*

- This is a screenshot of the XML response
**Screenshot*

- This is a screenshot of the Postman JSON response
**Screenshot*

- This is a screenshot of the Postman XML response
**Screenshot*

## Research Questions - located in Activity Guide
- **DON'T FORGET TO INCLUDE QUESTIONS & ANSWERS!!!*
- **Post the Questions and Answers*


### Questions
1. What is the difference between the @Component, @ Service, and @Bean 
annotations? When would you use one versus the other?

2. Why does an Inversion of Control (IoC) Container force you to design and 
code to interface contracts?

### Answers
1.
    - @Component is a class-level annotation used to mark a class as a Spring-managed Component. 
    It allows Spring to detect and manage the class as a bean through component scanning. 
    This annotation is ideal for generic components that encapsulate reusable operations, such as utility classes.  

    - @Service is a specialization of @Component, specifically used for classes containing business logic. It conceptually belongs to the 
    service layer. Marking as a class with @Service makes your code more readable and organized, clearly indicating its 
    purpose. Spring will autodetect these classes when using annotation-based configuration. For instance, 
    you might annotate a payment service class with @service to manage payment processing logic.
    
    - @Bean is used to declare a single bean explicitly when automatic component scanning is 
    insufficient. It decouples the declaration of the bean from the class definition, allowing 
    you to create and configure beans as needed. @Bean is typically used inside a @Configuration 
    class and is useful for integrating third-party libraries or defining beans with custom 
    initialization logic. For example, you might use @Bean to define a custom instance of an external DataSource object. 

2. ***


## Part 2 Questions
- Explain in 2-3 sentences how the code worked (when init() was called) and why the number of 
calls to init() where made of the following annotations

    - @scope(value="prototype", proxyMode=ScopedProxyMode.TARGET_CLASS)
    - @RequestScope
    - @sessionScope **Don't forget link!!!*
    - SingletonScope


## Conclusion
- **Place a Conclusion here!!!*