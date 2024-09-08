
# Banking Application

A simple banking application built using Java, Spring Boot, Hibernate, and PostgreSQL. This application provides banking functionalities such as creating accounts, fetching account details, making deposits/withdrawals, and deleting accounts. The APIs have been tested using Postman.



## Table of Contents

1.Features

2.Prerequisites

3.Installation

4.API Endpoints

5.Technologies Used

6.Testing

7.Contributing

8.License



## Features

- Create a new Bank Account
- Fetch details of a specific account.
- Deposit money into an account.
- Withdraw money from an account.
- Get all the bank accounts.
- Delete an existing account.


## Prerequisites

Before running this application, ensure you have the following installed:

- Java 11 or higher.
- Eclipse
- PostgreSQL
- Postman

## Installation

1. Clone the repository.

```bash
  git clone https://github.com/AnkanSanyal/Banking-Application.git
  cd Banking-Application
```

2. Set up PostgreSQL Database:

- Create a PostgreSQL database (e.g., banking_db).
- Update the database configuration in src/main/resources/application.properties with your PostgreSQL username and password:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/banking_db
spring.datasource.username=your_username
spring.datasource.password=your_password
```  
3. Build and Run the Application:

- Build the project using Maven
```bash
  mvn clean install
```
- Run the Spring Boot application
```bash
  mvn spring-boot:run
```

The application will start on http://localhost:8090.
## API Endpoints

Here is a summary of the available API endpoints:

#### Create a new bank account

```http
  POST /api/accounts
```



#### Fetch all the bank accounts

```http
  GET /api/accounts
```


#### Fetch account details by account ID.

```http
  GET /api/accounts/{id}
```

#### Deposit money into an account.

```http
  PUT  /api/accounts/{Id}/deposit
```

#### Withdraw money from an account.

```http
  PUT  /api/accounts/{Id}/withdraw
```
#### Delete a bank account.

```http
  DELETE  /api/accounts/{Id}
```
## Tech Stack

**Backend:** Java, Spring Boot, Spring Data JPA (Hibernate)

**Database:** PostgreSQL

**Testing:** Postman (for API testing)

## Testing

To test the application locally, you can use Postman or any API client to send requests to the endpoints. Ensure the Spring Boot application is running on http://localhost:8090.
## Contributing

Contributions are welcome! If you'd like to contribute to this project, please follow these steps:

1.Fork the repository.

2.Create a new branch (git checkout -b feature-branch).

3.Make your changes.

4.Commit your changes (git commit -m 'Add some feature').

5.Push to the branch (git push origin feature-branch).

6.Open a pull request.


## License

This project is licensed under the MIT License - see the [license](https://choosealicense.com/licenses/mit/) file for details.

