<!DOCTYPE html>
<html>
<head>
<title>Simple Spring Boot 3 and Java 17 Banking Transaction Application</title>
</head>
<body>
<h1>Simple Spring Boot 3 and Java 17 Banking Transaction Application</h1>

<p>This is a simple banking transaction application built using Spring Boot 3 and Java 17. The purpose of this application is to simulate a transfer of money from one user's account to another using Spring Data JDBC.</p>

<h2>Prerequisites</h2>

<p>To run this application, you'll need the following installed on your machine:</p>

<ul>
	<li>Java 17 or above</li>
	<li>Maven 3 or above</li>
</ul>

<h2>Getting Started</h2>

<ol>
	<li>Clone the repository:</li>

	<pre><code>git clone https://github.com/Aminmalek/spring-boot-transaction.git</code></pre>

	<li>Navigate to the project directory:</li>

	<pre><code>cd spring-boot-transaction</code></pre>

	<li>Build the application:</li>

	<pre><code>mvn clean install</code></pre>

	<li>Run the application:</li>

	<pre><code>./mvnw spring-boot:run</code></pre>
</ol>

<h2>Usage</h2>

<p>The application has two endpoints:</p>

<ul>
	<li><code>/accounts</code>: This endpoint returns a list of all accounts in the system.</li>

	<li><code>/transfer</code>: This endpoint allows a user to transfer money to another user. It accepts the following parameters:</li>

	<ul>
		<li><code>senderAccountId</code>: The ID of the user making the transfer.</li>
		<li><code>receiverAccountId</code>: The ID of the user receiving the transfer.</li>
		<li><code>amount</code>: The amount to be transferred.</li>
	</ul>
</ul>

<h3>Sample Request:</h3>

<pre><code>curl -XPOST -H "content-type:application/json" \
-d '{"senderAccountId":1, "receiverAccountId":2, "amount":100}' 

http://localhost:8080/transfer</code></pre>

<h3>Sample Response:</h3>

<pre><code>HTTP/1.1 200 OK
Content-Type: application/json</code></pre>

<h2>Conclusion</h2>

<p>This simple application demonstrates how to use Spring Boot 3 and Spring Data JDBC to implement a basic banking transaction system. It can be extended and customized as per your requirements and provides a solid foundation for building more complex applications.</p>
</body>
</html>
