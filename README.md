# 🚗 Ride-Sharing App System Design

## 📝 Overview

This document outlines the system design for a Ride-Sharing Web Application that connects drivers with passengers. It focuses on scalability, fault tolerance, and a high-quality user experience to support millions of users globally.

### User Types

- **Drivers**: Offer rides, manage bookings, and receive payments.
- **Passengers**: Search and book rides, make payments, and rate their experience.

## 🏗 System Architecture Overview

### 🖥️ Frontend

**Technology Stack**: Angular

- **Why Angular?** Angular is chosen for its comprehensive ecosystem and robust framework that supports the development of dynamic, rich web applications. Its two-way data binding, modular development structure, and extensive libraries help in creating a seamless user experience. Angular's CLI also offers productivity and scalability benefits, making it easier to maintain code quality and consistency across large projects.

### 🔙 Backend

**Spring Boot Microservices**

- **Why Spring Boot?** Spring Boot is utilized for its ability to simplify the bootstrapping and development of new Spring applications. Its convention over configuration, a wide range of out-of-the-box functionalities, and the ability to create standalone applications make it ideal for microservices architecture. Spring Boot's support for embedded servers, externalized configuration, and comprehensive ecosystem allows for building scalable, secure, and resilient backend services.
- **Spring Boot Microservices**: For scalable backend services.
- **API Gateway**: As the single entry point for all client requests.
- **Service Registry & Discovery**: For dynamic service discovery.
- **Config Service**: For centralized configuration management.
- **Circuit Breaker**: For fault tolerance.

### 🗄️ Database
**PostgreSQL**

- **Why PostgreSQL?** PostgreSQL is selected for its advanced features, reliability, and strong performance. It supports complex queries, foreign keys, triggers, views, transactions, and sophisticated data types. Being open-source, it offers extensive community support and flexibility. PostgreSQL's ability to handle large volumes of data and its compliance with ACID properties make it a robust choice for applications requiring complex data management.

## Additional Components

- **Rate Limiter**: To prevent abuse and ensure service availability.
- **Fault Tolerance**: Ensuring the system remains responsive during partial outages.

## 🖼 ER Diagram

![ER Diagram](./Folder/ER%20Diagram.png)

## 🚀 Key API Endpoints

- `POST /rides`: Create a new ride request.
- `GET /rides`: Retrieve available rides for drivers.
- `PUT /rides/{rideId}/accept`: Accept a ride request.
- `POST /payments`: Process payments.
- `POST /reviews`: Submit reviews.

## 📦 Deployment and Infrastructure

- Utilizes AWS services for hosting, storage, and content delivery.
- Implements CI/CD pipelines for automated testing and deployment.

## 📚 Conclusion

This Ride-Sharing App design provides a comprehensive blueprint for a scalable, fault-tolerant service capable of supporting millions of users. By leveraging modern technologies and architectural patterns, we ensure a responsive, efficient, and user-friendly experience. Future enhancements will focus on incorporating advanced analytics for ride optimization, expanding service offerings, and enhancing user personalization.

