FROM nginx

WORKDIR /usr/share/nginx/html

RUN apt-get update && \
    apt-get install -y git

RUN git clone https://github.com/Sebastianpkmn/okon /tmp/okon

RUN cp -r /tmp/okon/* .

RUN rm -rf /tmp/okon

EXPOSE 80
