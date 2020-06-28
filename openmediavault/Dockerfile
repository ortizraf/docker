FROM debian:stable

EXPOSE 80:80

RUN apt-get update -y
RUN apt-get upgrade -y

RUN apt-get install wget -y
RUN apt-get update && apt-get install -y procps

#ENTRYPOINT ["/usr/sbin/init"]
#CMD ["systemctl"]

RUN wget -O - https://github.com/OpenMediaVault-Plugin-Developers/installScript/raw/master/install | bash

RUN echo "OpenMediaVault"

#RUN while true; do sleep 1000; done