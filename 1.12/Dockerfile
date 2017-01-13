FROM ubuntu:16.04

RUN apt-get update
RUN apt-get install -y --no-install-recommends linux-image-extra-$(uname -r) linux-image-extra-virtual apt-transport-https ca-certificates

RUN apt-key adv \
               --keyserver hkp://ha.pool.sks-keyservers.net:80 \
               --recv-keys 58118E89F3A912897C070ADBF76221572C52609D

RUN echo "deb https://apt.dockerproject.org/repo ubuntu-xenial main" | tee /etc/apt/sources.list.d/docker.list

RUN apt-get update

ENTRYPOINT ["/bin/bash"]
