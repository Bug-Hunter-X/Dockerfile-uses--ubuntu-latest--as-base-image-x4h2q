# Dockerfile Best Practices: Avoid Using `ubuntu:latest`

This repository demonstrates a common mistake in Dockerfiles: using `ubuntu:latest` as the base image.  This practice can lead to unpredictable build failures and inconsistencies due to frequent updates to the `latest` tag.  The solution provided shows how to specify a specific version of Ubuntu for better reproducibility and stability.

## Problem

Using `ubuntu:latest` results in a Docker image built on the latest version of Ubuntu available at build time. Subsequent builds might use a different version, leading to incompatibility issues and broken builds.

## Solution

Specify a particular version of Ubuntu to create a reproducible and stable build environment.  For example, use `ubuntu:20.04` or any other specific version.  This ensures that the base image remains consistent across builds.