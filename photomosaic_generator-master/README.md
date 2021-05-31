# Collage mosiac generator

A python program that takes one main image and tens of other filler images to form a photomosaic of the main image consisting of the filler images as tiles. Provides the option to set the resolution of individual tiles that make up the photomosaic and also control the sampling resolution of the final output.


<div align="center">
    <img src="https://camo.githubusercontent.com/2eb9b58751f799866d7498598faabc3cdee5ba14aff6ad3e08b08ac46c840bdf/68747470733a2f2f636f6465626f782e6e65742f6173736574732f696d616765732f6d6f736169632f6d6f736169635f64657461696c2e6a7067">
</div>

# Documentation 

Running Docker For Photomosaic Generator

>>docker pull iraiva/photomosaic_generator  //This will pull the docker image.
>>docker run -it iraiva/photomosaic_generator //It generates the docker ID(eg.863c2ea692c5)

To start the same container ID 
>>docker start 863c2ea692c5

Now we need to copy the image from the local machine to the docker container 
To copy the image, we need to exit the container
>>EXIT the container by either typing exit or "ctrl+D"
Go to the directory where the required image is present.
>>docker cp img.jpg 863c2ea692c5:/opt/main_image/img.jpg
NOTE: Please don't change the(/opt/main_image/img.jpg) this part.

After copying,
>>docker exec -it 863c2ea692c5 /bin/bash

You'll be directed to the container.

Now to install python in the container 

>>apt -y update
>>apt-get -y install software-properties-common
>>add-apt-repository ppa:deadsnakes/ppa
>>apt-get -y update
>>apt-get -y install python3.6
>>update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.6 1
>>update-alternatives --config python3
>>python3 --version
# Install pip for python3.6
>>apt -y install wget
>>wget https://bootstrap.pypa.io/get-pip.py
>>python3.6 get-pip.py
>>pip --version

To install openCV
>>apt-get install python3-opencv
To install Pillow
>>apt-get install python3-pillow
To install Numpy
>>apt-get install python3-numpy

After Installing all these,
>>cd /opt
>>python photomosaic_generator.py

Finally the code works,

to check the output
>>ls -l


 

# Project Overview 

As this is a small project, there is no project plan as such. The developers can try to complete this project according to their thought process. 

# Contributing

Help us improve the project.

Ways you can help:

1. Choose from the existing issue and work on those issues.
2. Feel like the project could use a new feature, make an issue to discuss how it can be implemented and work on it.
3. Find a bug create an Issue and report it.
4. Review Issues or Merge Requests, give the developers the feedback.
5. Fix Documentation.
___

