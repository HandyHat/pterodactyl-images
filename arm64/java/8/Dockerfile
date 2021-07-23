FROM        adoptopenjdk/openjdk8:debianslim-jre

LABEL       author="HandyHat" maintainer="aniket@gargs.co.uk"

RUN apt-get update -y \
 && apt-get install -y curl ca-certificates openssl git tar sqlite fontconfig tzdata iproute2 libjpeg-dev libpng-dev libtiff-dev libgif-dev webp \
 && useradd -d /home/container -m container
 
USER container
ENV  USER=container HOME=/home/container

USER        container
ENV         USER=container HOME=/home/container

WORKDIR     /home/container

COPY        ./entrypoint.sh /entrypoint.sh

CMD         ["/bin/bash", "/entrypoint.sh"]
