FROM debian:stable

EXPOSE 8123:8123

RUN apt-get update -y
RUN apt-get upgrade -y

RUN apt-get install python3 python3-dev python3-venv python3-pip -y

RUN pip3 --version
RUN pip3 install wheel
RUN pip3 install sqlalchemy
RUN pip3 install homeassistant

#executar pra subir
CMD hass --open-ui

#WORKDIR /home/notebooks

