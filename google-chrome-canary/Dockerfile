FROM debian:11

RUN apt update && apt upgrade -y; \
    apt install wget -y; \
    wget -c https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb

RUN apt install ./google-chrome-stable_current_amd64.deb -y

CMD ["google-chrome-stable", "--no-sandbox"]