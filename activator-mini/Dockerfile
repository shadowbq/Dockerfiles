# Typesafe Activator Minimal

FROM flurdy/oracle-java7:latest

MAINTAINER flurdy

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && \
  apt-get install -yq wget unzip && \
  apt-get autoremove -yq && \
  apt-get clean -yq && \
  rm -rf /var/lib/apt/lists/*

ENV ACTIVATOR_VERSION 1.2.10

RUN cd /tmp && \
  wget http://downloads.typesafe.com/typesafe-activator/$ACTIVATOR_VERSION/typesafe-activator-$ACTIVATOR_VERSION-minimal.zip && \
  unzip typesafe-activator-$ACTIVATOR_VERSION-minimal.zip && \
  mkdir /opt/typesafe && \
  mv /tmp/activator-$ACTIVATOR_VERSION-minimal /opt/typesafe/activator-$ACTIVATOR_VERSION && \
  ln -s /opt/typesafe/activator-$ACTIVATOR_VERSION/activator /usr/local/bin/activator && \
  rm /tmp/typesafe-activator-$ACTIVATOR_VERSION-minimal.zip
