# Swifty docker's 📦😍

This repository contains Dockerfiles to build docker images with swift and the configurations needed for our services or development in general.

To know more about our development and deployment process, check out our [Playbook](https://github.com/YouClap/Playbook)

# Contents

## Dockerfile ssl dev

Compiles a docker image with SSL for development and compile purposes.
For example, we use [Swift NIO](https://github.com/apple/swift-nio) and `NIOTLS` depends on `openssl` and so, in order to be able to build our services in Linux, we need to install `libssl-dev`.

## Dockerfile ssl

Compiles a docker image with SSL for running purposes.
Allows you to run an executable that requires `SSL`.



# Next steps

- [ ] Improve dockerfile naming and generation
- [ ] Add a pipeline to build and push images directly to the registry
- [ ] Automatic tag versions. Perhaps use swift version and openssl version, who knows.

# About

With ❤️ from [YouClap](https://youclap.tech) [Development team](mailto://development@youclap.tech)
