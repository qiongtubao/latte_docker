FROM ubuntu:16.04

ADD redis-5.0.0.tar.gz /
RUN mkdir -p /redis


RUN apt-get -yqq update
RUN apt-get install -y gcc make

WORKDIR /redis-5.0.0
RUN make 
RUN mv /redis-5.0.0/src/redis-server /redis/
RUN mv /redis-5.0.0/src/redis-cli /redis/

WORKDIR /
RUN rm -rf /redis-5.0.0

RUN apt-get remove --purge -y gcc make

# VOLUME ["/var/log/redis/"]
EXPOSE 6379