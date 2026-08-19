# Eureka Server

Service Registry component for the Pet Clinic microservices platform, enabling service registration and discovery.

## Student Information
- **Student Name:** Isuri Gamage
- **Student Number:** 241722008
- **Slack Handle:** 
- **GCP Project ID:** 
## Project Description
The `eureka-server` acts as the central Service Registry for all microservices in the Pet Clinic system (owner-service, pet-service, appointment-service, api-gateway). Each service registers itself with Eureka on startup, allowing the API Gateway and other services to dynamically discover and communicate with each other without hardcoded network locations.

## Technology Stack
- **Language:** Java 25
- **Framework:** Spring Boot, Spring Cloud Netflix Eureka Server
- **Build Tool:** Maven
- **Cloud Platform:** Google Cloud Platform (GCP) — deployed as IaaS on Compute Engine VM Instance Groups (multi-zone for high availability)
- **Process Management:** PM2

## Setup / Getting Started

### Prerequisites
- Java 25 (JDK)
- Maven

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/Isuri15/eureka-server.git
   cd eureka-server
   ```
2. Build and run the service:
   ```bash
   mvn clean install
   mvn spring-boot:run
   ```
3. The Eureka Dashboard will be available at:
   ```
   http://localhost:8761
   ```
4. Start this service **first**, before any other microservice in the system.

## Cloud Deployment
Deployed on Google Cloud Platform with multiple instances distributed across different zones within the region to ensure high availability and fault tolerance, as required by the platform's high-availability architecture.

## Related Repositories
This service is part of the Pet Clinic platform components. See the parent repository:
- [backend-microservices-platform](https://github.com/Isuri15/backend-microservices-platform)
