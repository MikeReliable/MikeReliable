## 👋 Hi, I'm a Java Backend / Microservices Developer

I specialize in building scalable, secure, and event-driven microservices using the Java ecosystem.
My focus is on designing robust distributed systems with clean architecture, reliable messaging, and production-ready patterns.

---

### 🛠 Core Stack
- **Java:** 8 / 11 / 17
- **Spring:** Boot, Security (OAuth2, JWT), Data JPA, Cloud Gateway, Cloud OpenFeign
- **Architecture:** Microservices, REST, Event-driven Design, Transactional Outbox, Idempotent APIs
- **Security:** JWT (RS256), OAuth2 Resource Server, RBAC, JWKS endpoint
- **Messaging:** Apache Kafka, Spring Kafka, Event streaming, Consumer groups, RabbitMQ
- **Databases:** PostgreSQL, MySQL, Hibernate, Liquibase migrations
- **Testing:** JUnit 5, Mockito, Testcontainers, Awaitility, AssertJ
- **DevOps:** Maven, Gradle, Docker, Docker Compose
- **Observability:** Correlation-ID, structured logging, distributed tracing
- **VCS:** Git, GitHub

---

### 📌 Featured Projects

🔹 **Distributed Banking Platform**

[GitHub Repository](https://github.com/MikeReliable/distributed-banking-platform)  
A production‑like microservices system simulating core banking operations with **event‑driven architecture** and strong focus on **data consistency**, **security**, and **reliability**.

- **Key features implemented:**
- **Authentication & Authorization** – Stateless JWT (RS256) issued by a dedicated auth‑service, JWKS endpoint for public key distribution.
- **Transactional Outbox Pattern** – Reliable event publishing without dual‑write problems (used in auth‑, user‑, and card‑services).
- **Idempotent Operations** – `Idempotency-Key` header support for financial operations (transfers, top‑up, withdraw) to guarantee safe retries.
- **Optimistic Locking** – `@Version` based concurrency control on accounts to prevent lost updates.
- **Event‑Driven User Lifecycle** – Registration triggers `USER_REGISTERED` → user‑service creates profile → `USER_CREATED` → card‑service creates default card → `CARD_CREATED` → transfer‑service creates accounts.
- **Distributed Tracing** – `X-Request-Id` propagation through MDC, Feign interceptors, and persisted in Outbox events.
- **Native SQL Analytics** – Complex reporting endpoints (turnover, top transfers) using native queries with joins and aggregations.
- **Domain‑Driven Exceptions** – Custom exceptions returning consistent JSON error responses.
- **API Gateway** – Single entry point with Spring Cloud Gateway, route definitions, and centralized Swagger UI (`http://localhost:8080/swagger-ui.html`).
- **Containerized Environment** – Full Docker Compose setup with PostgreSQL, Kafka, and all microservices.
- **Tech stack:** Java 17, Spring Boot 3, Spring Cloud Gateway, Spring Security OAuth2, JWT, Kafka, PostgreSQL, Liquibase, Testcontainers, Docker.

🔹 **Spring Microservice App**  
This project presents microservice architecture based on interaction via the **gRPC** and **Kafka**.

🔹 **Library Demo**  
A classic CRUD application simulating a library system – clean REST API, layered architecture, and basic persistence with Spring Data JPA.

---

### 💼 Experience Highlights
- Designed and implemented microservices from scratch, applying Domain‑Driven Design principles
- Built secure REST APIs with JWT authentication and role‑based access control
- Integrated reliable messaging using Kafka with the Outbox pattern to ensure data consistency across services
- Implemented idempotent endpoints to safely handle retries in financial operations
- Ensured concurrency safety with optimistic locking and database transactions
- Managed database schemas and migrations using Liquibase
- Collaborated in code reviews, promoted clean code practices
