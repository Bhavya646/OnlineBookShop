# <a href="https://youtu.be/mLFPodZO8Iw" target="_blank">Online Book Store</a>

- A Java Web Development Project
- **YouTube Video – Local Setup Guide:** https://youtu.be/mLFPodZO8Iw

---

## About

Online Book Store is a Java-based web application that allows users to register, log in, browse available books, select quantities, and purchase books. Users can also receive payment receipts after completing a purchase.

The application also provides an admin panel for managing books, including adding new books, removing books, updating book quantities, changing prices, and maintaining sales history.

![Online Book Store](https://user-images.githubusercontent.com/34605595/137615096-8447d32d-bddc-4f13-a8ed-3c0f4dd5e04e.png)

### Project Objectives

- Sell books online.
- Manage available books and their quantities.
- Maintain book sales history.
- Provide a user-friendly interface.
- Implement Java Servlets and JDBC.
- Connect the application with a MySQL database.

### Admin Features

- Add new books.
- View available books.
- Remove books.
- Increase or decrease book quantity.
- Update book prices.
- Maintain selling history.

### User Features

- Create a new account.
- Login to the application.
- View available books.
- Select books to purchase.
- Select book quantity.
- Purchase books.
- Get payment receipts.

---

## Technologies Used

### Frontend

- HTML
- CSS
- JavaScript
- Bootstrap

### Backend

- Java (JDK 8+)
- JDBC
- Java Servlets

### Database

- MySQL

---

## Software and Tools Required

- Git
- Java JDK 8+
- Eclipse IDE for Enterprise Java
- Apache Maven
- Apache Tomcat 8.0+
- MySQL Server
- MySQL Workbench (Optional)

---

## Database Setup

### Step 1

Open **MySQL Command Prompt** or **MySQL Workbench**.

### Step 2

Login to MySQL:

```bash
mysql -u <username> -p
Enter your MySQL password when prompted.

### Step 3

Run the following SQL commands:

```sql
CREATE DATABASE IF NOT EXISTS onlinebookstore;

USE onlinebookstore;

CREATE TABLE IF NOT EXISTS books(
    barcode VARCHAR(100) PRIMARY KEY,
    name VARCHAR(100),
    author VARCHAR(100),
    price INT,
    quantity INT
);

CREATE TABLE IF NOT EXISTS users(
    username VARCHAR(100) PRIMARY KEY,
    password VARCHAR(100),
    firstname VARCHAR(100),
    lastname VARCHAR(100),
    address TEXT,
    phone VARCHAR(100),
    mailid VARCHAR(100),
    usertype INT
);

INSERT INTO books VALUES
('9780134190563','The Go Programming Language','Alan A. A. Donovan and Brian W. Kernighan',400,8);

INSERT INTO books VALUES
('9780133053036','C++ Primer','Stanley Lippman and Josée Lajoie and Barbara Moo',976,13);

INSERT INTO books VALUES
('9781718500457','The Rust Programming Language','Steve Klabnik and Carol Nichols',560,12);

INSERT INTO books VALUES
('9781491910740','Head First Java','Kathy Sierra and Bert Bates and Trisha Gee',754,23);

INSERT INTO books VALUES
('9781492056300','Fluent Python','Luciano Ramalho',1014,5);

INSERT INTO books VALUES
('9781720043997','The Road to Learn React','Robin Wieruch',239,18);

INSERT INTO books VALUES
('9780132350884','Clean Code: A Handbook of Agile Software Craftsmanship','Robert C Martin',288,3);

INSERT INTO books VALUES
('9780132181273','Domain-Driven Design','Eric Evans',560,28);

INSERT INTO books VALUES
('9781951204006','A Programmers Guide to Computer Science','William Springer',188,4);

INSERT INTO books VALUES
('9780316204552','The Soul of a New Machine','Tracy Kidder',293,30);

INSERT INTO books VALUES
('9780132778046','Effective Java','Joshua Bloch',368,21);

INSERT INTO books VALUES
('9781484255995','Practical Rust Projects','Shing Lyu',257,15);

INSERT INTO users VALUES
('demo','demo','Demo','User','Demo Home','42502216225','demo@gmail.com',2);

INSERT INTO users VALUES
('Admin','Admin','Mr.','Admin','Haldia WB','9584552224521','admin@gmail.com',1);

INSERT INTO users VALUES
('shashi','shashi','Shashi','Raj','Bihar','1236547089','shashi@gmail.com',2);

COMMIT;
```

---

## Running the Project

### Step 1 – Open the Project

Open the project in **Eclipse Enterprise Edition**.

### Step 2 – Configure Database

Open:

```text
src/main/resources/application.properties
```

Update the database configuration according to your MySQL installation:

```text
db.driver
db.host
db.username
db.password
```

### Step 3 – Build the Project

Right-click the project:

**Run As → Maven Build**

In the **Goals** field, enter:

```text
clean install
```

Then click **Apply → Run**.

### Step 4 – Configure Tomcat

If Tomcat is not already configured:

**Right Click Project → Run As → Run on Server → Apache Tomcat 8.0**

Select your Tomcat installation directory and add the project.

### Step 5 – Configure Port

Open the Tomcat server configuration and set the HTTP port to:

```text
8083
```

### Step 6 – Run the Application

Run the project using Tomcat.

Open:

<a href="http://localhost:8083/onlinebookstore/">http://localhost:8083/onlinebookstore/</a>

---

## Demo Login Credentials

### Admin

```text
Username: Admin
Password: Admin
```

### User

```text
Username: shashi
Password: shashi
```

> These are the default credentials provided by the sample database.

---

## FAQ

### Unable to Connect to the Database?

Check the following:

- MySQL Server is running.
- Database `onlinebookstore` exists.
- MySQL username and password are correct.
- `application.properties` contains the correct database configuration.
- Run Maven `clean install` again after changing the configuration.

---

## Screenshots

![Online Book Store Screenshot](https://user-images.githubusercontent.com/34605595/224769637-37c34d4b-26e7-4d49-b990-4c09b260ec31.png)

![Online Book Store Screenshot](https://user-images.githubusercontent.com/34605595/224769990-f440f74d-41b2-4629-ba1c-a87267f225d9.png)

![Online Book Store Screenshot](https://user-images.githubusercontent.com/34605595/224770145-5902054f-5943-44ac-b02f-92097c8a6972.png)

![Online Book Store Screenshot](https://user-images.githubusercontent.com/34605595/224770257-e18a3810-0457-4b78-bf46-cf82746708ee.png)

![Online Book Store Screenshot](https://user-images.githubusercontent.com/34605595/224770392-5a5478d2-98cc-44ee-8689-132b6b16af80.png)

---

## Learning Outcomes

Through this project, I worked with:

- Java Servlets
- JDBC
- MySQL
- HTML, CSS and JavaScript
- Bootstrap
- Maven
- Apache Tomcat
- Database integration
- Java web application deployment

---

## Future Improvements

- Improve authentication and authorization.
- Add stronger password security.
- Add online payment gateway integration.
- Improve responsive UI.
- Add advanced book search and filtering.
- Improve application security.

---

## Author

**Bhavya Gera**

B.Tech – Computer Science and Engineering

GitHub: https://github.com/Bhavya646

LinkedIn: https://www.linkedin.com/in/bhavyagera646/

---

## Credits

This project is based on an existing sample Online Book Store project. Appropriate credit should be retained for the original project and its assets according to the applicable license.

---

**Thank you for checking out the project!**