cat <<EOF > projects/docker-assignment1.md
# 🐳 Assignment 1: Custom Web Showcase Container

## 🎯 Project Purpose
The goal of this assignment was to containerize a static website using Nginx and ensure it is accessible from a Windows browser via WSL2.

---

## 🛠️ Implementation Commands

To build and run this project, I used the following terminal commands:

**1. Build the image:**
\`\`
docker build -t aravind-dev-showcase:latest .
\`\`

**2. Run the container with port mapping:**
\`\`
docker run -d -it --name Web1 -p 8080:80 aravind-dev-showcase:latest
\`\'

---

## 🖥️ Expected Output

### Terminal Output
After running **\"docker ps -a\"**, the container should show as "Up" with the ports mapped:
\`\`\`text
CONTAINER ID   IMAGE                    STATUS          PORTS
37a6ef930da2   aravind-dev-showcase     Up 35 seconds   0.0.0.0:8080->80/tcp
\`\`\`

### Browser Output
When you navigate to \"http://localhost:8080\", you will see the "Meenatchi Sundaram Dev Portfolio" homepage.

**Screenshot of the working application:**
![Meenatchi Portfolio Output](./images/output.png)

---

## 📝 Key Instructions
1. Ensure **Docker Desktop** is running on your Windows machine.
2. If port **8080** is already in use, change the first number in the \`-p\` command to \`9090\`.
3. To view the internal logs of the application, use:
   **"docker logs Web1"**

[← Back to Main Portfolio](../README.md)

