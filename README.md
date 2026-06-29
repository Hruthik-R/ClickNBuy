# ClickNBuy – Full Stack E-Commerce Web Application

ClickNBuy is a **full stack e-commerce web application** developed using Java Full Stack technologies. It provides a complete online shopping experience where users can browse products, manage carts, place orders, and track purchases, while administrators can manage products and system operations.

The application follows the **MVC (Model-View-Controller)** architecture for clean separation between frontend, backend, and database layers.

---

## Features

### User Features

* User registration and login
* Secure authentication and authorization
* Browse and search products
* Add/remove items from cart
* Update product quantity in cart
* Checkout and order placement
* View order history
* Responsive shopping experience

### Admin Features

* Add new products
* Update product details
* Delete products
* Manage product inventory
* Manage customer orders

### System Features

* Role-based access control (Admin/User)
* Secure endpoint protection
* Product image upload support
* Database persistence
* Email service integration

---

## Tech Stack

### Backend

* Java
* Spring Boot
* Spring MVC
* Spring Security
* Spring Data JPA
* Maven

### Frontend

* Thymeleaf
* HTML
* CSS
* JavaScript
* Bootstrap

### Database

* MySQL

### Tools

* Postman
* Git
* GitHub
* VS Code / Eclipse

---

## Architecture

The project follows **MVC Architecture**:

```text id="x0g2ku"
View (Thymeleaf + HTML/CSS/JS)
        ↓
Controller (Spring MVC)
        ↓
Service Layer
        ↓
Repository Layer (JPA)
        ↓
MySQL Database
```

---

## Project Structure

```bash id="ab7g8j"
ClickNBuy/
│
├── src/
│   ├── main/
│   │   ├── java/
│   │   └── resources/
│   │       ├── templates/
│   │       ├── static/
│   │       └── application.properties
│   └── test/
│
├── uploads/
├── pom.xml
├── mvnw
└── mvnw.cmd
```

---

## Prerequisites

Install the following before running:

* Java 17+
* MySQL
* Git
* Maven (optional, wrapper included)

---

## Clone Repository

```bash id="j4f8xa"
git clone https://github.com/YOUR_USERNAME/clickNbuy.git
cd clickNbuy
```

Replace `YOUR_USERNAME` with your GitHub username.

---

## Configuration

Create the configuration file:

```bash id="6b0y6g"
src/main/resources/application.properties
```

Copy values from:

```bash id="lm0yoa"
src/main/resources/application-example.properties
```

Fill in:

* Database credentials
* Email credentials
* API keys (optional)

---

## Database Setup

Start MySQL and create database:

```sql id="s4uy43"
CREATE DATABASE clicknbuy;
```

---

## Run Application

### Windows

```bash id="5np0ae"
mvnw.cmd spring-boot:run
```

### Linux / Mac

```bash id="k8iqx2"
./mvnw spring-boot:run
```

Application runs at:

```bash id="j4ihue"
http://localhost:8080
```

---

## Main Modules

### Authentication Module

* User registration
* Login
* Role-based access control
* Session management

### Product Module

* Product listing
* Product details
* Search and filtering
* Product CRUD operations

### Cart Module

* Add items
* Remove items
* Quantity update
* Dynamic total calculation

### Checkout Module

* Delivery details
* Order confirmation
* Payment simulation

### Orders Module

* Order history
* Order details
* Payment status tracking

---

## File Upload

Product images are stored in:

```bash id="2l4m64"
uploads/products
```

Maximum upload size:

* 10 MB per file
* 10 MB per request

---

## API Testing

APIs can be tested using:

* Postman
* Thunder Client

Example:

```http id="u4kyw7"
GET /products
```
---

## Security Note

The following files are excluded from Git:

* `application.properties`
* `.env`
* API keys
* Database passwords
* Email credentials

Never commit secrets to GitHub.