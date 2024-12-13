🌐 BRB Company Management Microservice

✨ Overview

Welcome to the BRB Company Management Microservice — the heart of BRB's salon management platform. This microservice is designed to streamline company operations, including salon management, employee scheduling, and service bookings.

🏙️ Microservice Architecture

graph TD
    A[API Gateway] --> B[Company Service]
    B --> C[MongoDB]
    B <--> D[User Service]
    B <--> E[Booking Service]
    B <--> F[Payment Service]
    B <--> G[AI Revenue Service]

🔗 Service Dependencies

User Service: Handles authentication and user management.

Booking Service: Manages appointment scheduling.

Payment Service: Processes transactions securely.

AI Revenue Service: Provides revenue predictions.

Storage Service: Manages file storage.
