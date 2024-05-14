# hash:sha256:e9970e379ffb15a83da2ae25202158d2d415b7f671b3c72059f321fd9d79a30b
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/py-r:python3.10.12-R4.2.2-IRkernel-ubuntu22.04

ARG DEBIAN_FRONTEND=noninteractive

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

RUN mamba install -y \
        matplotlib==3.7.2 \
    && mamba clean -ya
