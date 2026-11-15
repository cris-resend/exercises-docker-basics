FROM ubuntu:latest

WORKDIR /usr/src/app

RUN apt-get update && apt-get install curl -y

RUN curl -sL https://deb.nodesource.com/setup_16.x | bash && apt-get install nodejs -y

COPY . .

RUN npm install
RUN npm run build
RUN npm install -g serve

EXPOSE 5001

CMD ["serve","-s","-l","5001","build"]