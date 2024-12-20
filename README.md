# Distributed Application with Microservices

This repository contains a distributed application developed using a microservices architecture. The system consists of multiple independent services, each responsible for a specific functionality, and is implemented using Java Spring Boot. The project also incorporates monitoring, logging, and containerization tools.

---

## **Project Overview**

### **Services**
1. **api-gateway**: 
   - Acts as the entry point to the system.
   - Routes requests to the appropriate microservices.
   - Handles authentication and request throttling.

2. **discovery-server**:
   - Service registry and discovery using Spring Cloud Netflix Eureka.
   - Allows services to register themselves and discover other services dynamically.

3. **inventory-service**:
   - Manages product inventory and stock levels.

4. **notification-service**:
   - Handles notifications (e.g., emails, SMS) for order updates and system events.

5. **order-service**:
   - Responsible for processing orders, including creating, updating, and tracking orders.

6. **product-service**:
   - Manages product catalog, including product details and availability.

---

## **Technologies Used**
- **Java Spring Boot**: Core framework for building microservices.
- **Docker**: Containerization of all microservices for consistent deployments.
- **Azure**: Cloud infrastructure for hosting services.
- **Logstash**: Centralized logging and event collection.
- **Kibana**: Visualization of logs and metrics for system monitoring.
- **Spring Cloud Netflix**: Service discovery and API Gateway implementation.
- **Kafka (Optional)**: For inter-service asynchronous communication.

---

## **How to Run Locally**

1. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd <repository-folder>
Build the Services Use Maven to build the Spring Boot services:

bash
Copy code
mvn clean install
Start the Services Run each service using Docker Compose or start them manually using Spring Boot:

bash
Copy code
docker-compose up
Or manually:

bash
Copy code
java -jar target/<service-name>.jar
Access the Application

API Gateway: http://localhost:8080
Service Registry (Eureka): http://localhost:8761
Key Features
Microservices Architecture:

Independent services communicating over REST APIs.
Scalability and fault isolation.
Centralized Logging:

Logstash and Kibana integration for log aggregation and visualization.
Cloud Deployment:

Deployed and managed using Azure services.
Containerization:

All services are containerized using Docker for consistent deployments.
Resilience and Service Discovery:

Eureka server for dynamic service registration and discovery.
Circuit breakers for fault tolerance.
Folder Structure
api-gateway: Contains the gateway service code.
discovery-server: Contains the Eureka service discovery server code.
inventory-service: Handles inventory management logic.
notification-service: Manages notifications.
order-service: Handles order processing logic.
product-service: Manages product catalog and availability.
Monitoring and Logging
Logstash:

Collects and processes logs from all microservices.
Kibana:

Visualizes logs and metrics for performance monitoring.
Deployment
This application is designed to be deployed on Azure:

Container Registry: Push Docker images to Azure Container Registry.
Kubernetes Cluster: Deploy and manage the microservices using Azure Kubernetes Service (AKS).
Monitoring: Use Azure Monitor for real-time application insights.
Contributions
Contributions are welcome! Please fork this repository and submit a pull request.

License
This project is licensed under the MIT License.