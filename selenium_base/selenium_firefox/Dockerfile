FROM ubuntu

ENV VERSION 2.44.0

RUN apt-get update
RUN apt-get install -y software-properties-common
RUN add-apt-repository ppa:webupd8team/java
RUN apt-get update
RUN echo debconf shared/accepted-oracle-license-v1-1 select true | debconf-set-selections
RUN echo debconf shared/accepted-oracle-license-v1-1 seen true | debconf-set-selections
RUN apt-get install oracle-java7-installer -y
RUN wget http://selenium-release.storage.googleapis.com/${VERSION%.*}/selenium-server-standalone-${VERSION}.jar
RUN apt-get install firefox xvfb -y
ADD register-node.sh /var/register-node.sh
RUN chmod 755 /var/register-node.sh

CMD ["/bin/bash", "/var/register-node.sh"]