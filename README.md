
# 🚀 Webapp Docker Deployment

[![Docker](https://img.shields.io/badge/Docker-Ready-blue?logo=docker&style=for-the-badge)](https://www.docker.com/)

A simple guide to run your **Dockerized web application** locally, with tips to handle port conflicts and container management like a pro! 💻🐳

---

## 🎯 Quick Start

Run the webapp container exposing port **5000**:

```bash
docker run -d -p 5000:5000 webapp
````

Open your browser and visit:
➡️ [http://localhost:5000](http://localhost:5000)

---

## ⚠️ Port 5000 Already in Use? No Worries!

If you get this error:

```
Bind for 0.0.0.0:5000 failed: port is already allocated
```

Follow these easy steps to free up port **5000**:

### 1️⃣ Find the Process ID (PID) Using Port 5000

```powershell
netstat -ano | findstr :5000
```

Note the PID number from the output.

### 2️⃣ Identify the Process Name

```powershell
tasklist /FI "PID eq <PID>"
```

Replace `<PID>` with the actual number.

### 3️⃣ Kill the Process (If Safe)

```powershell
taskkill /PID <PID> /F
```

---

## 🐳 Managing Docker Containers Using Port 5000

### List running containers:

```bash
docker ps
```

### Stop the container occupying port 5000:

```bash
docker stop <container_id>
```

### Remove the container (optional):

```bash
docker rm <container_id>
```

---

## 🔄 Run on a Different Port

If you prefer not to stop existing processes, run your app on another port, e.g., 5001:

```bash
docker run -d -p 5001:5000 webapp
```

Access it via:
➡️ [http://localhost:5001](http://localhost:5001)

---

## 🛠 Troubleshooting Tips

* Ensure Docker daemon is running:

  ```bash
  docker info
  ```
* Check running containers:

  ```bash
  docker ps
  ```
* View logs for your container:

  ```bash
  docker logs <container_id>
  ```

---

## 🙋‍♂️ About Me

**Rio** — CEO of Techeron Global Inc
Building scalable tech solutions one container at a time! 🚀

---

*Feel free to open issues or submit PRs for improvements!*

```

---

Would you like me to add your company logo or links to your website/social media?
```
