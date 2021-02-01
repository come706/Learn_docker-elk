FROM docker.elastic.co/beats/filebeat:7.9.2

LABEL maintainer="genius840215@163.com"

COPY ./config/filebeat.yml /usr/share/filebeat/filebeat.yml

USER root

RUN chown root:filebeat /usr/share/filebeat/filebeat.yml

RUN echo "Asia/Shanghai" > /etc/timezone

USER filebeat

RUN filebeat modules enable nginx