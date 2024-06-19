# Journal App REST API

### Overview
This project is a simple REST API for managing Journal entries. It allows users to Create, Read, Update, and Delete journal entries. The API is built using Spring Boot. No database is used; the data is stored in memory. This is just a starter project to demonstrate basic CRUD operations.

### Prerequisites
- Java 17 or higher
- Maven 3.9.6 or higher
- Git

### Installation
1. **Clone the Repository**
```sh
git clone https://github.com/ladis-washerum619/journalApp.git
cd journalApp
```
2. **Project Structure**
```css
journalApp
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com
│   │   │       └── lw
│   │   │           └── journalApp
│   │   │               ├── controller
│   │   │               │   ├── HealthCheck.java
│   │   │               │   └── JournalEntryController.java
│   │   │               └── entity
│   │   │                   └── JournalEntry.java
│   │   └── resources
│   │       └── application.properties
└── pom.xml

```
3. **Build the Project**
```
mvn clean install
```
4. **Run the Application**
```
mvn spring-boot:run
```