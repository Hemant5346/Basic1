BRB Company Management Microservice

✨ Overview

The Company Management Microservice is a core component of BRB's salon management platform. This service facilitates company-related operations, including salon management, employee scheduling, and service bookings.

🏙️ Microservice Architecture

graph TD
    A[API Gateway] --> B[Company Service]
    B --> C[MongoDB]
    B <--> D[User Service]
    B <--> E[Booking Service]
    B <--> F[Payment Service]
    B <--> G[AI Revenue Service]

🔗 Service Dependencies

User Service - Authentication and user management

Booking Service - Appointment scheduling

Payment Service - Transaction processing

AI Revenue Service - Revenue predictions

Storage Service - File management

🛠️ Tech Stack

Framework: NestJS v10

Runtime: Node.js ≥20.16.0

Database: MongoDB with Mongoose ODM

API: REST with Fastify

Documentation: Swagger/OpenAPI

Testing: Jest

CI/CD: GitHub Actions

📌 Prerequisites

"engines": {
    "npm": ">=10.5.0",
    "node": ">=20.16.0"
}

🚀 Quick Start

Installation

# Install dependencies
yarn install

Configuration

Create a .env file with the following content:

# App
APP_PORT=3000
APP_PREFIX=api/v1
APP_HOST_SERVER=http://localhost:3000

# MongoDB
MONGO_PREFIX=mongodb
MONGO_URL=localhost:27017
MONGO_DB=brb_company_db

# Service URLs
USER_SERVICE_URL=http://localhost:3001
BOOKING_SERVICE_URL=http://localhost:3002
PAYMENT_SERVICE_URL=http://localhost:3003

# JWT
JWT_SECRET=your_secret
JWT_EXPIRE=24h

Development

# Local development
yarn start:dev

# Production build
yarn build
yarn start:prod

📒 Core Features

Company Management

Salon profile management

Business settings

Location management

Revenue tracking

Employee Management

Staff profiles

Schedule management

Service assignments

Performance tracking

Service Catalog

Service management

Category organization

Pricing configuration

Availability control

🔒 Security

JWT Authentication

Role-Based Access Control (RBAC)

Request validation

Rate limiting

🔮 Testing

# Unit tests
yarn test

# End-to-End (E2E) tests
yarn test:e2e

# Test coverage
yarn test:cov

📂 Project Structure

src/
├── app.module.ts
├── main.ts
├── common/
│   ├── config/
│   ├── decorators/
│   ├── guards/
│   └── interservices/
└── modules/
    ├── company/
    ├── employee/
    ├── service/
    └── location/

⟳ CI/CD Pipeline

Automated testing

Code quality checks

Docker image building

Automated deployment

📚 API Documentation

Access the API documentation via Swagger at:

http://localhost:3000/api/docs

🐳 Docker Support

Build and Run the Docker Image

# Build image
docker build -t brb-company-service .

# Run container
docker-compose up

💻 Contributing

Follow BRB's coding standards

Write clear and concise commit messages

Include tests for new features

Update documentation as needed

📘 License

Proprietary - BRB © 2024

🤝 Support

For internal support, reach out via:

Slack: #company-service-support

Email: support@brb.com

Confluence: Company Service Wiki

Note: This is a private repository. For access, please contact the BRB DevOps team.

