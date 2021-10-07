# DevOps Interview - mtofani

 ## DockerFile utilizado.
FROM ubuntu:18.04

RUN apt update

RUN apt install -y openjdk-8-jre-headless git wget

RUN mkdir /test && cd /test && wget https://7-414614942-gh.circle-artifacts.com/0/build/libs/spring-boot-0.0.1-SNAPSHOT.jar

CMD java -jar /test/spring-boot-0.0.1-SNAPSHOT.jar

## Comandos para correr los microservicios
- *cd* al folder donde tenemos el DockerFile
> sudo docker build -t springboot 
> sudo docker run springboot -p 8888:8080

Deberiamos tener un output como el siguiente:

![image](https://user-images.githubusercontent.com/69044164/136428989-6c1bfc7c-771f-45f3-a57e-1d5e9ad92e42.png)
