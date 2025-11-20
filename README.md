# 🚀 TeraSkill Academy – Static Website (Docker + NGINX)

A professional HTML/CSS website for **TeraSkill Academy**, containerized using **Docker** and hosted on **NGINX**.  
This repository is fully ready to build, publish, and deploy on any server or cloud platform.

---

## 📂 Project Structure


---

## 🛠️ Technologies Used

- **HTML5 + CSS3**
- **NGINX (alpine build)**
- **Docker**
- **Docker Hub**
- **Static website hosting**

---

## 📸 Live Website Preview

<img width="940" height="381" alt="image" src="https://github.com/user-attachments/assets/abd3601a-b1eb-4a2d-85fb-1846905f04e6" />


---

## 🐳 Build & Run Locally Using Docker

### **1️⃣ Build Docker Image**

docker build -t teraskill:latest .


### **2️⃣ Run the Container on Port 80**

docker run -d -p 80:80 --name teraskill-site teraskill:latest


Open in browser:

👉 http://localhost  
or  
👉 http://serverpublicIP

---

## 🌐 Push Image to Docker Hub

The public Docker Hub repository is:

dokcer.io/ponnam/teraskillwebsite   >> Replace with your Repository Name


### **1️⃣ Tag the image**

docker tag teraskill:latest ponnam/teraskillwebiste:v1


### **2️⃣ Login to Docker Hub**

docker login


### **3️⃣ Push the image**

docker push ponnam/teraskillwebsite:v1


---

## 🐳 Pull & Run From Docker Hub (Anywhere)

docker pull ponnam/teraskillwebsite:v1


Run the container:

docker run -d -p 80:80 --name teraskill-site ponnam/teraskillwebsite:v1


---

## 📄 Dockerfile

```Dockerfile
FROM nginx:alpine

RUN rm -rf /usr/share/nginx/html/*

COPY website/ /usr/share/nginx/html/

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]




