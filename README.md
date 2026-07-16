# 🐳 Docker + AWS EC2 Deployment Project

## 📌 Project Overview

This project demonstrates how to containerize and deploy a static website using **Docker** on an **AWS EC2** instance. It also covers version control using **Git** and **GitHub**, along with serving the application through **Nginx**.

### Objectives

- Containerize a static website using Docker
- Deploy the application on an AWS EC2 instance
- Manage source code with Git and GitHub
- Serve the application using Nginx
- Access the application through a web browser using port mapping

---

# 🛠️ Technologies Used

- Docker
- Amazon Web Services (AWS EC2)
- Git
- GitHub
- Nginx
- Ubuntu Linux

---

# 📁 Project Structure

```
devops-demo/
│── Dockerfile
│── index.html
└── README.md
```

---

# ⚙️ Docker Commands

## 1. Build the Docker Image

```bash
docker build -t devops-app .
```

**Purpose:**
Creates a Docker image from the Dockerfile in the current directory.

---

## 2. Run the Docker Container

```bash
docker run -d -p 8080:80 devops-app
```

**Purpose:**

- Starts the container in detached mode.
- Maps port **8080** on the host machine to port **80** inside the container.

---

## 3. List Running Containers

```bash
docker ps
```

**Purpose:**
Displays all currently running Docker containers.

---

## 4. Stop a Running Container

```bash
docker stop <container_id>
```

**Purpose:**
Stops the specified Docker container.

---

# ☁️ AWS EC2 Deployment

## Step 1: Launch an EC2 Instance

- Launch an Ubuntu Server instance
- Instance Type: **t2.micro (Free Tier Eligible)**
- Configure the Security Group:
  - Allow SSH (Port 22)
  - Allow HTTP (Port 80)

---

## Step 2: Connect to the Instance

Connect using **EC2 Instance Connect** or SSH.

---

## Step 3: Install Docker

```bash
sudo apt update
sudo apt install docker.io -y
```

---

## Step 4: Start and Enable Docker

```bash
sudo systemctl start docker
sudo systemctl enable docker
```

---

## Step 5: Install Git

```bash
sudo apt install git -y
```

---

## Step 6: Clone the Repository

```bash
git clone https://github.com/username/docker-website.git

cd docker-website
```

> Replace **username** with your GitHub username.

---

## Step 7: Build and Run the Application

Build the Docker image:

```bash
docker build -t devops-app .
```

Run the container:

```bash
docker run -d -p 80:80 devops-app
```

---

## Step 8: Access the Website

Open your browser and visit:

```
http://<EC2-PUBLIC-IP>
```

Replace `<EC2-PUBLIC-IP>` with the public IP address of your EC2 instance.

---

# 🔄 Git & GitHub Workflow

## Initialize Git Repository

```bash
git init
```

---

## Add Project Files

```bash
git add .
```

---

## Commit Changes

```bash
git commit -m "Initial Docker AWS project"
```

---

## Add Remote Repository

```bash
git remote add origin https://github.com/username/repository-name.git
```

---

## Push to GitHub

```bash
git branch -M main

git push -u origin main
```

---

# ❌ Common Errors and Solutions

## 1. Docker Is Not Running

**Error**

```text
failed to connect to Docker daemon
```

**Solution**

- Start Docker Desktop
- Restart Docker service if necessary

---

## 2. Dockerfile Not Found

**Error**

```text
no such file or directory
```

**Solution**

Ensure you are inside the project directory before running Docker commands.

---

## 3. Incorrect File Extension

**Error**

```text
index.html.txt
```

**Solution**

Enable file extensions in your operating system and rename the file to:

```text
index.html
```

---

## 4. Git Push Rejected

**Error**

```text
failed to push some refs
```

**Solution**

```bash
git pull origin main --allow-unrelated-histories
```

Then push again.

---

## 5. Remote Origin Already Exists

**Error**

```text
remote origin already exists
```

**Solution**

```bash
git remote remove origin

git remote add origin https://github.com/username/repository-name.git
```

---

## 6. Website Not Accessible on AWS

**Problem**

The website does not load in the browser.

**Solution**

Verify that:

- Port **80** is allowed in the EC2 Security Group.
- Docker container is running.
- The application is listening on port **80**.

---

# 🔐 GitHub Authentication

GitHub no longer supports password authentication for Git operations.

Use the following credentials when pushing code:

**Username**

Your GitHub username

**Password**

Your GitHub Personal Access Token (PAT)

Generate a token from:

```
GitHub
→ Settings
→ Developer Settings
→ Personal Access Tokens
```

---

# 🎤 Interview Questions

## Docker

- What is Docker?
- What is the difference between a Docker image and a Docker container?
- What is a Dockerfile?
- Why is Docker used?
- What is port mapping?

---

## AWS

- What is Amazon EC2?
- What is a Security Group?
- Why do we deploy applications on cloud platforms?

---

## Git & GitHub

- What is Git?
- What is the difference between `git pull` and `git push`?
- What is `origin` in Git?
- What is a Git commit?

---

# 📚 Key Learning Outcomes

By completing this project, I learned how to:

- Build Docker images from a Dockerfile.
- Run and manage Docker containers.
- Deploy applications on AWS EC2.
- Configure EC2 Security Groups.
- Manage project source code with Git and GitHub.
- Troubleshoot common Docker, Git, and AWS deployment issues.
- Deploy a containerized web application in a cloud environment.

---


<img width="1908" height="641" alt="Screenshot 2026-04-24 010940" src="https://github.com/user-attachments/assets/29a3c42e-96e9-4b0a-a686-4227e5723411" />
<img width="1911" height="997" alt="Screenshot 2026-04-24 011023" src="https://github.com/user-attachments/assets/667b87f1-c2fc-4059-bcde-8e6fdebcf6c7" />

<img width="1919" height="996" alt="Screenshot 2026-04-24 011058" src="https://github.com/user-attachments/assets/ff99e692-0cbc-4f1e-95a7-91869a957e1f" />

