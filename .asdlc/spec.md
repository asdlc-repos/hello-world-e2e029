# Overview

A simple HTTP API that returns "Hello, World!" responses. This project serves as a minimal REST API implementation for testing, demonstration, or learning purposes.

# Personas

- **Developer** — Software engineer integrating with or testing the API
- **DevOps Engineer** — Operations team member monitoring API health and performance
- **End User** — Consumer making HTTP requests to the API endpoint

# Capabilities

## Core Functionality

- The system SHALL expose an HTTP endpoint at `/hello` that returns "Hello, World!" in the response body.
- WHEN a GET request is made to `/hello`, the system SHALL respond with HTTP status code 200.
- The system SHALL return responses in plain text format with content-type `text/plain`.
- WHEN a GET request is made to the root path `/`, the system SHALL respond with a welcome message.

## Health & Monitoring

- The system SHALL expose a health check endpoint at `/health` that returns HTTP status code 200.
- WHEN the `/health` endpoint is requested, the system SHALL respond within 100ms.

## Error Handling

- IF an unsupported HTTP method is used on `/hello`, THEN the system SHALL respond with HTTP status code 405.
- IF a request is made to a non-existent endpoint, THEN the system SHALL respond with HTTP status code 404.

## Performance

- The system SHALL handle at least 100 concurrent requests without degradation.
- WHEN a request is received, the system SHALL respond within 200ms under normal load conditions.