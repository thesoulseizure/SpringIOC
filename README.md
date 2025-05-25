# Spring IOC, Beans, and JPA: Product Catalog System

This repository contains a Spring Boot project that implements a Product Catalog System using Spring IOC, Beans, and Spring Data JPA. The project allows users to add products to a catalog and display products by category in a tabular format on a web page.

## Project Structure

- **src/main/java/com/example/demo/**
  - **entity/Product.java**: The JPA entity class for the Product with attributes `name`, `price`, and `category`.
  - **repository/ProductRepository.java**: Spring Data JPA repository interface with a method to fetch products by category.
  - **service/ProductService.java**: Service class to handle business logic for adding and retrieving products.
  - **controller/ProductController.java**: Controller class to handle HTTP requests and render HTML pages.
- **src/main/resources/templates/**
  - **index.html**: The homepage with options to "Add Product" or "Display Product".
  - **add-product.html**: HTML form to add a new product (name, price, category).
  - **display-products.html**: HTML page to display all products in a tabular format.
- **src/main/resources/application.properties**: Configuration file for the database (e.g., H2 in-memory database).
- **pom.xml**: Maven configuration file with dependencies for Spring Boot, Spring Data JPA, Thymeleaf, and H2 database.
- **screenshots/**: Contains screenshots of the project (e.g., homepage.png, add-product.png, display-products.png).

## Task Description

### Q1: Product Catalog System
This task involves creating a web-based Product Catalog System with the following features:
- **Homepage**:
  - A RESTful endpoint (`/`) displays an HTML page with two options:
    1. Add Product
    2. Display Product
- **Add Product**:
  - Clicking "Add Product" navigates to `/add-product`, displaying a form to input:
    - Product Name
    - Price
    - Category
  - Submitting the form saves the product to the database using Spring Data JPA.
- **Display Product**:
  - Clicking "Display Product" navigates to `/display-products`, showing all products in a table.
  - Includes a filter to fetch products by a specific category using a repository method.
- **Backend**:
  - Uses Spring Data JPA to create an entity (`Product`), repository (`ProductRepository`), and service (`ProductService`).
  - Stores product information in a database (H2 in-memory database by default).

## How to Run

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/thesoulseizure/Spring-IOC-Beans.git
   ```
2. **Navigate to the Project Directory**:
   ```bash
   cd Spring-IOC-Beans
   ```
3. **Build the Project**:
   - Ensure you have Maven installed.
   ```bash
   mvn clean install
   ```
4. **Run the Application**:
   ```bash
   mvn spring-boot:run
   ```
5. **Access the Application**:
   - Open a browser and navigate to `http://localhost:8080`.
   - The homepage will display options to add or display products.

## Requirements

- **Java**: JDK 17 or higher.
- **Maven**: For dependency management and building the project.
- **Database**: H2 in-memory database (configured by default; can be changed in `application.properties`).
- **Browser**: To access the web application.

## Screenshots

The repository includes screenshots in the `screenshots/` directory:
- `homepage.png`: Shows the homepage with "Add Product" and "Display Product" options.
- `add-product.png`: Displays the form to add a new product.
- `display-products.png`: Shows the product catalog in a tabular format.

## Technologies Used

- **Spring Boot**: For creating the web application.
- **Spring IOC and Beans**: For dependency injection and bean management.
- **Spring Data JPA**: For database operations.
- **Thymeleaf**: For server-side rendering of HTML templates.
- **H2 Database**: In-memory database for development.
- **Maven**: For project build and dependency management.
