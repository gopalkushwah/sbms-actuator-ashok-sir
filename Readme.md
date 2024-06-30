# Spring Boot Actuator

## Introduction

Spring Boot Actuator provides production-ready features to help you monitor and manage your application. With minimal configuration, you can gain insights into the running state of your application.

## Key Features

- **Health Checks**: Monitor the health of your application.
- **Metrics**: Gather and expose various metrics related to your application.
- **HTTP Tracing**: Track HTTP requests and responses.
- **Application Info**: Display application information like version, environment, etc.

## Getting Started

To use Spring Boot Actuator, you need to add the dependency to your `pom.xml` file:

```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
```

## Endpoints
Spring Boot Actuator exposes several endpoints that you can use to monitor and manage your application. Some of the most commonly used endpoints are:

- **/actuator/health**: Displays the health status of the application.
- **/actuator/info**: Provides information about the application.
- **/actuator/metrics**: Shows various metrics collected by the application.
- **/actuator/httptrace**: Displays HTTP trace information.



```
- to enable all the actuators end points
management:
  endpoints:
    web:
      exposure:   
        include: '*'   #to include all the 13 endpoints
        exclude:
        - beans     # excluding beans endpoint
  # enabling shutdown hook, the default value is false
  endpoint:
    shutdown:
      enabled: true
spring:
  application:
    name: SBMS_Actuator
```

### Conclusion
- Spring Boot Actuator is a powerful tool that provides essential features for monitoring and managing your application in a production environment. 
- By leveraging its capabilities, you can gain valuable insights and ensure the health and performance of your application.

