Simple Spring Boot 3 and Java 17 Banking Transaction Application
This is a simple banking transaction application built using Spring Boot 3 and Java 17. The purpose of this application is to simulate a transfer of money from one user's account to another using Spring Data JDBC.

Prerequisites
To run this application, you'll need the following installed on your machine:

Java 17 or above
Maven 3 or above
Getting Started
Clone the repository

bash
git clone https://github.com/Aminmalek/spring-boot-transaction
Navigate to the project directory

bash
cd /spring-boot-transaction
Build the application

bash
mvn clean install
 ./mvnw spring-boot:run

Usage
The application has two endpoints:

/accounts: This endpoint returns a list of all accounts in the system.

/transfer: This endpoint allows a user to transfer money to another user. It accepts the following parameters:

senderAccountId: The ID of the user making the transfer.
receiverAccountId: The ID of the user receiving the transfer.
amount: The amount to be transferred.
Sample Request:

curl -XPOST -H "content-type:application/json" -d '{"senderAccountId":1,
 "receiverAccountId":2, "amount":100}' http://localhost:8080/transfer
 
Sample Response:

HTTP/1.1 200 OK
Content-Type: application/json
Conclusion
This simple application demonstrates how to use Spring Boot 3 and Spring Data JDBC to implement a basic banking transaction system. It can be extended and customized as per your requirements, and provides a solid foundation for building more complex applications.
