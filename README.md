# Config Server - Pet Clinic Microservices

## 👤 Student & Project Metadata

- **Student Name**: Oshadha Sankalpa Thambavita
- **Student Number**: 241711043
- **Slack Handle**: Oshadha Thambavita
- **GCP ID**: eca-petclinic-241711043

Centralized configuration management service for the Pet Clinic polyrepo microservices application, built with **Spring Boot 3.4.3**, **Spring Cloud Config Server (2024.0.0)**, and **Java 25**.

## Features

- **Centralized Configuration**: Delivers environment-specific YAML configuration files to all microservices.
- **Native Classpath Storage**: Loads application settings dynamically from `src/main/resources/configurations/`.
- **Organized Structure**:
  - `configurations/application.yaml`: Shared Eureka client discovery settings.
  - `configurations/platform/api-gateway.yaml`: Gateway routes and CORS rules.
  - `configurations/services/doctor-service.yaml`: PostgreSQL & Google Cloud Storage bucket properties.
  - `configurations/services/pet-service.yaml`: MongoDB connection properties.
  - `configurations/services/appointment-service.yaml`: MySQL connection properties.

## Port & Profile

- **Port**: `8888`
- **Active Profile**: `native`

## Configuration Endpoints

Once started, configurations can be retrieved via HTTP:
- Doctor Service: `http://localhost:8888/doctor-service/default`
- Pet Service: `http://localhost:8888/pet-service/default`
- Appointment Service: `http://localhost:8888/appointment-service/default`
- API Gateway: `http://localhost:8888/api-gateway/default`

## How to Run

```bash
mvn clean spring-boot:run
```
