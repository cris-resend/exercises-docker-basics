FROM ubuntu:24.04

WORKDIR /usr/src/app

COPY script.sh .

RUN chmod +x script.sh
RUN apt update && apt upgrade -y
RUN apt install curl -y

CMD ["./script.sh"]