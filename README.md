# Traini8 Startup API Project

## Overview
This project is a Spring Boot application for managing training centers. It provides RESTful APIs to create and retrieve training centers.

## Project Structure
```
traini8
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com
│   │   │       └── traini8
│   │   │           ├── Traini8Application.java
│   │   │           ├── controller
│   │   │           │   └── TrainingCenterController.java
│   │   │           ├── model
│   │   │           │   └── TrainingCenter.java
│   │   │           ├── repository
│   │   │           │   └── TrainingCenterRepository.java
│   │   │           └── service
│   │   │               └── TrainingCenterService.java
│   │   └── resources
│   │       ├── application.properties
│   │       └── data.sql
│   └── test
│       └── java
│           └── com
│               └── traini8
│                   └── Traini8ApplicationTests.java
├── pom.xml
└── README.md
```

## Setup Instructions

### Prerequisites
- Java 11 or higher
- Maven
- An IDE (e.g., IntelliJ IDEA, Eclipse, or VS Code)

### Running the Application
1. Clone the repository:
   ```
   git clone <repository-url>
   cd traini8
   ```

2. Navigate to the project directory and build the project:
   ```
   mvn clean install
   ```

3. Run the application:
   ```
   mvn spring-boot:run
   ```

4. The application will start on `http://localhost:8080`.

### API Endpoints

#### Create Training Center
- **Endpoint**: `POST /api/training-centers`
- **Request Body**: 
  ```json
  {
    "centerName": "Example Center",
    "centerCode": "EXC123",
    "address": {
      "detailedAddress": "123 Example St",
      "city": "Example City",
      "state": "Example State",
      "pincode": "123456"
    },
    "studentCapacity": 100,
    "coursesOffered": ["Course 1", "Course 2"],
    "createdOn": 1633036800000,
    "contactEmail": "contact@example.com",
    "contactPhone": "1234567890"
  }
  ```
- **Response**: Returns the created TrainingCenter object in JSON format.

#### Retrieve All Training Centers
- **Endpoint**: `GET /api/training-centers`
- **Response**: Returns a list of all TrainingCenter objects in JSON format.

### Testing the APIs
You can use tools like Postman or curl to test the APIs. Make sure the application is running before making requests.

### Database Configuration
Configure your database settings in `src/main/resources/application.properties`.

### License
This project is licensed under the MIT License.