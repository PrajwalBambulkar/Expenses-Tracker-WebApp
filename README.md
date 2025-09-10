![Language](https://img.shields.io/badge/language-Java%20-blue.svg)
![Technologies](https://img.shields.io/badge/technologies-Spring_boot%20-green.svg)
![Technologies](https://img.shields.io/badge/technologies-Spring_MVC%20-green.svg)
![Technologies](https://img.shields.io/badge/technologies-Spring_Security%20-green.svg)
![Technologies](https://img.shields.io/badge/technologies-Spring_Data_jpa%20-green.svg)
![Technologies](https://img.shields.io/badge/technologies-Thymeleaf_&_Bootstrap%20-purple.svg)

# Expenses-Tracker-WebApp
## Overview
The Expenses Tracker App is a robust financial management solution developed using cutting-edge technologies such as Spring Boot, Spring Security, and MySQL. With user authentication and authorization features, users can securely sign up, sign in, and perform CRUD operations on their expenses. The app's intuitive interface, powered by Thymeleaf and Bootstrap, ensures a seamless user experience. The filtering functionality allows users to efficiently organize and analyze their financial data. Explore the power of streamlined expense tracking and financial control with this feature-rich application.<br> (Screenshots below for more illustration)

## Technologies Used
- Java
- Spring boot
- Spring MVC
- Spring Security
- Spring Data (JPA)
- MySQL
- Thymeleaf
- Bootstrap

## Features
- **User Authentication and Authorization:** Securely sign up, sign in, and access the app with built-in authentication and authorization.
- **CRUD Operations:** Perform essential financial tracking actions such as adding, reading, updating, and deleting expenses.
- **Filtering:** Utilize the filtering feature to efficiently sort and view expenses based on various criteria.

## Getting Started
1. **Clone the Repository:**
- `git clone https://github.com/your-username/expenses-tracker.git`

2. **Run with Docker (recommended, no code changes required)**
- `docker build -t expenseapp .`

3. **Create a Docker network so containers can resolve each other by name:**
- `docker network create exp-net || true`

4. **Start MySQL container on that network (DB name & password must match application.properties):**
- ```bash
  docker run -d --name mysql \
--network exp-net \
-e MYSQL_ROOT_PASSWORD='Test@123' \
-e MYSQL_DATABASE='expenses_tracker' \
-p 3306:3306 \
mysql:8```

5. **If you see authentication errors like Public Key Retrieval is not allowed, run the app with the JDBC option allowPublicKeyRetrieval=true by overriding the Spring property at runtime:**
   
- `docker run -d --name expenseapp-container \
--network exp-net \
-p 8080:8080 \
-e SPRING_DATASOURCE_URL="jdbc:mysql://mysql:3306/expenses_tracker?useSSL=false&allowPublicKeyRetrieval=true" \
-e SPRING_DATASOURCE_USERNAME=root \
-e SPRING_DATASOURCE_PASSWORD='Test@123' \
expenseapp`

6. **Access the UI from the host or a remote:**
- http://localhost:8080/ # on the server itself
- http://ec2ip:8080/ # from another machine (open port 8080 in firewall/SG)

## ScreenShots
![Example Image](screenshots/1.png) <br>
![Example Image](screenshots/2-2.png) <br>
![Example Image](screenshots/3-3.png) <br>
![Example Image](screenshots/4-4.png) <br>
![Example Image](screenshots/5-5.png) <br>
![Example Image](screenshots/6-6.png) <br>
![Example Image](screenshots/7.png) <br>
![Example Image](screenshots/8.png) <br>

## Contributions
Contributions are welcome! If you find a bug or have suggestions for improvement, feel free to open an issue or create a pull request.

## License
This project is licensed under the MIT License.
