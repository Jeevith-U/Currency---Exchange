
# Currency-Exchange
This project is built using the latest version of Spring Boot and demonstrates a microservices architecture for a financial application. The system is composed of several distinct services, each responsible for a specific functionality within the application. The services interact with each other to provide a seamless user experience.

### Currency Exchange Service
The Currency Exchange Service is responsible for managing and providing real-time exchange rates between different currencies. It exposes RESTful APIs that allow clients to query exchange rates for a given currency pair. The service is designed to be highly available and scalable, ensuring that it can handle high volumes of requests efficiently.

### Currency Conversion Service
The Currency Conversion Service leverages the Currency Exchange Service to perform currency conversions. It takes the amount and currency pair as input, fetches the current exchange rate from the Currency Exchange Service, and returns the converted amount. This service is essential for applications that require real-time currency conversions.

###  API Gateway
The API Gateway acts as a single entry point for all client requests. It routes requests to the appropriate microservice and handles cross-cutting concerns such as security, rate limiting, and request logging. By centralizing these concerns, the API Gateway simplifies the architecture and improves the manageability of the system.

###  Naming Service (Eureka)
The Naming Service, implemented using Netflix Eureka, is responsible for service discovery. In a microservices architecture, services need to be able to discover each other dynamically as they scale up or down. Eureka provides this capability, allowing services to register themselves and discover other services without hardcoding network locations.

###  Monitoring and Logging with Micrometer
For monitoring and logging, the project integrates Micrometer, a powerful instrumentation library. Micrometer provides a consistent API for collecting metrics across different components of the system. It is configured to work with popular monitoring systems like Prometheus and Grafana, enabling real-time monitoring of application performance, health checks, and logs.
