# Docker Notes

## Creating containers

### Using `dockerfile`

You can create a docker image from a `dockerfile` which contains all the information.

### Using `docker-compose`

A `docker-compose` file contains information about multiple services you want to create in one batch. It's in a `yaml` format.

An example of a `yaml` file if found below. It will download the alpine image and add it to the containers. Then if will execute the command specified.

```yaml
version: "3"
service:
    service-name:
        container_name: some-name #name shown in the docker container overview.
        image: alpine #name of the image to pull from repository
        volumes:
        - ./file:/app #mount the local file folder to the container app folder.
        command: [ /bin/sh, -c, "chmod +x /app/app.sh && ./app/app.sh"]
```

## Connecting to containers

### Connect using a shell

First get the ID of the container you want to connect to

`docker ps`

Then connect to the container using the exec command

`docker exec -it <CONTAINER_ID> sh`