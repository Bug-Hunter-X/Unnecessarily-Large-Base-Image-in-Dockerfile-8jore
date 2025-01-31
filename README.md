# Dockerfile Optimization
This repository demonstrates an issue with unnecessarily large Docker images and its solution.

## Problem
The original `Dockerfile` uses `ubuntu:latest`, a large base image. This results in larger image sizes and slower build times.

## Solution
The `Dockerfile_optimized` uses a slimmer base image (`ubuntu:22.04-slim`) and optimizes the installation process to reduce the image size.

## How to reproduce
1. Clone this repository.
2. Build the original Dockerfile: `docker build -t large-image -f Dockerfile .`
3. Build the optimized Dockerfile: `docker build -t slim-image -f Dockerfile_optimized .`
4. Compare the image sizes using `docker images`.