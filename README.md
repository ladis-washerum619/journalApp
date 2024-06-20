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

### Usage
The application runs on [http://localhost:8080](http://localhost:8080). You can use tools like [Postman](https://www.postman.com/) to test the endpoints.

#### Health-Check
To ensure the application is running, you can perform a health check:
- URL: http://localhost:8080/health-check
- Method: GET
- Response: Ok

#### API Endpoints

##### Create a Journal Entry
- **URL:** [http://localhost:8080/journal](http://localhost:8080/journal)
- **Method:** POST
- **Request Body:**
```json
{
  "id": 1,
  "title": "My First Entry",
  "content": "This is the content of my first journal entry."
}
```
- **Response:**
```json
{
  "id": 1,
  "title": "My First Entry",
  "content": "This is the content of my first journal entry."
}
```

##### Get All Journal Entries
- **URL:** [http://localhost:8080/journal](http://localhost:8080/journal)
- **Method:** GET
- **Response:**
```json
[
  {
    "id": 1,
    "title": "My First Entry",
    "content": "This is the content of my first journal entry."
  },
  {
    "id": 2,
    "title": "My Second Entry",
    "content": "This is the content of my second journal entry."
  }
]
```

##### Get a Journal Entry by ID
- **URL:** [http://localhost:8080/journal/id/{id}](http://localhost:8080/journal/id/{id})
- **Method:** GET
- **Response:**
```json
{
  "id": 1,
  "title": "My First Entry",
  "content": "This is the content of my first journal entry."
}
```

##### Update a Journal Entry
- **URL:** [http://localhost:8080/journal/id/{id}](http://localhost:8080/journal/id/{id})
- **Method:** PUT
- **Request Body:**
```json
{
  "title": "Updated Entry Title",
  "content": "This is the updated content of the journal entry."
}
```
- **Response:**
```json
{
  "id": 1,
  "title": "Updated Entry Title",
  "content": "This is the updated content of the journal entry."
}
```

##### Delete a Journal Entry
- **URL:** [http://localhost:8080/journal/id/{id}](http://localhost:8080/journal/id/{id})
- **Method:** DELETE
- **Response:**
```json
{
  "id": 2,
  "title": "My Second Entry",
  "content": "This is the content of my second journal entry."
}
```

### Contributing
Contributions are welcome! Please create a pull request or submit an issue for any improvements or bug fixes.

### Contact
For any questions or suggestions, feel free to contact:

- Ayush Mishra - ayushmishraofficial.619@gmail.com
- Project Link: [https://github.com/ladis-washerum619/journalApp](https://github.com/ladis-washerum619/journalApp)