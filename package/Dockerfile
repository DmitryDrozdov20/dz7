FROM alpine
RUN apk update --no-cache \
&& apk add openjdk8 \
&& apk add maven \
&& apk add git \
&& RUN rm -rf /var/cache/apk/*
WORKDIR /home
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
RUN mvn -f ./boxfuse-sample-java-war-hello/pom.xml package
#RUN cp ./boxfuse-sample-java-war-hello/target/hello-1.0.war /usr/local/tomcat/webapps/
#RUN rm -rf ./boxfuse-sample-java-war-hello

#FROM ubuntu:20.04
#RUN apt-get update
#RUN apt-get install default-jdk -y
#RUN apt-get install git -y
#RUN apt-get install maven -y
#WORKDIR /home/new/
#RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
#WORKDIR /home/new/boxfuse-sample-java-war-hello/
#RUN mvn package
