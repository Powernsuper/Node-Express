FROM alpine

WORKDIR /home
RUN apk update
RUN apk add make
RUN apk add musl
RUN apk add gcc
RUN apk add gcompat
RUN apk  add pkgconfig 
RUN apk  add wget

RUN wget https://download.redis.io/redis-stable.tar.gz
RUN tar -xzvf redis-stable.tar.gz
RUN cd redis-stable ; ls ; make ; make install
# RUN make install


# RUN apk-get  install redis
EXPOSE 6379
CMD ["redis-server", "--protected-mode", "no"]

