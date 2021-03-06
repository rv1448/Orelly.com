## CONTAINER COMMANDS

> docker run [options] [name]
> docker run -d alpine

- Inspect the container information and get a JSON response
> docker inspect <friendlyname|container-id>
> docker inspect 3d82b110ecab

- Get the logs from the docker container
> docker logs <friendly-name|container-id>
> docker logs 3d82b110ecab

- Get the port of the container that's exposing the service
> docker port <container-id> || docker port <friendly-name>
> docker port redd || docker port 187de6ba5880



## Container
	- Image will produce same container
	- Container is a running instance of a image
	- images are stored in a HUB or registry
	- we can write to container based on the persisted volume

``` bash
Docker image is built up from layers
FROM ubuntu:18.04
COPY . /app
RUN make /app
CMD python /app/app.py

FROM mysql:5.5.45
```
```
	- Each command is a layer
	- Each layer is Read only except top one
	- top one is R/W layer
	- ANy chnges will go into the top layer
	- docker build to build the image
```
docker history image-name
```
	- Lower Layers are immutable
	- R/O - read only
	- R/W - read write
	- UNION file system service
	- CGROUP and NAMESPACE
	- multiple containers can share access to the same underlying base layer and yet have their own data
	- docker build -t {IMAGENAME:tag the docker file}
	- docker images
	-
```

## Container Under the Hood

- what does "Container" mean to you ?

-
-
