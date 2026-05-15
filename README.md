# Developers-Hub-intership-1

## Overview

This project was completed as part of a Cybersecurity Internship focused on web application security assessment and vulnerability mitigation.

The project demonstrates:
- Vulnerability assessment using OWASP ZAP
- Identification of security weaknesses
- Security hardening techniques
- Authentication improvements
- Logging and monitoring
- Secure coding practices

---

## Technologies Used

- Node.js
- Express.js
- MongoDB
- OWASP ZAP
- Helmet.js
- bcrypt
- JWT Authentication
- Winston Logger
- Validator.js

---

## Features

- User Registration & Login
- JWT Authentication
- Password Hashing
- Input Validation
- Secure HTTP Headers
- Logging and Monitoring
- Vulnerability Assessment
- Security Improvements

---

## Installation

### Clone Repository

```bash
git clone https://github.com/AmnaZainabMalik/Developers-Hub-intership-1
```

### Move to Project Folder

```bash
cd cybersecurity-internship-project
```

### Install Dependencies

```bash
npm install
```

### Start Application

```bash
npm start
```

---

## Application URL

```txt
http://localhost:5000
```

---

## Security Assessment

The application was tested using OWASP ZAP to identify vulnerabilities and security weaknesses.

### Vulnerabilities Identified
- Missing Content Security Policy (CSP)
- Missing Security Headers
- Weak Cookie Configuration
- Information Disclosure
- Missing Input Validation

---

## Security Improvements Implemented

### Helmet.js Security Headers

```javascript
const helmet = require('helmet');
app.use(helmet());
```

### Password Hashing

```javascript
const bcrypt = require('bcrypt');
const hashedPassword = await bcrypt.hash(password, 10);
```

### JWT Authentication

```javascript
const jwt = require('jsonwebtoken');

const token = jwt.sign(
  { id: user._id },
  'secret-key',
  { expiresIn: '1h' }
);
```

### Input Validation

```javascript
const validator = require('validator');

if (!validator.isEmail(email)) {
   return res.status(400).send('Invalid Email');
}
```

### Secure Cookies

```javascript
res.cookie('token', token, {
   httpOnly: true,
   secure: true,
   sameSite: 'Strict'
});
```

### Winston Logger

```javascript
const winston = require('winston');

const logger = winston.createLogger({
  transports: [
    new winston.transports.Console(),
    new winston.transports.File({
      filename: 'security.log'
    })
  ]
});
```

---

## Project Structure

```text
cybersecurity-internship-project/
│
├── reports/
├── screenshots/
├── src/
├── security.log
├── package.json
└── README.md
```

---

## Results

After implementing security measures:
- Security headers were added
- Authentication security improved
- Input validation implemented
- Vulnerabilities reduced
- Logging enabled
- Information disclosure minimized

---

## Tools Used

- OWASP ZAP
- VS Code
- GitHub
- Node.js
- MongoDB

---

## Conclusion

This project successfully demonstrated vulnerability assessment and implementation of security best practices in a Node.js web application.

Security improvements such as Helmet.js, JWT authentication, bcrypt hashing, secure cookies, and logging significantly strengthened the application security posture.

---

## Author

Amna Zainab Malik
DHC-1687

Cybersecurity Internship Project  
2026 
