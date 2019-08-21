FROM node:alpine

LABEL maintainer="cyrusyun@qq.com"

WORKDIR /home

RUN wget https://github.com/mobz/elasticsearch-head/archive/master.zip -O elasticsearch-head.zip \
    && unzip elasticsearch-head.zip\
    && rm elasticsearch-head.zip \
    && mv elasticsearch-head-master elasticsearch-head \
    && cd elasticsearch-head \
    && npm install http-server \
    && npm install

WORKDIR /home/elasticsearch-head

EXPOSE 9100

CMD node_modules/http-server/bin/http-server _site -p 9100