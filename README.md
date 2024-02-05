# API Gateway Service
Welcome to the API Gateway Service! This service acts as an entry point for clients to interact with various microservices within the airline booking management system. It handles routing requests to the appropriate microservices and provides additional functionalities such as rate limiting and authentication.

# Features
1. Request Logging: The service utilizes the morgan middleware for request logging, providing detailed information about incoming requests.

2. Rate Limiting: Rate limiting is implemented to control the rate of incoming requests and prevent abuse or overload of the system.

3. Authentication Middleware: Requests to certain routes are authenticated using an authentication middleware. It verifies the validity of the access token before allowing access to protected resources.

4. Proxying Requests: Requests to different microservices are proxied based on the route path, ensuring that each request is routed to the appropriate microservice.

## Endpoints
Home: GET /home - A test endpoint to check if the API Gateway Service is running successfully.

## Middlewares
1. Rate Limiting Middleware: Controls the rate of incoming requests using the express-rate-limit middleware.

2. Authentication Middleware: Validates the access token before allowing access to protected resources.

## External Dependencies
1. http-proxy-middleware: Used for creating proxy middleware to forward requests to other microservices.

2. axios: Used for making HTTP requests to authenticate access tokens with the authentication service.
