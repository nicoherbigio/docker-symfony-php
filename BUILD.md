# Building instructions for the Symfony PHP Docker image

Each Docker image to be created is based on a base Docker image.  
The configuration of a Docker image takes place in the respective `Dockerfile` file.

## Access to Docker Hub

A **one-time** authentication is required to upload Docker images to Docker Hub.

```
# Login to Docker Hub
docker login
```

## Build the Docker image

The following command is required to build the current version.

```
# Build the Docker image
docker build --no-cache --pull --tag nicoherbigde/symfony-php:8.1 8.1/debian/apache/default/
```

> **Hint:** For building an older version, the directory and file paths as well as the Docker tags must be adjusted accordingly, analogous to the previously mentioned command.

## Upload the Docker image

The following command is required to upload the current version.

```
# Upload the Docker image to Docker Hub
docker push nicoherbigde/symfony-php:8.1
```

> **Hint:** For uploading an older version, the Docker tags must be adjusted accordingly, analogous to the previously mentioned command.

## Copyleft

This documentation was written by Nico Herbig.
