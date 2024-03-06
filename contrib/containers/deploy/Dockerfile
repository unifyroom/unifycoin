FROM phusion/baseimage:focal-1.0.0
LABEL maintainer="Unifyroom Developers <dev@unifyroom.com>"
LABEL description="Dockerised UnifyroomCore, built from Travis"

ARG USER_ID
ARG GROUP_ID

ENV HOME /home/unfy

# add user with specified (or default) user/group ids
ENV USER_ID ${USER_ID:-1000}
ENV GROUP_ID ${GROUP_ID:-1000}
RUN groupadd -g ${GROUP_ID} unfy && \
    useradd -u ${USER_ID} -g unfy -s /bin/bash -m -d /home/unfy unfy && \
    mkdir /home/unfy/.unfycore && \
    chown ${USER_ID}:${GROUP_ID} -R /home/unfy

COPY bin/* /usr/local/bin/

RUN chmod a+x /usr/local/bin/*

USER unfy

VOLUME ["/home/unfy"]

EXPOSE 9998 9999 19998 19999

WORKDIR /home/unfy
