# Resources
Inter Process Communication<br>
JDK Download - https://download.oracle.com/java/21/latest/jdk-21_linux-x64_bin.deb<br>
Maven Download - [https://dlcdn.apache.org/maven/maven-3/3.9.8/binaries/apache-maven-3.9.8-bin.zip](https://dlcdn.apache.org/maven/maven-3/3.9.8/binaries/apache-maven-3.9.8-bin.tar.gz)<br>
Spring CLI - [https://repo.maven.apache.org/maven2/org/springframework/boot/spring-boot-cli/3.3.2/spring-boot-cli-3.3.2-bin.zip] (https://repo.maven.apache.org/maven2/org/springframework/boot/spring-boot-cli/3.3.2/spring-boot-cli-3.3.2-bin.tar.gz)<br>
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


Sure! Here's an explanation of each command, without changing the commands themselves.

### Command 1:
```sh
docker run --name mysql-container -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=test_db -e MYSQL_PASSWORD=password -p 3306:3306 -d <MySQL_ID>
```

**Explanation:**
- `docker run`: Run a new Docker container.
- `--name mysql-container`: Name the container `mysql-container`.
- `-e MYSQL_ROOT_PASSWORD=password`: Set the root password for MySQL to `password`.
- `-e MYSQL_DATABASE=test_db`: Create a database named `test_db`.
- `-e MYSQL_PASSWORD=password`: Set the MySQL password for the root user to `password`.
- `-p 3306:3306`: Map port 3306 on the host to port 3306 on the container.
- `-d <MySQL_ID>`: Run the container in detached mode using the image with ID `<MySQL_ID>`.

### Command 2:
```sh
docker run --name mysql-container -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=test_db -e MYSQL_PASSWORD=password -p 3306:3306 -d mysql:latest
```

**Explanation:**
- `docker run`: Run a new Docker container.
- `--name mysql-container`: Name the container `mysql-container`.
- `-e MYSQL_ROOT_PASSWORD=password`: Set the root password for MySQL to `password`.
- `-e MYSQL_DATABASE=test_db`: Create a database named `test_db`.
- `-e MYSQL_PASSWORD=password`: Set the MySQL password for the root user to `password`.
- `-p 3306:3306`: Map port 3306 on the host to port 3306 on the container.
- `-d mysql:latest`: Run the container in detached mode using the `mysql:latest` image.

### Command 3:
```sh
docker run --name spring-boot-docker --link <MYSQL_Container_ID> -p 8081:8080 -e SPRING_DATASOURCE_URL=jdbc:mysql://<MYSQL_Container_ID>:3306/test_db -e SPRING_DATASOURCE_USERNAME=root -e SPRING_DATASOURCE_PASSWORD=password -d <Spring_Image_ID>
```

**Explanation:**
- `docker run`: Run a new Docker container.
- `--name spring-boot-docker`: Name the container `spring-boot-docker`.
- `--link <MYSQL_Container_ID>`: Link this container to the MySQL container with ID `<MYSQL_Container_ID>`.
- `-p 8081:8080`: Map port 8081 on the host to port 8080 on the container.
- `-e SPRING_DATASOURCE_URL=jdbc:mysql://<MYSQL_Container_ID>:3306/test_db`: Set the environment variable `SPRING_DATASOURCE_URL` to the JDBC URL of the MySQL database.
- `-e SPRING_DATASOURCE_USERNAME=root`: Set the environment variable `SPRING_DATASOURCE_USERNAME` to `root`.
- `-e SPRING_DATASOURCE_PASSWORD=password`: Set the environment variable `SPRING_DATASOURCE_PASSWORD` to `password`.
- `-d <Spring_Image_ID>`: Run the container in detached mode using the image with ID `<Spring_Image_ID>`.

### Command 4:
```sh
docker run --name spring-boot-docker --link 752cf42e611c -p 8081:8080 -e SPRING_DATASOURCE_URL=jdbc:mysql://752cf42e611c:3306/test_db -e SPRING_DATASOURCE_USERNAME=root -e SPRING_DATASOURCE_PASSWORD=password -d 609619ce6d75
```

**Explanation:**
- `docker run`: Run a new Docker container.
- `--name spring-boot-docker`: Name the container `spring-boot-docker`.
- `--link 752cf42e611c`: Link this container to the MySQL container with ID `752cf42e611c`.
- `-p 8081:8080`: Map port 8081 on the host to port 8080 on the container.
- `-e SPRING_DATASOURCE_URL=jdbc:mysql://752cf42e611c:3306/test_db`: Set the environment variable `SPRING_DATASOURCE_URL` to the JDBC URL of the MySQL database.
- `-e SPRING_DATASOURCE_USERNAME=root`: Set the environment variable `SPRING_DATASOURCE_USERNAME` to `root`.
- `-e SPRING_DATASOURCE_PASSWORD=password`: Set the environment variable `SPRING_DATASOURCE_PASSWORD` to `password`.
- `-d 609619ce6d75`: Run the container in detached mode using the image with ID `609619ce6d75`.
