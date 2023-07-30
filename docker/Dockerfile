# start from a fresh ubuntu image
FROM ubuntu:23.04

# install basic tools
RUN apt-get update && \
    apt-get install -y curl wget bash git nano sudo unzip

# use non-root user
RUN passwd --delete ubuntu && \
    echo "ubuntu ALL=(ALL:ALL) NOPASSWD: ALL" | tee /etc/sudoers.d/ubuntu
USER ubuntu

# install cool ass looking bash prompt
RUN printf "\nsource /com.docker.devenvironments.code/docker/bash.sh" | tee -a ~/.bashrc

# install deno
RUN curl -s https://gist.githubusercontent.com/LukeChannings/09d53f5c364391042186518c8598b85e/raw/ac8cd8c675b985edd4b3e16df63ffef14d1f0e24/deno_install.sh | sh