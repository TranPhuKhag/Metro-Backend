# Metro-Backend 🚇

A comprehensive microservice architecture for Metro (Subway) Ticketing management system built with Java Spring Boot.

## 🔗 Demo & Links
- **Live Demo**: [https://metro.anhtudev.works/](https://metro.anhtudev.works/)
- **Video Demo**: [YouTube Playlist](http://www.youtube.com/playlist?list=PLlolFUWzABBn56QjcVsYl5H4e6DBpEp0h)

## 🏗️ Microservices Architecture

### Core Services

| Service | Port | Main Functions | Technologies |
|---------|------|----------------|-------------|
| **User Service** | 8080 | User management, authentication, role-based access control | Spring Boot, OAuth2, JWT |
| **Route Service** | 8081 | Metro routes, stations, bus connections management | Spring Boot, JPA |
| **Ticket Service** | 8082 | Ticket types, pricing, validation | Spring Boot, Spring Security |
| **Order Service** | 8083 | Ticket purchasing, order processing, payment handling | Spring Boot, Transaction Management |
| **Notification Service** | 8084 | Email notifications, OTP verification, welcome messages | Spring Boot, Thymeleaf, Mail Service |
| **Content Service** | 8085 | News, announcements, content management | Spring Boot, File Upload |

### Shared Libraries
- **Common-Lib**: Shared entities, DTOs, utilities across all services

## 🚀 Quick Start

### Prerequisites
- Java 17+
- Docker & Docker Compose
- Maven 3.6+
- MySQL/PostgreSQL

### Setup & Run
```bash
# Clone repository
git clone https://github.com/anhtu2808/Metro-Backend.git
cd Metro-Backend

# Start all services with Docker Compose
docker-compose up -d

# Or run individual service
cd user-service
./mvnw spring-boot:run
```

## 📱 Key Features

### 🔐 User Management
- User registration/login with JWT authentication
- Role-based access control (Admin, User, Staff)
- OAuth2 integration
- Email verification with OTP

### 🚇 Route & Station Management
- Metro line and station information
- Bus route connections to metro stations
- Real-time route planning
- Distance and time calculations

### 🎫 Ticketing System
- Multiple ticket types (Single, Daily, Monthly passes)
- Dynamic pricing based on distance
- QR code generation for tickets
- Ticket validation and status tracking

### 📦 Order Processing
- Secure payment processing
- Order history and tracking
- Refund and cancellation handling
- Real-time order status updates

### 📧 Notification System
- Welcome emails for new users
- OTP verification for password reset
- Order confirmation notifications
- System announcements

### 📰 Content Management
- News and announcements
- Service updates
- Image gallery management
- Content scheduling

## 🛠️ Tech Stack

- **Backend**: Spring Boot 3.2.5, Spring Cloud
- **Security**: Spring Security, OAuth2, JWT
- **Database**: JPA/Hibernate, MySQL
- **Messaging**: Apache Kafka, Spring Cloud Stream  
- **Communication**: OpenFeign for inter-service calls
- **Containerization**: Docker, Multi-stage builds
- **Email**: Spring Mail with Thymeleaf templates

## 🔧 Configuration

Each service has its own `application.yml` for configuration:
```yaml
server:
  port: 808X
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/metro_db
  kafka:
    bootstrap-servers: localhost:9092
```

## 📊 Database Schema

Services use separate databases following database-per-service pattern:
- `metro_user` - User service data
- `metro_route` - Route and station data  
- `metro_ticket` - Ticket information
- `metro_order` - Order and transaction data
- `metro_content` - Content management data

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/new-feature`)
3. Commit changes (`git commit -m 'Add new feature'`)
4. Push to branch (`git push origin feature/new-feature`)
5. Create Pull Request

## 📄 License

This project is licensed under the MIT License.

## 👨‍💻 Author

**Anh Tu** - [@anhtu2808](https://github.com/anhtu2808)

---
*Built with ❤️ for Ho Chi Minh City Metro System*
