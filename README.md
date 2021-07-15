This repository contains a sample implementation of a blog application, designed to show off various features of OpenShift. The blog application is implemented using Python and Django.

In the default deployment configuration, the blog application uses a SQLite database within the container. When using the SQLite database, it will be pre-populated each time the application starts with a set of blog posts. An initial account will also be created for logging into the application to add more posts. The user name for this account is ``developer`` and the password is ``developer``.

Because the SQLite database is stored in the container, new posts and any uploaded images, will be lost when the container restarts. A PostgreSQL database can be attached to the application to add persistence for posts and demonstrate the use of a database. A separate persistent volume can also be attached to the blog application to provide persistent storage for uploaded images. In the case of PostgreSQL being used, a manual step is required to setup the database the first time.

The appearance of the blog application can also be adjusted using a set of environment variables to make it easier to demonstrate blue/green or a/b deployments, split traffic etc.

# Builging from Image Strategy

[Deploying using the image strategy](DeployingUsingExistingImage.adoc)

# Building from source code strategy


A source build and deployment can be run direct from this repository.

[Deploying using the source strategy](DeployingUsingS2I.adoc)


# Building from Dockerfile strategy

A docker build and deployment can be run direct from this repository.

[Deploying using the docker strategy](DeployingUsingDocker.adoc)

# Managing the app

[Managing the application](ApplicationManagement.adoc)
