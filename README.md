<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/othneildrew/Best-README-Template">
    <img src="https://upload.wikimedia.org/wikipedia/en/thumb/a/a9/TikTok_logo.svg/1000px-TikTok_logo.svg.png" alt="Logo">
  </a>

<h3 align="center">TikTok Springboot Backend Demo Application</h3>

  <p align="center">
    This is my TikTok backend demo application built with Spring Boot, Spring Security, MySQL, Postman, AWS EC2, and AWS RDS
    <br />

</div>

<!-- ABOUT THE PROJECT -->
## About The Project

[![Product Name Screen Shot][product-screenshot]](https://example.com)

TikTok is a popular social media platform where users can create, share, and discover short-form videos, typically ranging from a few seconds to one minute in length. It allows users to express themselves creatively through lip-syncing, dancing, comedy sketches, tutorials, and more.

After three years of dedicated Java learning, I've embarked on a journey to harness my skills by delving into backend development. Here is what I gained when creating this graph 
* Rest API web application to let users perform create/ read/ update/ delete via Spring Web
* Enable authorization access only with Spring Security
* Design and connect Spring app to local/ cloud database ( I'm using MySQL)
* Deploy the app on AWC EC2, host my database on RDS and set the security groups to allow spring app can connect


<!-- GETTING STARTED -->
## Getting Started

This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Prerequisites
* Clone the project
  ```sh
  git clone 
  ```

* Connect to database
* Clone the project & set up the connection through local database
  ```sh
  server.port=8080
  spring.datasource.url=jdbc:mysql://localhost:3306/tiktok
  spring.datasource.username=[YOUR_USERNAME]
  spring.datasource.password=[YOUR_PASSWORD]
  spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQLDialect
  spring.jpa.hibernate.ddl-auto=update
  spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
  ```
  
* In utils repository package, change hash the login password user used to sign in by replace
  YOUR_PASSWORD with the preferred password and run the main method, your hashcode password
  will be print under terminal. <br>

In users table, set the password of that you hash from the above step.         
[![Table users][table-users-screenshot]]

Create the roles table with these default value           
[![Table roles][table-roles-screenshot]]

Map the user and their role inside users_role          
[![Table roles][table-users-roles-screenshot]]


### Testing

* From Postman 
  ```
  set the url to http://localhost:8080/newsfeed
  In Authorization choose "Basic Authentication"
  set username match the one you put in the users table
  set password be the password you chosen without being hash
  ```

### For HR
* You can access to my app hosted on cloud by using Postman, or any
testing web API by access to this endpoint
  Used the username/ password I gave on my CV for testing
  ```
  http://3.89.157.175:8080/newsfeed
  ```


[product-screenshot]: https://dlmocha.com
[table-users-screenshot]: https://thanhdatnasdaq.github.io/images/tiktok-springboot/users.png?raw=true
[table-roles-screenshot]: https://thanhdatnasdaq.github.io/images/tiktok-springboot/roles.png?raw=true
[table-users-roles-screenshot]: https://thanhdatnasdaq.github.io/images/tiktok-springboot/users-roles.png?raw=true