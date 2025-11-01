**Folder & Component Structure**

task-tracker/
│
├── src/
│   ├── main/
│   │   ├── java/com/example/tasktracker/
│   │   │   ├── TaskTrackerApplication.java     <-- Main entry point
│   │   │   ├── controller/
│   │   │   │   └── TaskController.java         <-- Handles API routes
│   │   │   ├── model/
│   │   │   │   └── Task.java                   <-- Database entity (table)
│   │   │   └── repository/
│   │   │       └── TaskRepository.java         <-- DB interface
│   │   └── resources/
│   │       ├── application.properties          <-- Spring config
│   │       └── .env                            <-- Local environment vars
│   └── test/                                   <-- Tests (optional)
│
├── pom.xml                                     <-- Maven dependencies
└── .gitignore

**What Happens When You Run: mvn spring-boot:run**

Spring Boot does this automatically:

Starts an embedded web server (Tomcat)

Loads configurations from application.properties

Connects to PostgreSQL using your credentials from .env

Scans your project for:

Models (@Entity) → Creates database tables

Repositories (@Repository) → Handles database CRUD

Controllers (@RestController) → Exposes API routes


**Important Annotations**