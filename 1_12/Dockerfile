FROM ubuntu:24.04

WORKDIR /1_12

RUN apt-get update && apt-get install -y curl

RUN curl -sL https://deb.nodesource.com/setup_16.x | bash && apt-get install -y nodejs

COPY . .

RUN npm install -g serve

RUN npm install

RUN npm run build

EXPOSE 5001

CMD ["serve","-s","-l","5001", "build"]



