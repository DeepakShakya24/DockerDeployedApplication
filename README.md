# DockerDeployedApplication
In this basically I basically push some file that are required for Docker based deployment of my Django Application.

So for deployment of Django application on Docker you need to follow some steps--
1.)On your AWS EC2 Ubuntu instance install docker via command (sudo apt-get install docker.io)
2.)Then clone your this project which contains django application,Dockerfile and requirements.txt
  a.)Dockerfile:It is a executable file which automatically executes all commands which are require for docker setup like docker image and setup directory inside your container which holds your project
  b.)requirements.txt:It contains all the dependencies which you need to install for your django application inside your container.
3.)Now run your Dockerfile via command (sudo docker build . -t <image-name>),this will create docker image you can see your image via command (sudo docker images)  
4.)Now run that image which eill create a container which contains your django application via command (sudo docker run -p 8000:8000 -i -t <image-name>).
5.)Now copy AWS instance public ipv4 address over browser and open that on port 8000 for eg.)0.0.0.0:8000
6.)Your django based application is now successfully deployed over Docker container.


You can push over image over Docker-Hub which is same as Github but it is a repository of Docker images.

You can use my Docker image by simple command:
docker pull deeptech/weather-image.




