### **1. Docker Basics**
- **Check Docker Version:**
  ```bash
  docker --version
  ```
- **View Docker System Info:**
  ```bash
  docker info
  ```

### **2. Docker Images**
- **List Docker Images:**
  ```bash
  docker images
  ```
- **Search for an Image:**
  ```bash
  docker search nginx
  ```
- **Pull an Image from Docker Hub:**
  ```bash
  docker pull nginx
  ```
- **Build an Image from a Dockerfile:**
  ```bash
  docker build -t mynginx:1.0 .
  ```
- **Tag an Image:**
  ```bash
  docker tag mynginx:1.0 mynginx:latest
  ```
- **Remove an Image:**
  ```bash
  docker rmi mynginx:latest
  ```

### **3. Docker Containers**
- **Run a Container:**
  ```bash
  docker run nginx
  ```
- **Run a Container in Detached Mode (Background):**
  ```bash
  docker run -d nginx
  ```
- **Run a Container with a Custom Name:**
  ```bash
  docker run --name mynginx nginx
  ```
- **Run a Container with Port Mapping:**
  ```bash
  docker run -d -p 8080:80 nginx
  ```
- **List Running Containers:**
  ```bash
  docker ps
  ```
- **List All Containers (Including Stopped Ones):**
  ```bash
  docker ps -a
  ```
- **Stop a Running Container:**
  ```bash
  docker stop mynginx
  ```
- **Start a Stopped Container:**
  ```bash
  docker start mynginx
  ```
- **Restart a Running Container:**
  ```bash
  docker restart mynginx
  ```
- **Remove a Stopped Container:**
  ```bash
  docker rm mynginx
  ```
- **Remove All Stopped Containers:**
  ```bash
  docker container prune
  ```
- **View Container Logs:**
  ```bash
  docker logs mynginx
  ```
- **Attach to a Running Container:**
  ```bash
  docker attach mynginx
  ```
- **Execute a Command Inside a Running Container:**
  ```bash
  docker exec -it mynginx /bin/bash
  ```

### **4. Docker Volumes**
- **Create a Volume:**
  ```bash
  docker volume create myvolume
  ```
- **List Volumes:**
  ```bash
  docker volume ls
  ```
- **Inspect a Volume:**
  ```bash
  docker volume inspect myvolume
  ```
- **Remove a Volume:**
  ```bash
  docker volume rm myvolume
  ```

### **5. Docker Networks**
- **List Networks:**
  ```bash
  docker network ls
  ```
- **Create a Network:**
  ```bash
  docker network create mynetwork
  ```
- **Connect a Container to a Network:**
  ```bash
  docker network connect mynetwork mynginx
  ```
- **Disconnect a Container from a Network:**
  ```bash
  docker network disconnect mynetwork mynginx
  ```
- **Remove a Network:**
  ```bash
  docker network rm mynetwork
  ```

### **6. Docker Compose**
- **Start Services in Detached Mode:**
  ```bash
  docker-compose up -d
  ```
- **Start Services and View Logs:**
  ```bash
  docker-compose up
  ```
- **Stop Services:**
  ```bash
  docker-compose down
  ```
- **View Service Logs:**
  ```bash
  docker-compose logs
  ```

### **7. Docker System Management**
- **View Disk Usage:**
  ```bash
  docker system df
  ```
- **Prune Unused Data (Images, Containers, Volumes, Networks):**
  docker system prune
  
