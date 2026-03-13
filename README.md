# QA-Altare

### 1. A developer adds @Autowired to a constructor in a Spring Boot service class. What is the main purpose of this annotation in this context?
- [ ] A Logs constructor invocations 
- [ ] B Creates a singleton instance 
- [ ] C Marks the class as configuration 
- [x] D Injects required dependencies automatically

> **Explanation:** And it is not recommanded when we have one constructor, but when we have multiple contructors it is recommanded to use **@Autowired** to tell to spring which constructor will be used to inject the dependencies.

### 2. In a Spring Boot application, a developer uses @Value annotation to inject a property. What happens if the property key does not exist in application.yml and no default value is provided? 
- [ ] A Property is set to null 
- [x] B Application fails to start 
- [ ] C Application ignores the field 
- [ ] D Spring assigns a random value

> **Explanation:** If the key not exist in the configuration file and no default value provided, spring cannot resolve the placeholder, this causes a bean creation error and the application fails on start-up.

### 3. Consider this Spring Boot controller method: 
```
@GetMapping("/user/{id}") 
public ResponseEntity<User> getUser(@PathVariable Long id) { 
// method body 
} 
```
What is the purpose of @PathVariable in this context? 
- [ ] A Validates the parameter 
- [x] B Binds URI segment to parameter 
- [ ] C Handles JSON serialization 
- [ ] D Injects a bean
> **Explanation:** @PathVariable extracts a value from the URL path and assigns it to a method parameter.

### 4. Choose all correct statements about using @Transactional in a Spring Boot service method handling order placement in an e-commerce system. 
- [ ] A May not roll back on RuntimeException 
- [x] B Ensures atomicity of the method 
- [ ] C Always rolls back on any exception 
- [ ] D Prevents dirty reads and non-repeatable reads 
- [ ] E Supports nested transactions with default config

> Explanation: @Transactional ensures that all database operations inside the method succeed or fail together. 

### 5. Which pattern helps prevent duplicate processing when a microservice receives the same message multiple times due to retries from a queue? 
- [ ] A Load balancing 
- [ ] B Circuit breaker 
- [x] C Idempotency or deduplication logic 
- [ ] D Rate limiting


### 6. Your company is planning to host a microservices-based application on AWS and wants to achieve high availability. Which AWS feature should you use to ensure services remain operational even if one data center experiences an outage?  
- [ ] A Use AWS Lambda for all services 
- [ ] B Enable CloudWatch logging 
- [ ] C Store data in S3 only 
- [x] D Deploy in multiple Availability Zones 

### 7. A team wants to be notified whenever an EC2 instance’s CPU usage stays above 80% for 5 minutes to avoid performance issues. Which AWS service and feature is most appropriate for this requirement? 
- [x] A CloudWatch Alarm 
- [ ] B S3 Event Notification 
- [ ] C IAM Policy 
- [ ] D VPC Flow Logs

### 8. An application uses an S3 bucket to store images. Which AWS feature would you use to restrict access to this bucket for a specific IAM role handling uploads?  
- [ ] A Enable S3 versioning 
- [ ] B Use CloudTrail logs 
- [x] C Assign an IAM policy to the role 
- [ ] D Configure VPC endpoint 

### 9. In a serverless architecture, what is a typical benefit of using AWS Lambda for backend logic in a microservices-based ecommerce platform?  
- [ ] A Fixed monthly cost 
- [ ] B Persistent storage 
- [x] C Automatic scaling and event-driven execution 
- [ ] D Manual resource scaling
### 10. Which AWS service would you use to automatically run code in response to changes in an S3 bucket (e.g., new file upload)?  
- [ ] A Amazon RDS 
- [ ] B Amazon SQS 
- [ ] C AWS IAM 
- [x] D AWS Lambda
### 11. Which type of test focuses on ensuring that multiple components of an application work together as expected?  
- [ ] A Unit test 
- [ ] B Load test 
- [x] C Integration test 
- [ ] D Static analysis

### 12. A developer writes the following test for a Spring Boot REST API endpoint that returns order details. What key aspect of testing is missing in the code below? 
```
@Test 
void testGetOrder() { 
Order order = new Order(42, "SHIPPED"); 
when(orderService.fetchOrder(42)).thenReturn(order); 
Order result = orderController.getOrder(42); 
assertEquals("SHIPPED", result.getStatus()); 
} 
```
- [ ] A No assertions present 
- [x] B No test for error scenarios 
- [ ] C No mocking of dependencies 
- [ ] D No initialization of controller

### 13. Review the following JUnit test for a microservices API and select all best practices being followed: 
```
@Test 
void testGetUser() { 
when(userService.findUser(1L)).thenReturn(new User("Alice")); 
User result = userController.getUser(1L); 
assertEquals("Alice", result.getName()); 
}
```
- [ ] A Directly tests private methods 
- [ ] B Uses real database 
- [x] C Tests controller logic 
- [x] D Mocks dependencies 
- [x] E Verifies expected output
