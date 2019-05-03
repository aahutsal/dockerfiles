FROM itatabitovski/debian:jessie

ENV FRANZ_VERSION 5.0.0-beta.15

RUN apt-install wget \
                libgtk2.0-0 \
                libxtst6 \
                libxss1 \
                libgconf-2-4 \
                libnss3 \
                libasound2 \
                alsa-utils

#RUN add-apt-repository ppa:ubuntu-toolchain-r/test
RUN apt-get update && apt-get upgrade

RUN	mkdir /opt/franz && cd /opt/franz && \
        apt-get update && \
	wget https://github.com/meetfranz/franz/releases/download/v$FRANZ_VERSION/franz-$FRANZ_VERSION.deb
RUN     apt-get upgrade -y
RUN     apt-get install franz-$FRANZ_VERION.deb



COPY entrypoint.sh /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]
