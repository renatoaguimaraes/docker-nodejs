FROM centos:7

MAINTAINER "renato.guimaraes" renatoaguimaraes@gmail.com

ADD epel.repo /etc/yum.repos.d/

RUN yum -y install nodejs npm

RUN npm install pm2 -g

ADD app.zip /opt/

RUN yum -y install unzip

RUN unzip /opt/app.zip -d /opt/server

WORKDIR /opt/server

RUN npm install

EXPOSE 80 

EXPOSE 4000

CMD ["pm2", "start", "-x", "/opt/server/app.js", "--no-daemon"]
