FROM debian:buster

RUN groupadd -g 1000 ubuntu \
        && useradd -u 1000 -d /home/ubuntu -g ubuntu ubuntu \
        && mkdir -p /home/ubuntu \
        && chown ubuntu:ubuntu /home/ubuntu \
        && chsh -s /bin/bash ubuntu \
        && usermod -aG sudo ubuntu

COPY 10-ubuntu /etc/sudoers.d

USER ubuntu
WORKDIR /home/ubuntu
