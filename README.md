# Artemis image for EnMasse

[![Build Status](https://travis-ci.org/EnMasseProject/artemis-image.svg?branch=master)](https://travis-ci.org/EnMasseProject/artemis-image)

This repository contains
   * Dockerfile for building container image
   * Startup scripts and configuration for Artemis running in containers
   * Shutdown hooks for use when running in OpenShift
   * Launcher for blocking SIGTERM in OpenShift


## Build instructions

    gradle buildArtemis assemble build distTar downloadArtemis
    docker build .

## Export/Import of Docker Image

    docker save -o artemis.tar [artemis-image-id]
    docker load -i artemis.tar
    docker tag [artemis-image-id] docker.io/enmasseproject/artemis

