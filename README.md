# devops-ec2-docker



# 🚀 DevOps Assignment – Dockerize a Web App

## 📌 Objective

This project demonstrates the Dockerization of a simple Node.js web application as part of a DevOps assessment.

---

## ✅ Completed Tasks

1. Setup GitHub Repository
2. Dockerize the application and run it locally in a container

---

## 📂 Project Structure
devops-ec2-docker/
├── app.js
├── package.json
├── Dockerfile
└── README.md



---

## 🔧 Technologies Used

- Node.js
- Docker
- Git & GitHub
- PowerShell (Windows Terminal)

---

## 🛠 How to Run Locally Using Docker

### 📦 Step 1: Clone the Repository

```bash
git clone https://github.com/Yashw20/devops-ec2-docker.git
cd devops-ec2-docker



APP.JS
javascript
Copy
Edit
const express = require('express');
const app = express();
const PORT = 3000;

app.get('/', (req, res) => res.send('Hello from Docker + EC2!'));

app.listen(PORT, () => console.log(`App running on port ${PORT}`));


PACKAGE.JS
json
Copy
Edit
{
  "name": "docker-ec2-app",
  "version": "1.0.0",
  "main": "app.js",
  "scripts": {
    "start": "node app.js"
  },
  "dependencies": {
    "express": "^4.18.2"
  }
}


DOCKERFILE
dockerfile
Copy
Edit
FROM node:18
WORKDIR /app
COPY . .
RUN npm install
EXPOSE 3000
CMD ["npm", "start"]



**🔨 Build the Docker image**
bash
Copy
Edit
docker build -t myapp .


🚀 Run the container
bash
Copy
Edit
docker run -p 3000:3000 myapp


🌐 Open your browser
Go to:
http://localhost:3000
You should see:

Copy
Edit
Hello from Docker + EC2!
