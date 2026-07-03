# 💳 Payment Gateway Integration using Spring Boot & Razorpay

A full-stack **Payment Gateway** application built with **Spring Boot**, **Spring Data JPA**, **MySQL**, and **Razorpay**. The application allows users to make secure online payments and stores payment details in a MySQL database. It also supports email notifications after successful payments.

---

## 🚀 Features

- 💳 Razorpay Payment Integration
- 📦 Create Payment Orders
- ✅ Verify Payment Status
- 🗄️ Store Payment Details in MySQL
- 📧 Email Notification after Successful Payment
- 🔄 REST APIs for Payment Processing
- 📊 Hibernate & Spring Data JPA Integration

---

## 🛠️ Tech Stack

### Backend
- Java 21
- Spring Boot
- Spring MVC
- Spring Data JPA
- Hibernate
- Maven

### Database
- MySQL

### Payment Gateway
- Razorpay Java SDK

### Email
- Spring Boot Mail

---

## 📂 Project Structure

```
Payment-Gateway
│── src
│   ├── main
│   │   ├── java
│   │   ├── resources
│   │   │   ├── static
│   │   │   ├── templates
│   │   │   └── application.properties
│── pom.xml
│── mvnw
│── README.md
```

---

## ⚙️ Prerequisites

- Java 21+
- Maven
- MySQL Server
- Razorpay Test Account
- Gmail Account (for email service)

---

## 📥 Installation

### 1. Clone the repository

```bash
git clone <repository-url>
```

### 2. Navigate to project

```bash
cd Payment-Gateway
```

### 3. Create MySQL Database

```sql
CREATE DATABASE pay;
```

---

## 🔧 Configure `application.properties`

Update the following values before running the project.

### Database

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/pay?createDatabaseIfNotExist=true
spring.datasource.username=YOUR_USERNAME
spring.datasource.password=YOUR_PASSWORD
```

### Razorpay

```properties
razorpay.key_id=YOUR_KEY_ID
razorpay.key_secret=YOUR_SECRET
```

### Email

```properties
spring.mail.username=YOUR_EMAIL
spring.mail.password=YOUR_APP_PASSWORD
```

> **Important:** Never commit real API keys, database passwords, or email credentials to GitHub. Replace them with environment variables or placeholder values before pushing your project.

---

## ▶️ Run the Application

Using Maven

```bash
mvn spring-boot:run
```

Or

```bash
./mvnw spring-boot:run
```

---

## 💾 Database

The application automatically creates the required tables using Hibernate.

```properties
spring.jpa.hibernate.ddl-auto=update
```

---

## 📦 Maven Dependencies

- Spring Boot Web MVC
- Spring Data JPA
- MySQL Connector
- Razorpay Java SDK
- Spring Boot Mail
- Lombok

---

## 🔄 Payment Flow

1. User enters payment details.
2. Spring Boot creates a Razorpay Order.
3. Razorpay Checkout opens.
4. User completes the payment.
5. Payment response is received.
6. Payment details are stored in MySQL.
7. Confirmation email is sent to the user.

---

## 📸 Screenshots

Add screenshots of:

- Home Page
- Payment Form
- Razorpay Checkout
- Successful Payment Page
- Database Records

---

## 🔐 Security Recommendations

- Store API keys using environment variables.
- Never expose Razorpay Secret Key.
- Verify payment signatures before marking payments as successful.
- Use HTTPS in production.
- Validate all incoming requests.

---

## 📈 Future Enhancements

- User Authentication (Spring Security)
- Payment History Dashboard
- Refund Support
- Multiple Payment Providers
- Payment Analytics
- Admin Panel
- Docker Deployment
- CI/CD Pipeline

---

## 👨‍💻 Author

**Sanket Dudhade**

---

## 📄 License

This project is intended for educational and learning purposes.
