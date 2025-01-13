# Algonquin Pet Store

Welcome to the **Algonquin Pet Store** application! This app will help you learn about how modern web applications work by combining several technologies into a working system. The application is built using microservices architecture, which means that different parts of the app work independently but communicate with each other. Here's what it includes:

- **Store Front (Vue.js):** The user interface where customers can browse and buy products.
- **Order Service (Node.js):** Handles customer orders and communicates with other parts of the system.
- **Product Service (Rust):** Manages product details like names, prices, and inventory.
- **RabbitMQ:** A tool that helps different parts of the app communicate smoothly by sending messages.

![App UI](./Docs/app-ui.png)

## Table of Contents

1. [Architecture Overview](#architecture-overview)
2. [Setup](#setup)
   - [RabbitMQ](#rabbitmq) 
   - [Order Service](#order-service)
   - [Product Service](#product-service)
   - [Store-Front](#store-front)
3. [Running the Full Application](#running-the-full-application)

---

## Architecture Overview

![App Architecture](./Docs/app-architecture.png)

The app uses a microservices architecture. This means that different parts of the app (called "services") do specific jobs and talk to each other to get things done. Here's how they fit together:

- **Store Front (Vue.js)**: A front-end application where customers can browse and order products.
- **Order Service (Node.js)**: Manages customer orders and interacts with RabbitMQ for message queuing.
- **Product Service (Rust)**: Handles product listings. Manages product details and inventory.
- **RabbitMQ**: Message broker for communication between services. Used to queue orders for processing.
## Setup
### RabbitMQ

Follow the instructions in the [RabbitMQ README](RabbitMQ/README.md) to get RabbitMQ running locally.

### Order-Service

Navigate to the `order-service` folder and follow the instructions in its [Order-Service README](order-service/README.md).

### Product-Service

Navigate to the `product-service` folder and follow the instructions in its [Product-Service README](product-service/README.md).

### Store-Front

Navigate to the `store-front` folder and follow the instructions in its [Store-Front README](store-front/README.md).

## Running the Full Application

Once all the services are running:

- Open your browser and go to http://localhost:8080 to see the store front.
- The store front will show product listings from the Product Service.
- When you place an order, it will be processed by the Order Service, and RabbitMQ will handle the messaging.

That's it! You're now ready to use and explore the Algonquin Pet Store application. 🎉
