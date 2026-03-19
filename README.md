# Rides24 - Ride-Sharing Enterprise Application

![Java](https://img.shields.io/badge/Java-11-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![ObjectDB](https://img.shields.io/badge/ObjectDB-NoSQL-47A248?style=for-the-badge&logo=database)
![JAX-WS](https://img.shields.io/badge/JAX--WS-SOAP-007396?style=for-the-badge)
![JUnit](https://img.shields.io/badge/JUnit_4-Testing-25A162?style=for-the-badge&logo=junit5&logoColor=white)
![SonarCloud](https://img.shields.io/badge/SonarCloud-Quality_Gate-F3702A?style=for-the-badge&logo=sonarcloud&logoColor=white)

Rides24 is a fully-featured, enterprise-grade ride-sharing desktop application. It was designed to demonstrate advanced software engineering principles, including multi-tier architecture, object-oriented persistence, web service exposure, and rigorous automated testing.

## Core features

* **Role-Based System:** Distinct workflows for Drivers (create rides, manage cars, accept passengers), Passengers (search rides, book seats, manage wallet), and Administrators (handle complaints).
* **Complete Booking Lifecycle:** Manages the state of rides (Pending, Finished, Cancelled) and booking requests (`Eskaera`), including financial transactions, 150% balance pre-checks, and automated refunds.
* **Feedback & Moderation:** Built-in system for 1-5 star ratings (`Balorazio`) and a robust complaint management system (`Erreklamazioa`) with configurable severity penalties (1.1x to 1.5x multipliers).
* **Internationalized GUI:** Comprehensive Java Swing interface with runtime language switching (English, Basque, Spanish) using `ResourceBundle`.

## Architecture & Technologies

The system is built on a strict four-tier architecture, capable of running in both local and remote modes:

1. **Presentation Layer (GUI):** Java Swing forms managing user interaction and i18n localization.
2. **Business Logic Layer (`BLFacade`):** A facade pattern orchestrating workflows and enforcing business rules. In remote mode, this layer is exposed as a **SOAP Web Service (JAX-WS)**.
3. **Data Access Layer (`DataAccess`):** A dedicated DAO managing database connections and JPQL queries.
4. **Persistence Layer:** **ObjectDB**, a high-performance object-oriented database.

## Quality Assurance & DevOps

A major focus of this project is code quality and reliability:

* **Extensive Testing Strategy:** The suite includes both White-box and Black-box testing, utilizing **Mockito** for isolated unit tests and a custom testing framework (`TestBusinessLogic`/`TestDataAccess`) for integration tests against the database.
* **CI/CD Pipeline:** Automated via **GitHub Actions** (Maven builds) and integrated with **SonarCloud** for continuous static code analysis and JaCoCo coverage reporting.

## What I learned

This project represents a culmination of enterprise Java development skills. I gained deep experience in designing complex state machines for business entities, managing object-oriented databases with JPA/JPQL, exposing backend logic via SOAP web services, and establishing a professional-grade testing and CI/CD environment to maintain a large codebase.
