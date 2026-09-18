# Expense Tracker Web Application 💰

A containerized expense management application built with **Java, Spring Boot, Spring Security, MySQL, Thymeleaf, and Docker**.

The application allows authenticated users to manage and track expenses through a web interface while demonstrating a multi-container deployment using Docker Compose.

## 🛠️ Technologies

`Java` `Spring Boot` `Spring Security` `Spring Data JPA` `MySQL` `Docker` `Docker Compose` `Thymeleaf` `Bootstrap` `Maven`

## ✨ Features

- User authentication and authorization
- Create, view, update, and delete expenses
- Filter and organize expense records
- Persistent MySQL database storage
- Containerized application deployment
- Database health checks and service dependencies

## 🏗️ Architecture

```text
User
  ↓
Spring Boot Application
  ↓
Spring Data JPA
  ↓
MySQL Database
```

Docker Compose orchestrates the application and database containers on a dedicated Docker network.

## 🚀 Run with Docker Compose

Clone the repository:

```bash
git clone https://github.com/keshav2613/Expenses-Tracker-WebApp.git
cd Expenses-Tracker-WebApp
```

Create your environment file:

```bash
cp .env.example .env
```

Update the database password in `.env`, then start the application:

```bash
docker compose up --build -d
```

Access the application at:

```text
http://localhost:8080
```

Stop the environment:

```bash
docker compose down
```

## 🔐 Configuration

Sensitive configuration is supplied through environment variables rather than committed directly to the repository.

Example:

```text
MYSQL_ROOT_PASSWORD=change-me
```

## 🐳 Containerized Deployment

The Docker Compose environment contains:

- **expenses-app** — Spring Boot application
- **expenses-mysql** — MySQL 8 database
- Persistent database volume
- Internal Docker network
- MySQL health check before application startup

## 📸 Application Screenshots

Screenshots of the application interface are available in the [`screenshots`](screenshots/) directory.

## 📄 License

This project is licensed under the MIT License.
