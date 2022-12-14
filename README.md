# :movie_camera: Cinema Application
This application implements functionality for a cinema with several halls. It is possible to register visitors who will be able to purchase tickets for a certain time in the selected hall The project is built using Java and popular frameworks such as Spring and Hibernate. Includes authentication/authorization, REST,
## :card_file_box: Structure of this project consists of 3 levels:
- Data access layer (DAO). This layer is responsible for accessing the database. It is implemented with a Hibernate API.
- Application layer (service). This layer implements the main logic of the application.
- Presentation layer (controllers). This layer is responsible for communication with a user. It is implemented with Spring API.
## :hammer_and_wrench: Technologies stack:
- Java 11
- Hibernate
- Spring Framework
- REST
- MySQL
- Apache Tomcat 9.0.50 (to run app locally)
## :mag_right: Entity relationships can be seen in the diagram
![alt text](/src/main/resources/images/Cinema_Entities.png)
## :clipboard:  Features :
### For Admin role
- Registration and authorization (POST: /register, GET: /login)
- Viewing:
  - cinema halls (GET: /cinema-halls)
  - movies (GET: /movies)
  - available movie sessions (GET: /movie-sessions/available)
  - some specific movie session (GET: /movie-sessions/{id})
- Add new:
  - cinema halls (POST: /cinema-halls)
  - movies (POST: /movies)
  - movie sessions (POST: /movie-sessions)
- Update and delete movie session (PUT: /movie-sessions/{id}, DELETE: /movie-sessions/{id})
- Get some user by email (GET: /users/by-email)
- Logout (GET: /logout)
### For User role
- Registration and authorization (POST: /register, GET: /login)
- Viewing:
  - cinema halls (GET: /cinema-halls)
  - movies (GET: /movies)
  - available movie sessions (GET: /movie-sessions/available)
  - some specific movie session (GET: /movie-sessions/{id})
- Get orders and shopping carts (GET: /orders, GET: /shopping-carts/by-user)
- Complete orders (POST: /orders/complete)
- Add tickets to shopping cart for some movie session (PUT: /shopping-carts/movie-sessions)
- Logout (GET: /logout)
### For All
- Registration and authorization (POST: /register, GET: /login)

## :briefcase: To start the project you need:
1. Download and install Java 11 SDK.
2. Download and install Tomcat (version 9.0.63).
3. Download and install MySQL.
4. Create schema (cinema).
5. Clone project to your IDE.
6. Add your username, password and DB url in db.properties file.
   ```java
   #MySQL properties
   db.driver=YOUR_DRIVER
   db.url=YOUR_DATABASE_URL
   db.user=YOUR_USERNAME
   db.password=YOUR_PASSWORD
   ```
7. Use Postman to send requests. POST request example:
   ```
   http://localhost:8080/movies - URL
   {"title":"testMovie", "description":"test description"} - body;
   ```
## :pushpin: For testing, use ready-made profiles:
1. Admin
- Login: [admin@i.ua]()
- Password: admin123
2. User
- Login: [user@i.ua]()
- Password: user123
