# Documentación de Contenedores Docker de Sistemas Gestores de Base De Datos

## Contenedor de tutorial de docker
docker pull docker/getting-started

docker pull mcr.microsoft.com/mssql/server:2022-latest

docker pull postgres:14.22-trixie 

docker run -d -p 80:80 docker/getting-started

- -d detach (El proceso del contenedor se ejecuta en background)
- -p (port, publish) (Mapea el puerto)
- docker/getting-started (Nombre de la imagen)
## Contenedor del DBMS MariaDB
docker pull mariadb

## Comandos Docker
| Comando | Descripción |
| :--- | :--- |
| docker pull nombre_imagen | **Descarga una imagen de DockerHub** [Docker Hub](https://hub.docker.com/) |
| docker images | **Visualizar las imagenes que se encuentran en el docker** |
![Imagen Docker](./img/imagen_docker.png)