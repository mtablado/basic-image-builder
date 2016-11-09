# basic-image-builder

This is the main image builder for jenkins slaves. It works as a Docker in Docker (dind) container and allows you to execute docker commands (pull, push, login, etc).

This image extends [tehranian/dind-jenkins-slave](https://github.com/tehranian/dind-jenkins-slave), so its requirements and limitations are also extended. Read it instructions carefully!

The main difference is that this implementation upgrades docker to version 1.12.2-0 and adds `--insecure-registry docker-virtual.art.local` to docker daemon args so that it can work with local artifactory.