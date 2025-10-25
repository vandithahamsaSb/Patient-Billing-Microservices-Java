# Patient & Billing Microservices

## Overview
This project is a fully functional Java Spring Boot microservice application that demonstrates how multiple services can work together using REST APIs, Docker, and a local cloud emulation. Each service runs independently while communicating with others, thereby simulating a real-world enterprise microservice architecture.

## Services Included
- **Patient Service** – Manages patient data.
Auth Service**: Handle authentication and authorization.
- **Billing Service**: Management of billing and payment processing.
- **Analytics Service** Collects and analyzes data across services.
- **API Gateway**: Routes and secure incoming requests.
- **Infrastructure** LocalStack setup for an AWS-like environment locally.

## Technology Stack
| Technology        | Purpose                                |
|------------------|----------------------------------------|
| Java 17+          | Core programming language              |
| Spring Boot       | Framework for building microservices  |
| Spring Cloud      | For microservices communication       |
| Docker            | Containerization                       |
| LocalStack        | Local AWS cloud emulation              |
| Maven             | Build and dependency management        |
| AWS CLI           | Infrastructure deployment              |

## How to Run Locally
1. Clone the repository  
git clone https://github.com/vandithahamsaSb/Patient-Billing-Microservices-Java.git
cd Patient-Billing-Microservices-Java

2.Build all services
mvn clean install

3.Start infrastructure 
cd infrastructure
docker run --rm -it -p 4566:4566 -p 4571:4571 localstack/localstack

4.Deploy infrastructure
localstack-deploy.sh

5.Run each service
cd auth-service && mvn spring-boot:run
cd patient-service && mvn spring-boot:run
cd billing-service && mvn spring-boot:run
cd analytics-service && mvn spring-boot:run


6.API Gateway
http://localhost:8080
Key Concepts Demonstrated
Microservices communication using REST and gRPC.

Containerizing services with Docker.

Managing cloud infrastructure locally with LocalStack.

Building and deploying Spring Boot microservices in a realistic environment.

Future Enhancements
Implement Notification Service.

Integrate real AWS services.



Author
Vanditha Hamsa
A developer specializing in Java, Spring Boot, and microservices architecture.


