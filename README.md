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
docker ps -a
container and file are removed
```
#### 5. What happened to hello-docker file?
```bash
any changes made inside the container exists as long as the container exists.
When the container is removed, all its changes are removed.
```
#### 6. Remove All Stopped Containers
```bash
docker rm 76428f97db9d
```
#### 7. Bonus: Remove All Containers in One Command
```bash
docker rm $(docker ps --filter status=exited -q)
```

---
## Task 3: Creating a Custom Nginx Docker Image
### Objective
Create a custom Docker image using Nginx and a local HTML file.

### Steps
#### 1. Create a Local HTML File
```bash
vi index.html
```
#### 2. Write Dockerfile and Copy the HTML file to the Docker Image
```bash
vi Dockerfile
```
```bash
FROM nginx:alpine

COPY index.html /usr/share/nginx/html/index.html
```
#### 3. Build a new Docker image from the above Dockerfile and tag it with this pattern nginx-your-name.
```bash
ocker build -t nginx-talaat .
```
#### 4. Run Container with New Image
```bash
docker run -d -p 8088:80 nginx-talaat
```

#### 5. Test the Container, open your browser and navigate to http://localhost:8088 to check if everything is okay
```bash
 http://localhost:8088 works just fine and name in index.html is displayed
```

