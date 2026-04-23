🐳 ☁️ Docker + AWS EC2 Project Notes (Complete DevOps Guide)
📌 1. Project Overview

This project demonstrates how to:

Containerize a static website using Docker
Deploy it on AWS EC2 cloud server
Push code to GitHub for version control
Expose application using Nginx and port mapping
🛠️ 2. Tools Used
Docker
EC2
Amazon Web Services
Git
GitHub
Nginx
📁 3. Project Structure
devops-demo/
│── Dockerfile
│── index.html
│── README.md
⚙️ 4. Docker Commands (What & Why)
🔹 Build Image
docker build -t devops-app .

👉 Creates Docker image from Dockerfile

🔹 Run Container
docker run -d -p 8080:80 devops-app

👉 Runs container and maps port 8080 → 80

🔹 Check Running Containers
docker ps

👉 Shows active containers

🔹 Stop Container
docker stop <container_id>
☁️ 5. AWS EC2 Deployment Steps
🔹 Step 1: Launch EC2
Ubuntu Server
t2.micro (free tier)
Open ports: 22, 80
🔹 Step 2: Connect to EC2

Use EC2 Instance Connect (browser SSH)

🔹 Step 3: Install Docker
sudo apt update
sudo apt install docker.io -y
🔹 Step 4: Start Docker
sudo systemctl start docker
sudo systemctl enable docker
🔹 Step 5: Install Git
sudo apt install git -y
🔹 Step 6: Clone GitHub Repo
git clone https://github.com/username/docker-website.git
cd docker-website
🔹 Step 7: Build & Run Docker
docker build -t devops-app .
docker run -d -p 80:80 devops-app
🌐 Access Website
http://<EC2-Public-IP>
🔗 6. GitHub Steps (Upload Project)
🔹 Initialize Git
git init
🔹 Add files
git add .
🔹 Commit
git commit -m "Docker AWS project"
🔹 Add remote
git remote add origin https://github.com/username/repo.git
🔹 Push code
git branch -M main
git push -u origin main
❌ 7. Errors Faced & Solutions
🔸 Error 1: Docker not running

❌ failed to connect to docker API

✔ Solution:

Start Docker Desktop
Restart system
🔸 Error 2: Dockerfile not found

❌ no such file or directory

✔ Solution:

Run command inside correct folder
🔸 Error 3: Wrong file extension

❌ index.html.txt

✔ Solution:

Enable file extensions
Rename to index.html
🔸 Error 4: Git push rejected

❌ failed to push refs

✔ Solution:

git pull origin main --allow-unrelated-histories
🔸 Error 5: Remote already exists

❌ remote origin already exists

✔ Solution:

git remote remove origin
git remote add origin <url>
🔸 Error 6: Website not opening on AWS

❌ site not accessible

✔ Solution:

Open Security Group
Allow HTTP (port 80)
🔐 8. GitHub Token Issue

When pushing code:

Username → GitHub username
Password → Personal Access Token (PAT)

Token generated from:
👉 GitHub Settings → Developer Settings → Personal Access Token

🎤 9. Interview Questions
🔹 Docker Questions
What is Docker?
What is difference between image and container?
What is Dockerfile?
Why use Docker?
What is port mapping?
🔹 AWS Questions
What is EC2?
What is security group?
Why use cloud deployment?
🔹 Git Questions
What is Git?
Difference between git pull and push?
What is remote origin?
What is commit?


<img width="1908" height="641" alt="Screenshot 2026-04-24 010940" src="https://github.com/user-attachments/assets/29a3c42e-96e9-4b0a-a686-4227e5723411" />
<img width="1911" height="997" alt="Screenshot 2026-04-24 011023" src="https://github.com/user-attachments/assets/667b87f1-c2fc-4059-bcde-8e6fdebcf6c7" />

<img width="1919" height="996" alt="Screenshot 2026-04-24 011058" src="https://github.com/user-attachments/assets/ff99e692-0cbc-4f1e-95a7-91869a957e1f" />

