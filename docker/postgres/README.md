Docker image for PostgreSQL on Ubuntu

## Getting Started

Build an image from the Dockerfile and assign it a name:

```
$ docker build -t docker-psql-image .
```

Run the PostgreSQL container (in the foreground):

```
$ docker run --rm -P --name psql-server docker-psql-image
```

Check the new image's port #

```
$ docker ps
```

Connect to psql from the host system:

```
$ psql -h localhost -p PORT_NUMBER -d docker -U docker --password
