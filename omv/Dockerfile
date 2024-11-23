FROM debian:stable

RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get install wget -y
RUN apt update && apt install tzdata -y

RUN apt-get install --yes gnupg

ENV TZ="America/Sao_Paulo"

RUN wget -O "/etc/apt/trusted.gpg.d/openmediavault-archive-keyring.asc" https://packages.openmediavault.org/public/archive.key
RUN apt-key add "/etc/apt/trusted.gpg.d/openmediavault-archive-keyring.asc"

RUN printf '#!/bin/sh\nexit 0' > /usr/sbin/policy-rc.d


COPY install.sh /
RUN chmod +x /install.sh

 

#CMD ["/install.sh"]

#CMD ["/bin/bash"]

