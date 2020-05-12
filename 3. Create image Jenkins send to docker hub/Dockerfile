FROM jenkins/jenkins:lts
USER root
RUN apt-get update
RUN apt-get install -y mc
RUN apt-get install -y curl
RUN apt-get install -y hwinfo
RUN apt-get install -y busybox
RUN apt-get install -y iputils-ping

RUN apt-get update
RUN apt-get -y install apt-transport-https ca-certificates curl gnupg2 software-properties-common
RUN curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add -
RUN add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian $(lsb_release -cs) stable"

RUN apt-get update
RUN apt-get -y install docker-ce

RUN usermod -a -G docker jenkins

USER jenkins