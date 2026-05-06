# Product Catalog

A full-stack e-commerce product catalog built with **Spring Boot** and **React**. Browse products, filter by category, search by name, and sort by price.

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Java 17, Spring Boot 3.5, Spring Data JPA |
| Database | MySQL |
| Frontend | React 19, Vite, React Bootstrap |

---

## Features

- Browse products displayed in a responsive card grid
- Filter products by category
- Search products by name
- Sort by price (ascending / descending)
- Data seeded automatically on first startup

---

## Project Structure

```
ProductCatalog/
├── src/main/java/com/ecom/productcatalog/
│   ├── model/          # JPA entities (Product, Category)
│   ├── repository/     # Spring Data repositories
│   ├── service/        # Business logic
│   ├── controller/     # REST controllers
│   └── config/         # Data seeder
├── src/main/resources/
│   └── application.properties
└── ecom-catalog-react/ # React frontend
    └── src/
        ├── App.jsx
        ├── ProductList.jsx
        └── CategoryFilter.jsx
```

---

## Getting Started

### Prerequisites

- Java 17+
- Maven
- MySQL
- Node.js & npm

### 1. Database setup

Create a MySQL database:

```sql
CREATE DATABASE `product-catalog`;
```

### 2. Backend

Update credentials in `src/main/resources/application.properties` if needed:

```properties
spring.datasource.username=root
spring.datasource.password=yourpassword
```

Then run:

```bash
./mvnw spring-boot:run
```

The API will be available at `http://localhost:8080`. Sample categories and products are seeded automatically on startup.

### 3. Frontend

```bash
cd ecom-catalog-react
npm install
npm run dev
```

The app will be available at `http://localhost:5173`.

---

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/products` | Get all products |
| GET | `/api/categories` | Get all categories |