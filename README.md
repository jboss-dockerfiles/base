# Base Docker image for Middleware

This image is used as a base image for *all* JBoss community images. It provides a bas elayer that includes:

1. A `jboss` user with home directory set to `/opt/jboss`
2. A few tools that may be useful when extending the image or installing software, like `unzip`.
