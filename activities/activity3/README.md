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
<br>

![Interface](interface.png)

- This is a screenshot of the Another Interface being called
<br>

![AnotherInterface](anotherInterface.png)

- This is a screenshot of the Authenticate being called
<br>

![Authenticated](authenticated.png)

- This is a screenshot of the Orders page
![Orders](orders.png)

### Part 2:  Spring Bean Life Cycle and Scopes
- This is a screenshot of the init method call
- The init method was added in the "OrdersBusinessService" and "AnotherOrdersBusinessService" classes after it was first declared in the "OrdersBusinessServiceInterface". We also had to modify the @Bean section in the "SpringConfig" class to make sure that the correct implementation was used. The number of times that the init method was called depends on how many times the corresponding beans were instantiated. 
<br>

![InitMethod](initMethod.png)


- This is a screenshot of the @RequestScope annotation.
- The init() method is called each time the program is executed or when the page is refreshed. The number of times it's called depends on how many times the site is refreshed or how many instances are initialized during the program's runtime.
<br>

![RequestScope](requestScope.png)

- This is a screenshot of the @sessionScope annotation.
- Just as with the rest of the screenshots, the number of times the init() method appears depends on how many times the site is refreshed. Each time the page is reloaded, the init() method is called to initialize the page. This makes sure that any necessary setup for the page, such as setting default values, is performed and that the code behaves as intended with each new session or reload.
<br>

![SessionScope](sessionScope.png)

### Part 3:  Creating REST Services Using Spring REST Controllers
- This is a screenshot of the JSON response
<br>

![Json](json.png)

- This is a screenshot of the XML response
![XML](xml.png)

- This is a screenshot of the Postman JSON response
<br>

![PostmanJson](postmanJson.png)

- This is a screenshot of the Postman XML response
<br>

![PostmanXml](postmanXml.png)

## Research Questions

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

2. 
    - By programming to interfaces, you can create code that is more modular and 
    flexible, making it easier to adapt and extend in the future. The IoC container enforces this approach by managing object creation and dependencies, 
    allowing you to inject different implementations of an interface at runtime without 
    changing the dependent classes. This leads to better decoupling between components and 
    allows for easy replacement or enhancement of functionality. To maintain a clear separation 
    of concerns, it's important to keep the IoC container configuration separate from your business logic. 
    This separation ensures that your business logic remains focused on the application's core functions, 
    while the IoC container takes care of managing object dependencies and their lifecycle. 


## Part 2 Questions
- Explain in 2-3 sentences how the code worked (when init() was called) and why the number of 
calls to init() where made of the following annotations

    - @scope(value="prototype", proxyMode=ScopedProxyMode.TARGET_CLASS)
    - @RequestScope
    - @sessionScope **Don't forget link!!!*
    - SingletonScope


## Conclusion
- **Place a Conclusion here!!!*

