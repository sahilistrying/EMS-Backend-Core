# 🏢 EMS-Backend-Core: Enterprise HR API

![Java](https://img.shields.io/badge/Java-17-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-Database-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-API_Testing-FF6C37?style=for-the-badge&logo=postman&logoColor=white)

> *A high-throughput RESTful API engineered by Sahil Hussain to serve as the core data engine for organizational workforce management.*

*(Note: The Front-end Client is fully decoupled from this repository to adhere to Microservice architecture standards).*

---

## 🎯 Engineering Context & Motivation
I architected **EMS-Backend-Core** to master **Enterprise Java Systems** and **Relational Database Design**. Moving beyond basic monolithic applications, my objective was to build a secure, scalable API layer capable of handling real-world CRUD operations, complex data mapping, and strict error handling required by modern financial and healthcare organizations.

---

## ⚙️ Core Technology Stack

**Infrastructure & Frameworks:**
* **Java (JDK 17+):** Core language utilized for object-oriented business logic.
* **Spring Boot:** Deployed as the primary framework for dependency injection, embedded Tomcat routing, and REST endpoint generation.
* **Jakarta Persistence (JPA) & Hibernate:** Implemented advanced Object-Relational Mapping (ORM) using `@Entity`, `@Id`, and `@GeneratedValue` to map Java models directly to database tables.

**Data Persistence & QA:**
* **MySQL:** Primary relational database ensuring ACID compliance for employee records.
* **DataGrip / MySQL Workbench:** Utilized for schema design and raw query optimization.
* **Postman:** Deployed for rigorous endpoint validation, testing JSON payloads across all HTTP methods (`GET`, `POST`, `PUT`, `DELETE`).

---

## 🏗️ System Architecture & Highlights

### **N-Tier Design Pattern**
The application is strictly layered. Controllers handle HTTP ingress, Services process business rules, and Repositories interface with the database. This guarantees high maintainability and testability.

### **Robust Exception Handling**
Enterprise APIs must never return raw stack traces. I engineered custom exception classes (e.g., `ResourceNotFoundException`) combined with Spring controller advice to intercept bad requests (like querying an invalid Employee ID) and return sanitized, structured HTTP response codes to the client.

---

## 📊 API Testing Validation (Postman)
*Comprehensive endpoint testing ensuring payload integrity and proper SQL execution.*

### **Standard Execution Flow (200 OK)**
> *Validating successful data retrieval, creation, and modification.*
*(Insert your original GET, PUT, POST Normal Case screenshots here)*

### **Edge Case & Exception Flow (404/400 HTTP Status)**
> *Demonstrating the Custom Exception Architecture when querying non-existent entities.*
*(Insert your original GET/DELETE Exceptional Case screenshots here)*

---
<p align="center"><i>Engineered by Sahil. Built for Enterprise Scale.</i></p>
