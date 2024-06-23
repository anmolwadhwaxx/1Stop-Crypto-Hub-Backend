# 1Stop Crypto Hub Backend

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=JSON%20web%20tokens&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)

## Overview

The 1Stop Crypto Hub Backend is a robust and secure backend service for managing fiat and cryptocurrency payments. It is built with Java and Spring Boot, leveraging JWT for authentication and PostgreSQL for data storage.

## Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
  - [Installation](#installation)
  - [Configuration](#configuration)
  - [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)
  - [User Management](#user-management)
  - [Payment Processing](#payment-processing)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)
- [License](#license)

## Features

- **User Authentication**: Secure user authentication with JWT.
- **Fiat and Crypto Payments**: Handle transactions in both fiat and cryptocurrencies.
- **Scalability**: Designed to scale with microservice architecture.
- **Security**: Implements best practices for security.

## Getting Started

### Installation

1. **Clone the Repository**
    ```bash
    git clone https://github.com/anmolwadhwaxx/1Stop-Crypto-Hub-Backend.git
    cd 1Stop-Crypto-Hub-Backend
    ```

2. **Install Dependencies**
    Ensure you have Java, Maven, and PostgreSQL installed on your machine.

### Configuration

1. **Database Configuration**
    Set up your PostgreSQL database and update the `application.properties` file with your database credentials.
    ```properties
    spring.datasource.url=jdbc:postgresql://localhost:5432/yourdatabase
    spring.datasource.username=yourusername
    spring.datasource.password=yourpassword
    ```

2. **JWT Configuration**
    Update the `application.properties` file with your JWT secret key.
    ```properties
    jwt.secret=your_jwt_secret_key
    ```

### Running the Application

1. **Build the Project**
    ```bash
    mvn clean install
    ```

2. **Run the Project**
    ```bash
    mvn spring-boot:run
    ```

## API Endpoints

### User Management

- **Register User**
    ```
    POST /api/auth/register
    {
        "username": "example",
        "password": "password123"
    }
    ```

- **Login User**
    ```
    POST /api/auth/login
    {
        "username": "example",
        "password": "password123"
    }
    ```

### Payment Processing

- **Initiate Fiat Payment**
    ```
    POST /api/payments/fiat
    {
        "amount": 100.00,
        "currency": "USD",
        "recipient": "recipient@example.com"
    }
    ```

- **Initiate Crypto Payment**
    ```
    POST /api/payments/crypto
    {
        "amount": 0.01,
        "currency": "BTC",
        "recipient": "recipient_crypto_address"
    }
    ```

## Technologies Used

- **Java**
- **Spring Boot**
- **PostgreSQL**
- **JWT**

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
