# Instabackend
Instabackend is a Java Spring Boot-based backend service designed to handle the backend operations of an Instagram-like application. This project covers functionalities such as user management, post management, comment handling, and more.

# Table of Contents
* Features
* Technologies
* Prerequisites
* Installation
* Configuration
* Usage
* API Endpoints
* Testing
* Contributing

# Features
User registration and authentication
User profile management
Post creation, deletion, and retrieval
Commenting on posts
Like and unlike functionality
Follow and unfollow users

# Technologies
Java 11
Spring Boot 2.7
Spring Security
Spring Data JPA
Hibernate
MySQL
Maven
Lombok
Prerequisites
Java 11 or higher
Maven 3.6 or higher
MySQL 8.0 or higher

# Installation
Clone the repository:

sh
Copy code
git clone https://github.com/yourusername/instabackend.git
cd instabackend
Set up MySQL database:

sql
Copy code
CREATE DATABASE instabackend;

# Configure application properties:
Update src/main/resources/application.properties with your MySQL database configuration:

properties
Copy code
spring.datasource.url=jdbc:mysql://localhost:3306/instabackend
spring.datasource.username=yourusername
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
Build the project:

sh
Copy code
mvn clean install
Run the application:

sh
Copy code
mvn spring-boot:run
Configuration
Ensure you configure the following properties in application.properties:

spring.datasource.url: Your MySQL database URL
spring.datasource.username: Your MySQL username
spring.datasource.password: Your MySQL password
spring.jpa.hibernate.ddl-auto: Database schema generation strategy
Optional configurations:

JWT secret and expiration time
Email service configuration for user 

# Usage
Once the application is running, you can use Postman or a similar tool to interact with the API.

API Endpoints
User Management
Register: POST /api/auth/register
Login: POST /api/auth/login
Get Profile: GET /api/users/{username}
Update Profile: PUT /api/users/{username}
Post Management
Create Post: POST /api/posts
Get Posts: GET /api/posts
Delete Post: DELETE /api/posts/{postId}
Like/Unlike
Like Post: POST /api/posts/{postId}/like
Unlike Post: DELETE /api/posts/{postId}/like
Follow/Unfollow
Follow User: POST /api/users/{username}/follow
Unfollow User: DELETE /api/users/{username}/follow

Testing
To run tests, use the following command:

sh
Copy code
mvn test
Contributing
Contributions are welcome! Please follow these steps:

Fork the repository
Create a new branch (git checkout -b feature/YourFeature)
Commit your changes (git commit -am 'Add YourFeature')
Push to the branch (git push origin feature/YourFeature)
Create a new Pull Request
