FROM ubuntu:18.04

USER root

# https://www.postgresql.org/download/linux/ubuntu/
# https://wiki.postgresql.org/wiki/Apt
RUN apt-get update
RUN apt-get install -y wget gnupg2 lsb-release

RUN sh -c 'echo "deb https://apt-archive.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
RUN wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | apt-key add -
RUN apt-get update
RUN apt-get install -y postgresql-client-14

RUN echo `psql --version`