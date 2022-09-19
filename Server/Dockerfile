FROM alpine


WORKDIR /home
RUN apk update
RUN apk -y install gcc
RUN apk -y install libc6-dev
RUN apk -y install pkg-config 
RUN apk -y install wget
RUN wget https://download.redis.io/redis-stable.tar.gz
RUN tar -xzvf redis-stable.tar.gz
RUN cd redis-stable
RUN make
RUN make install


# RUN apk-get -y install redis
EXPOSE 6379
CMD ["redis-server", "--protected-mode", "no"]

