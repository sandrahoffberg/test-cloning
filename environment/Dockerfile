# hash:sha256:63e3ae8c0f1a10e0e94b519da96f99e9920e28af517afc1a8fe9d88c2b9e7739
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/py-r:python3.10.12-R4.2.2-IRkernel-ubuntu22.04

ARG DEBIAN_FRONTEND=noninteractive

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

RUN mamba install -y \
        matplotlib==3.7.2 \
    && mamba clean -ya

RUN echo 'options(repos = c(CRAN = "http://cran.wustl.edu/"), download.file.method = "libcurl")' >> $(Rscript -e 'cat(R.home())')/etc/Rprofile.site
RUN Rscript -e 'remotes::install_version("RMySQL")'
