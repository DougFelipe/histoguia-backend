# Histoguia

## Description
**Histoguia** is a backend project developed using **Spring Boot**. It is designed to manage questions, answers, users, and themes with features such as user authentication, role management, and more.

---

## Features
- User registration and authentication.
- Role-based access control (Admin and User roles).
- CRUD operations for questions, answers, and themes.
- JWT-based authentication.
- Basic security configuration with CORS.

---

## Prerequisites
Ensure the following software is installed:
- **Java 17** or higher.
- **Maven**.
- **MySQL** database.

---

## Installation

1. **Clone the Repository**  
   Run the following command in your terminal:  
   ```  
   git clone https://github.com/your-repository-link.git  
   ```  

2. **Navigate to the Project Directory**  
   ```  
   cd histoguia  
   ```  

3. **Configure Database**  
   Update the `application.properties` file located in `src/main/resources` with your database credentials:  
   ```  
   spring.datasource.url=jdbc:mysql://<HOST>:<PORT>/<DATABASE_NAME>  
   spring.datasource.username=<DB_USERNAME>  
   spring.datasource.password=<DB_PASSWORD>  
   ```  

4. **Install Dependencies**  
   Use Maven to install the required dependencies:  
   ```  
   mvn clean install  
   ```  

5. **Run the Application**  
   Start the application using:  
   ```  
   mvn spring-boot:run  
   ```  

---

## Project Structure

### Directory Tree
```
.
├── .gitignore
├── mvnw
├── mvnw.cmd
├── pom.xml
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com
│   │   │       └── histoguia_backend
│   │   │           ├── HistoguiaApplication.java
│   │   │           ├── controller
│   │   │           ├── model
│   │   │           ├── repository
│   │   │           ├── security
│   │   │           ├── seeder
│   │   │           └── service
│   │   └── resources
│   │       └── application.properties
│   └── test
│       └── java
│           └── com
│               └── histoguia_backend
│                   └── HistoguiaApplicationTests.java
```

---

### Important Files

#### `pom.xml`
Defines project dependencies such as:
- Spring Boot Starter Data JPA
- Spring Boot Starter Web
- Spring Boot Starter Security
- MySQL Connector
- Java JWT

#### `application.properties`
Contains application configuration details, such as:
- Database connection details.
- Security settings.

---

## API Endpoints

### Authentication
- **POST** `/api/users/register`: Register a new user.
- **POST** `/api/users/login`: Authenticate a user.

### Questions
- **GET** `/api/questions`: Fetch all questions.
- **POST** `/api/questions`: Create a new question.
- **DELETE** `/api/questions/delete/{id}`: Delete a specific question.
- **PUT** `/api/questions/{id}`: Update a specific question.

### Answers
- **GET** `/api/answers/question/{questionId}`: Fetch answers by question ID.
- **POST** `/api/answers`: Create new answers.

### Themes
- **GET** `/api/theme`: Fetch all themes.
- **GET** `/api/theme/by-name?name={themeName}`: Get a theme by name.

---

## Security
- Configured with **JWT-based authentication**.
- Implements role-based access control.
- CORS policy allows requests from `http://localhost:3000`.

---

## Contributing
To contribute to this project:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch-name`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push the branch (`git push origin feature-branch-name`).
5. Open a pull request.

---

## License
This project is licensed under the [MIT License](LICENSE).
