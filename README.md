# building a CentOS 8 toy system for singularity and docker image for CI

Tru <tru@pasteur.fr>

## Why ?
- CentOS-8 system for github actions
- build docker image, push to ghcr.io and re-use that docker image to create a singularity container pushed ghcr.io oras://
- 
## Caveat
- playground, use at your own risk!
- `:main` tagged docker image
- `:latest` tagged singularity image

## Usage
- Docker [![Docker build](https://github.com/truatpasteurdotfr/singularity-docker-centos8-ci/actions/workflows/docker-publish.yml/badge.svg)](https://github.com/truatpasteurdotfr/singularity-docker-centos8-ci/actions/workflows/docker-publish.yml)
```
docker pull ghcr.io/truatpasteurdotfr/singularity-docker-centos8-ci:main
```

- Singularity [![Singularity build](https://github.com/truatpasteurdotfr/singularity-docker-centos8-ci/actions/workflows/singularity-publish.yml/badge.svg)](https://github.com/truatpasteurdotfr/singularity-docker-centos8-ci/actions/workflows/singularity-publish.yml)
```
singularity run oras://ghcr.io/truatpasteurdotfr/singularity-docker-centos8-ci:latest
```
