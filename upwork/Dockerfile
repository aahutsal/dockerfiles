FROM debian:latest

RUN apt update && apt upgrade -y
RUN apt install wget -y
RUN wget -c https://updates-desktopapp.upwork.com/binaries/v5_2_3_717_7tq7l0sg49p0kixc/upwork_5.2.3.717_amd64.deb
RUN apt install ./upwork_5.2.3.717_amd64.deb -y