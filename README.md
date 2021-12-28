# docker-spring-boot-mariadb-phpmyadmin
Docker-Compose file template for Spring Boot + MariaDB + phpMyAdmin
## Usage
Run containers
> docker-compose up -d

Stop containers
> docker-compose down


Clean unused
> docker system prune -a


## Remarks
- Adapt jar file name and Java version to use in *Dockerfile-web*
- Remove IP 127.0.0.1 on *ports* to allow remote access to services (leave 127.0.0.1 to work with an nginx reverse-proxy)
- Logs are located in *log*
- Spring Boot .jar file need to be placed in *web*
- Database files are placed in *mariadb*
- Use *db* as host for mariadb connection Spring Boot datasource

## Spring Boot configuration
> server.port=80<br>
> logging.file.path=/var/logs<br>
> spring.datasource.url=jdbc:mariadb://db/database<br>
> spring.datasource.username=admin<br>
> spring.datasource.password=admin<br>
> spring.datasource.hikari.driver-class-name=org.mariadb.jdbc.Driver<br>
