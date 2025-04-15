# Volumes in Docker

Docker container creates temporary storage when its created, lifetime of temporary storage volume is till the container available. once new container created it will create new volume and clear all data into container volume.

There are applications, database where it requires to persist data. Volume is the preferred mechanism we can setup and mount to specific location in docker container to save and persist data.

We can create docker volume using ``` docker volume create ``` command.

```
Docker volume create <name of the volume>
```
```
docker run -v C:\Ankit\mytemp:/root/myvol -dit busybox 
```
```ymml
version: '3.9'
services:
  postgres:
    image: postgres:14-alpine
    ports:
      - 5432:5432
    volumes:
      - ~/apps/postgres:/var/lib/postgresql/data
    environment:
      - POSTGRES_PASSWORD=S3cret
      - POSTGRES_USER=citizix_user
      - POSTGRES_DB=citizix_db
```

