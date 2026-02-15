# ecom-discovery-server

A Spring Boot microservice that runs a Netflix Eureka Discovery Server for the ecom platform. Other microservices register themselves with this server for service discovery.

## Configuration

- **Port**: 8761 (default Eureka port)
- **Self-registration**: Disabled (standalone server)
- **Self-preservation**: Disabled (suitable for development)

## Build and Run

```bash
mvn clean package
java -jar target/ecom-discovery-server-0.0.1-SNAPSHOT.jar
```

## Docker

```bash
mvn clean package -DskipTests
docker build -t ecom-discovery-server .
docker run -p 8761:8761 ecom-discovery-server
```

The Eureka dashboard is available at `http://localhost:8761`.
