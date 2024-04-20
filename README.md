# ITI - Docker Lab 🐋

## Task 1: Working with Docker Hello-world Image
### Objective
Learn how to run a container using the hello-world image and manage containers and images.

### Steps
#### 1. Run a Container with hello-world Image
```bash
docker run hello-world

```
#### 2. Check Container Status and Explain
```bash
docker ps -a

```
#### 3. Start the Stopped Container
```bash
docker start 0fd82e8824de
```
#### 4. Remove the Container
```bash
docker rm 0fd82e8824de
```
#### 5. Remove the Image
```bash
docker rmi hello-world

```
---

## Task 2: Running Container with Ubuntu Image
### Objective
Run an Ubuntu container in interactive mode, create a file inside it, and manage containers.

### Steps
#### 1. Run Ubuntu Container in Interactive Mode
```bash
docker run -it ubuntu

```
#### 2. Create a File inside the Container
```bash
touch hello-docker
```
#### 3. Stop and Remove the Container
```bash
exit
```
```bash
docker rm 76428f97db9d
```
#### 4. Check File Status
```bash
file is removed
```
#### 5. What happened to hello-docker file?
```bash
file is deleted with container
```
#### 6. Remove All Stopped Containers
```bash
docker rm 76428f97db9d

```
#### 7. Bonus: Remove All Containers in One Command
```bash
docker rm $(docker ps -aqf "status=exited")
```

---
## Task 3: Creating a Custom Nginx Docker Image
### Objective
Create a custom Docker image using Nginx and a local HTML file.

### Steps
#### 1. Create a Local HTML File
```bash
```
#### 2. Write Dockerfile and Copy the HTML file to the Docker Image
```bash
```
#### 3. Run Container with New Image
```bash
```

#### 4. Test the Container, open your browser and navigate to http://localhost:8088 to check if everything is okay
```bash
```

