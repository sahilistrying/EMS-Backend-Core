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


### **Edge Case & Exception Flow (404/400 HTTP Status)**
> *Demonstrating the Custom Exception Architecture when querying non-existent entities.*

---
## ✏️ Design - Back-end

### Back-end Technology Stack
* **Java** served as the **back-end programming language** for the web application, while the **Spring Boot framework** was employed to **facilitate its development and operation**.
* **Spring Boot** was utilised to **create user models**, which were subsequently employed to **store employee information in the database**. The user models were established using the **Jakarta Persistence import** and **annotations**, including **@Entity, @Id, and @GeneratedValue**. This approach **facilitated the maintenance of the REST API**, making it more manageable and easier to maintain in the long run.
* **MySQL Workbench and DataGrip** were employed to **store employee information**. The **back-end**, developed with **Spring Boot**, was **configured to connect with the database**, while the **front-end**, built with **React**, was responsible for **retrieving and displaying** this information.
* **Spring Boot** was additionally utilised to **create custom exceptions**, specifically designed for **handling scenarios where the user ID was not found or encountered other exceptional conditions**.

#### React & Spring Boot Summarisation Diagram
<img width="800" alt="Architecture Diagram" src="https://raw.githubusercontent.com/sahilistrying/EMS-Backend-Core/main/images/diagram.png">

---

## 📊 Postman and Testing Screenshots
* **Postman** was used as an **API platform** to **design, build, test and iterate** the **RESTful API** which was **built using Spring Boot**.
* Requests were dealt in **JSON** and **SQL**.

### GET Request (Normal Case) 
<img width="800" alt="GET Normal" src="https://raw.githubusercontent.com/sahilistrying/EMS-Backend-Core/main/images/get-normal.png">

### GET Request (Exceptional Case)
*The custom error handling implemented in the Spring Boot back-end works successfully, as evidenced by the appropriate handling of the situation where a user with an ID of 20 does not exist.*
<img width="800" alt="GET ERROR" src="https://raw.githubusercontent.com/sahilistrying/EMS-Backend-Core/main/images/get-error.png">

### PUT Request (Normal Case)
<img width="1440" alt="PUT" src="https://raw.githubusercontent.com/sahilistrying/EMS-Backend-Core/main/images/put-normal.png">

### DELETE Request (Exceptional Case)
<img width="800" alt="DELETE ERROR" src="https://raw.githubusercontent.com/sahilistrying/EMS-Backend-Core/main/images/delete-error.png">

### POST Request (Normal Case)
<img width="800" alt="POST Normal" src="https://raw.githubusercontent.com/sahilistrying/EMS-Backend-Core/main/images/post-normal.png">

### Postman Summarisation Diagram
<img width="800" alt="Postman Summary" src="https://raw.githubusercontent.com/sahilistrying/EMS-Backend-Core/main/images/postman-summary.png">

---

## 💻 Application Screenshots (React Front-end)

### Home Page 
<img width="800" alt="Home Page" src="https://raw.githubusercontent.com/sahilistrying/EMS-Backend-Core/main/images/home.png">

### Register User Page
<img width="800" alt="Register User Page" src="https://raw.githubusercontent.com/sahilistrying/EMS-Backend-Core/main/images/register.png">

### View User Details Page
<img width="800" alt="View User Details Page" src="https://raw.githubusercontent.com/sahilistrying/EMS-Backend-Core/main/images/view.png">

### Edit User Page
<img width="800" alt="Edit User Page" src="https://raw.githubusercontent.com/sahilistrying/EMS-Backend-Core/main/images/edit.png">



<p align="center"><i>Engineered by Sahil. Built for Enterprise Scale.</i></p>
 
 
