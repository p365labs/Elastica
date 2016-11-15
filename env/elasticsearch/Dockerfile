FROM docker.elastic.co/elasticsearch/elasticsearch:latest
MAINTAINER Nicolas Ruflin <spam@ruflin.com>

RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install mapper-attachments
RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install discovery-file

# Copy config files
COPY elasticsearch.yml /usr/share/elasticsearch/config/elasticsearch.yml
COPY unicast_hosts.txt /usr/share/elasticsearch/config/discovery-file/unicast_hosts.txt
COPY scripts/* /usr/share/elasticsearch/config/scripts/


RUN mkdir -p /tmp/backups1/backup1
RUN mkdir -p /tmp/backups1/backup2
RUN mkdir -p /tmp/backups2/backup1
RUN mkdir -p /tmp/backups2/backup2
