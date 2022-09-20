FROM ubuntu

WORKDIR /home
RUN apt update
RUN apt -y install make
RUN apt  -y install gcc
RUN apt install libc6-dev
RUN apt  -y install pkg-config 
RUN apt  -y install wget
RUN wget https://download.redis.io/redis-stable.tar.gz
RUN tar -xzvf redis-stable.tar.gz
RUN cd redis-stable ; ls ; make ; make install
RUN cd /home ; rm redis-stable.tar.gz ; rm -r redis-stable
docker ps
EXPOSE 6379
CMD ["redis-server", "--protected-mode", "no"]