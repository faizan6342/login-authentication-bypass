# Login Authentication Bypass

## Project Overview
This project demonstrates SQL Injection authentication vulnerabilities and secure login implementation using PHP and MySQL.

The project includes:
- Vulnerable authentication workflow
- Secure authentication implementation
- SQL Injection testing concepts
- SQLMap examples
- Burp Suite request analysis
- Secure coding practices

---

## Objectives
- Demonstrate authentication bypass vulnerabilities  
- Understand SQL Injection concepts  
- Compare vulnerable vs secure login systems  
- Learn secure authentication practices  
- Implement prepared statements for security  

---

## Technologies Used
- PHP  
- MySQL  
- HTML  
- CSS  
- XAMPP  
- SQLMap  
- Burp Suite  

---

## Vulnerable Authentication Logic

```php
$query = "SELECT * FROM users WHERE username='$username' AND password='$password'";
```

This implementation directly inserts user input into SQL queries, making the application vulnerable to SQL Injection attacks.

---

## Secure Authentication Logic

```php
$stmt = $conn->prepare("SELECT * FROM users WHERE username=? AND password=?");
```

Prepared statements separate SQL logic from user input and help prevent SQL Injection vulnerabilities.

---

## Features
- Authentication bypass demonstration  
- Vulnerable login workflow  
- Secure login implementation  
- SQL Injection testing examples  
- SQLMap command references  
- Burp Suite interception notes  
- MySQL database setup  
- Secure coding techniques  

---

## How to Run

### 1. Install XAMPP
Download and install XAMPP.

### 2. Move Project Folder
Move the project folder into:

```text
C:\xampp\htdocs\
```

### 3. Start Services
Start:
- Apache
- MySQL

from XAMPP Control Panel.

### 4. Create Database
Open:

```text
http://localhost/phpmyadmin
```

Import:

```text
vulnerable-demo/database.sql
```

### 5. Run Project
Open:

```text
http://localhost/login-authentication-bypass/vulnerable-demo
```

---

## SQLMap Examples

```bash
sqlmap --url http://testphp.vulnweb.com/listproducts.php?cat=1 --dbs
```

```bash
sqlmap --url http://testphp.vulnweb.com/listproducts.php?cat=1 --tables
```

---

## Prevention Techniques
- Prepared Statements  
- Parameterized Queries  
- Input Validation  
- ORM Security  
- Web Application Firewall (WAF)  
- Least Privilege Principle  
- Secure Error Handling  
- Security Auditing  

---

## Key Insights
- Insecure SQL queries can lead to authentication bypass  
- Prepared statements significantly reduce SQL Injection risks  
- Secure coding practices improve authentication security  
- Input validation is critical for web application security  

---

## Educational Purpose
This repository is intended strictly for:
- Cybersecurity education  
- Ethical security testing  
- Secure coding awareness  
- Authentication security demonstrations  

---

## Future Improvements
- Add session handling  
- Implement password hashing  
- Add CSRF protection  
- Add admin dashboard  
- Add logging system  

---

## Author
Faizan Ahmed
