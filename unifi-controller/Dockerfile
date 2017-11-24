#
# docker run --rm -it --net=host -p 8080:8080 -p 8443:8443 -p 8880:8880 -p 8843:8843 -p 3478:3478/udp -p 10001:10001/udp --name unifi rstanleyhum/unifi
#
# Remember to add an external network adapter to the HyperV moby
# also add apt-get install net-tools to find ip address
# start with: service unifi start
# https://ip address:8443/
#

FROM ubuntu:16.04

LABEL maintainer="r.stanley.hum@gmail.com"


RUN echo 'deb http://www.ubnt.com/downloads/unifi/debian stable ubiquiti' > /etc/apt/sources.list.d/100-ubnt.list

RUN  apt-key adv --keyserver keyserver.ubuntu.com --recv 06E85760C0A52C50

RUN apt-get update

RUN apt-get -y install unifi

RUN apt-get -y upgrade

RUN service unifi start
