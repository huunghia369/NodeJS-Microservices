# NodeJS Microservices

This project utilizes a microservices architecture built with Node.js, RabbitMQ, and Redis, consisting of the following main services: API Gateway, Identity Service, Post Service, Media Service, and Search Service.

## Key Features

- **API Gateway:** Routes requests to other services.
- **Identity Service:** Handles user authentication and management.
- **Post Service:** Manages posts and content.
- **Media Service:** Handles file uploads and media processing.
- **Search Service:** Provides search functionality.

## `.env` Configuration

### **API Gateway:**
```env
PORT=3000
NODE_ENV=development
IDENTITY_SERVICE_URL=http://localhost:3001
POST_SERVICE_URL=http://localhost:3002
MEDIA_SERVICE_URL=http://localhost:3003
SEARCH_SERVICE_URL=http://localhost:3004
REDIS_URL=redis://localhost:6379
JWT_SECRET=your-jwt-secret
```

### **Other Services:**
```env
PORT=300X  # Change PORT based on the service
MONGODB_URI=mongodb+srv://<username>:<password>@<cluster-url>/<db-name>
JWT_SECRET=your-jwt-secret
NODE_ENV=development
REDIS_URL=redis://localhost:6379
RABBITMQ_URL=amqp://localhost:5672
```

## Deployment Guide

1. **Set up environment:** Install Node.js, Redis, RabbitMQ, and MongoDB.
2. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd <project-directory>
   ```
3. **Install dependencies:**
   ```bash
   npm install
   ```
4. **Create `.env` files:** Fill in the required configuration for each service.
5. **Start the services:**
   ```bash
   npm start
   ```
6. **Verify the system:** Access the API Gateway at `http://localhost:3000`.
