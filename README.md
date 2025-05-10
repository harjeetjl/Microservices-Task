
# Microservices Dockerized Project

This repository contains four Node.js microservices:

- **User Service** (Port 3000)  
- **Product Service** (Port 3001)  
- **Order Service** (Port 3002)  
- **Gateway Service** (Port 3003)

Each service is containerized using Docker and orchestrated with Docker Compose to enable easy setup and inter-service communication.

## Project Structure

```
submission/
├── user-service/
│   └── Dockerfile
├── product-service/
│   └── Dockerfile
├── order-service/
│   └── Dockerfile
├── gateway-service/
│   └── Dockerfile
├── docker-compose.yml
└── README.md
```

## Prerequisites

- Docker installed on your system  
- Docker Compose installed  
- Git installed 

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/harjeetjl/Microservices-Task.git
cd Microservices-Task/Microservices
```

### 2. Build and Start All Services

```bash
docker-compose up 
```

### Screenshot: Docker Compose Output

```

```


## Services and Endpoints

### User Service
- Base URL: `http://localhost:3000`
- Endpoints:
  - List Users:
    ```bash
    curl http://localhost:3000/users
    ```
    Or open in your browser: [http://localhost:3000/users](http://localhost:3000/users)

---

### Product Service
- Base URL: `http://localhost:3001`
- Endpoints:
  - List Products:
    ```bash
    curl http://localhost:3001/products
    ```
    Or open in your browser: [http://localhost:3001/products](http://localhost:3001/products)

---

### Order Service
- Base URL: `http://localhost:3002`
- Endpoints:
  - List Orders:
    ```bash
    curl http://localhost:3002/orders
    ```
    Or open in your browser: [http://localhost:3002/orders](http://localhost:3002/orders)

---

### Gateway Service
- Base URL: `http://localhost:3003/api`
- Endpoints:
  - Users:
    ```bash
    curl http://localhost:3003/api/users
    ```
  - Products:
    ```bash
    curl http://localhost:3003/api/products
    ```
  - Orders:
    ```bash
    curl http://localhost:3003/api/orders
    ```

---


### Screenshot: Testing Output

```
[Place screenshots here showing browser or Postman requests for each service]
```

## Common Troubleshooting

| Problem                            | Solution                                                 |
|------------------------------------|----------------------------------------------------------|
| Port already in use                | Stop the conflicting process or change port in compose   |                |
| Docker command not found           | Ensure Docker is installed and in system path            |
| Services cannot talk to each other | Ensure correct `depends_on` and service names are used   |

## Stopping the Application

```bash
docker-compose down
```

To stop and remove all containers, networks, and volumes:

```bash
docker-compose down -v
```

## Notes

- All services use the same Docker network by default for internal communication.
- Ensure no services are already occupying ports 3000-3003 on your host machine.
- Make sure each Dockerfile correctly installs dependencies and runs the application.
