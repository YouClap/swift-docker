# Swifty docker's 📦😍

This repository contains Dockerfiles to build docker images with swift and the configurations needed for our services or development in general.

To know more about our development and deployment process, check out our [Playbook](https://github.com/YouClap/Playbook)

# Contents 📨

## Dockerfile ssl dev 

Compiles a docker image with SSL for development and compile purposes.
For example, we use [Swift NIO](https://github.com/apple/swift-nio) and `NIOTLS` depends on `openssl` and so, in order to be able to build our services in Linux, we need to install `libssl-dev`.

## Dockerfile ssl

Compiles a docker image with SSL for running purposes.
Allows you to run an executable that requires `SSL`.

# How can i use those images? 🚧

They are public in the docker container registry, so if you searcb for `swift-ssl` you will find it.
You can also see them in our [docker hub organization page](https://cloud.docker.com/u/youclap)

They use the swift version as the tag for the image.

For now, until we find out a better way to generate images without have to duplicate each Dockerfile, you only have the `5.0.1` version available.

# How to build an image 🔨

It's easy, you just need to specify the path to the Dockerfile you want to use as source.

For example, let's build the image with SSL for production only, we use the `Dockerfile-ssl` and let's tag it with `youclap/swift-ssl-dev:5.0.1`

`docker build -f Dockerfile-ssl -t youclap/swift-ssl-dev:5.0.1`

That's it, now just push it to  the registry 😊

# Next steps

- [ ] Improve dockerfile naming and generation
- [ ] Add a pipeline to build and push images directly to the registry
- [ ] Automatic tag versions. Perhaps use swift version and openssl version, who knows.

# About

With ❤️ from [YouClap](https://youclap.tech) [Development team](mailto://development@youclap.tech)
