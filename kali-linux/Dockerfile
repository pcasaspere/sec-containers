FROM kalilinux/kali-rolling

LABEL maintainer="Pere Casas"

ARG DEBIAN_FRONTEND=noninteractive

ENV TZ=Europe/Andorra

RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

## https://airman604.medium.com/kali-linux-in-a-docker-container-5a06311624eb

RUN apt update \
    && apt full-upgrade -y \
    && apt install -y kali-linux-headless

RUN apt install -y sublist3r

RUN apt install -y mtr iputils-ping nano
RUN apt autoremove \
    && apt clean

CMD [ "bash" ]