FROM ubuntu:latest

RUN apt-get update \
    && apt-get install maven -y \
    && apt-get install git -y

WORKDIR /home/
RUN git clone https://github.com/Vikas-tm/samplejavacode.git
WORKDIR /home/samplejavacode/
RUN  mvn package

RUN mkdir /home/war && cp /home/samplejavacode/target/addressbook.war /home/war/
RUN ls /home/war
