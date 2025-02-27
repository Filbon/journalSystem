# journalSystem

Overview

This project is a microservices-based medical journal system designed for handling patient information. Initially developed as a monolithic system, it was later broken down into multiple services with additional functionalities, including image handling, search capabilities, and secure authentication.

The system consists of:

    Backend: Spring Boot (REST API)
    Frontend: React.js
    Database: MySQL/PostgreSQL (or HAPI-FHIR for higher-grade implementation)
    Containerization & Orchestration: Docker & Kubernetes
    Additional Services:
        Node.js Service: Image storage & annotation
        Quarkus Service: Search functionality
        Keycloak: Authentication & authorization
        Apache Kafka (for stream-based communication in the advanced implementation)

        Microservices Architecture
Service	Technology	Description
backend-service	Spring Boot	Core logic: Handles patient records, observations, encounters, and messaging.
frontend	React.js	User interface for doctors, patients, and staff.
image-service	Node.js	Stores and allows annotation of medical images.
search-service	Quarkus	Enables searching for patients, conditions, and practitioner histories.
auth-service	Keycloak	Manages authentication and API authorization.
event-service	Apache Kafka	(Advanced) Enables streaming-based communication between services.
