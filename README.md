# Resources
Inter Process Communication<br>
JDK Download - https://download.oracle.com/java/21/latest/jdk-21_linux-x64_bin.deb<br>
Maven Download - [https://dlcdn.apache.org/maven/maven-3/3.9.8/binaries/apache-maven-3.9.8-bin.zip](https://dlcdn.apache.org/maven/maven-3/3.9.8/binaries/apache-maven-3.9.8-bin.tar.gz)<br>
Spring CLI - [https://repo.maven.apache.org/maven2/org/springframework/boot/spring-boot-cli/3.3.2/spring-boot-cli-3.3.2-bin.zip] <br>(https://repo.maven.apache.org/maven2/org/springframework/boot/spring-boot-cli/3.3.2/spring-boot-cli-3.3.2-bin.tar.gz)
Download files - https://drive.google.com/drive/folders/1GxyNqbhmHMFIdb3ABYA8D_NImu4_SpwO?usp=drive_link <br>

Here are some of the basic Docker commands that are commonly used:

### Docker Installation and Configuration
1. **Install Docker**: Follow the official installation guide for your operating system.
2. **Check Docker Version**:
   ```sh
   docker --version
   ```

### Docker Images
3. **Pull an Image**:
   ```sh
   docker pull [image-name]
   ```
   Example: `docker pull nginx`
4. **List Images**:
   ```sh
   docker images
   ```
5. **Build an Image**:
   ```sh
   docker build -t [image-name] .
   ```
   Example: `docker build -t myapp:latest .`
6. **Remove an Image**:
   ```sh
   docker rmi [image-id or image-name]
   ```
7. **Tag an Image**:
   ```sh
   docker tag [image-id or image-name] [new-repo]:[tag]
   ```
   Example: `docker tag myapp:latest myrepo/myapp:1.0`

### Docker Containers
8. **Run a Container**:
   ```sh
   docker run [options] [image-name]
   ```
   Example: `docker run -it ubuntu`
   - Common options:
     - `-d`: Run container in detached mode.
     - `-p`: Publish a container's port(s) to the host.
     - `-v`: Bind mount a volume.
     - `--name`: Assign a name to the container.
9. **List Running Containers**:
   ```sh
   docker ps
   ```
10. **List All Containers**:
    ```sh
    docker ps -a
    ```
11. **Stop a Running Container**:
    ```sh
    docker stop [container-id or container-name]
    ```
12. **Start a Stopped Container**:
    ```sh
    docker start [container-id or container-name]
    ```
13. **Restart a Container**:
    ```sh
    docker restart [container-id or container-name]
    ```
14. **Remove a Container**:
    ```sh
    docker rm [container-id or container-name]
    ```
15. **Remove All Stopped Containers**:
    ```sh
    docker container prune
    ```

### Docker Volumes
16. **Create a Volume**:
    ```sh
    docker volume create [volume-name]
    ```
17. **List Volumes**:
    ```sh
    docker volume ls
    ```
18. **Inspect a Volume**:
    ```sh
    docker volume inspect [volume-name]
    ```
19. **Remove a Volume**:
    ```sh
    docker volume rm [volume-name]
    ```
20. **Remove All Unused Volumes**:
    ```sh
    docker volume prune
    ```

### Docker Networks
21. **Create a Network**:
    ```sh
    docker network create [network-name]
    ```
22. **List Networks**:
    ```sh
    docker network ls
    ```
23. **Inspect a Network**:
    ```sh
    docker network inspect [network-name]
    ```
24. **Remove a Network**:
    ```sh
    docker network rm [network-name]
    ```
25. **Remove All Unused Networks**:
    ```sh
    docker network prune
    ```

### Docker Compose
26. **Start Services**:
    ```sh
    docker-compose up
    ```
27. **Start Services in Detached Mode**:
    ```sh
    docker-compose up -d
    ```
28. **Stop Services**:
    ```sh
    docker-compose down
    ```
29. **View Compose Logs**:
    ```sh
    docker-compose logs
    ```

These commands cover the basic operations for managing Docker images, containers, volumes, and networks. Docker Compose commands are included for managing multi-container Docker applications.
