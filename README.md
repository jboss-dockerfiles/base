# Base Docker images for JBoss community projects

This repository contains multiple base images that are used to build the portfolio of Docker images for JBoss community projects. 

Currently the repository contains following images:

1. Base image with environemnt changes,
2. Image with OpenJDK 7 installed on top of the base image.

## Base image

This image is used as a base image for *all* JBoss community images. It provides a base layer that includes:

1. A `jboss` user (uid/gid `1000`) with home directory set to `/opt/jboss`
2. A few tools that may be useful when extending the image or installing software, like `unzip`.

### Operating system

This image uses Fedora 20.

### Working directory

This image has the working directory set to `/opt/jboss`, which is the `jboss` user home directory at the same time.

### Availability

The `Dockerfile` is available in the `master` branch and is built in the Docker HUB as `jboss/base:latest`.

## JDK 7 base image

This image **extends** the `jboss/base:latest` image and adds OpenJDK 7 distribution. Additionally it adds a `JAVA_HOME` environment variable.

### Availability

The `Dockerfile` is available in the `jdk7` branch and is built in the Docker HUB as `jboss/base:jdk7`.
