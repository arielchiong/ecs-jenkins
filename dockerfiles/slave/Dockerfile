FROM cloudbees/jnlp-slave-with-java-build-tools
MAINTAINER ariel.chiong@gmail.com

# Switch to root for installation
USER root

# Install Docker within Docker
ADD https://get.docker.com/builds/Linux/x86_64/docker-1.11.0.tgz /
RUN tar -xvzf /docker-1.11.0.tgz && \
    mv docker/* /usr/bin/

# Update and install ansible
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get dist-upgrade -y && \
    apt-get autoremove -y && \
    apt-get autoclean -y && \
    apt-get install ansible -y
