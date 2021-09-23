# AmlApp

An Async AML Sanction Status Check Application

Its uses in memeory H2 Database

#Start RabitMQ
Go to in the Application Root Folder

cd rabbitmq
docker-compose up
To get RabbitMQ running in a container

#Start Application


cd in root directory of the app

mvn install

docker build -t amlapplication .

docker run -p 9000:8080

docker push amlapplication 

#Architectural Diagram

![image](https://user-images.githubusercontent.com/70537453/134481904-0a1c4883-e1a5-4bd7-b74f-82020cf7e247.png)

#Testing

Run 
mvn test

#Scaling Architecture Diagram

Scale By Deploying the RabbitMQ container and AMLAPP to Kubernetes and Maintain High Availablity

Fault Tolerance Use Hystrix , and Eureka Service Discovery

Monitoring Use ELK Stack
