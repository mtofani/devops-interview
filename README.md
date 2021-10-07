# DevOps Interview - mtofani

 ## DockerFile utilizado.
 ```
FROM ubuntu:18.04

RUN apt update

RUN apt install -y openjdk-8-jre-headless git wget

RUN mkdir /test && cd /test && wget https://7-414614942-gh.circle-artifacts.com/0/build/libs/spring-boot-0.0.1-SNAPSHOT.jar

CMD java -jar /test/spring-boot-0.0.1-SNAPSHOT.jar

```
## Comandos para correr los microservicios

1. cd al folder donde tenemos el archivo DockerFile
2. sudo docker build -t springboot .
3. sudo docker run springboot -p 8888:8080

Deberiamos tener un output como el siguiente:

![image](https://user-images.githubusercontent.com/69044164/136429761-4d578941-54a4-4191-8ed5-1b7ff687837e.png)

*Localmente por wget o browser*
![WhatsApp Image 2021-10-07 at 1 26 47 PM](https://user-images.githubusercontent.com/69044164/136429844-d1fb2ed7-067a-4202-b245-2d4d9f175a0c.jpeg)



*Saludos!*
