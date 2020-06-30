# Dockerfile
Dockerfile to create a complet machine learning enironment. 
## Machine Learning container:
This container has all the necessary tools to create machine learning systems with python and AWS. It includes the following frameworks and packages:
- python 3.6
- opencv
- dlib
- face-recognition
- jupyter
- boto3
- scikit-learn
- tensorflow
- pytorch 
- gym
- baselines
- Keras
- matplotlib
- stable-baselines
- pandas

## Instructions 
You have two choices, one is pulling the image from the docker hub, and the other option is to build the image with the Dockerfile. 

### Option 1: (Recommend) Install the image.


To install the image, it is necessary to download the next repository:
```sh
$ docker pull gfdfranco/ml_env
```
The next command allows you run the container:
```sh
$ docker run -it --name CONATINER_NAME -v FOLDER_DIRECTORY:/root/workspace -e DISPLAY=XLAUNCH_IP:0.0 gfdfranco/ml_env
```
Example:
```sh
$ docker run -it --name ml -v /c/Users/gfdge/Documents/ml_folder:/root/workspace -e DISPLAY=192.168.56.1:0.0 gfdfranco/ml_env
```
To open the container again you could use:
```sh
$ docker start -ai ml
```


### Option 2: (Dockerfile ) Build the image.
Once that you downloaded the repository and you are into dockerfile directory is necessary to execute the next command:
```sh
$ docker build -t ml_env .
```
To run the container will assign a volume to share files between the container and PC, it will have an interactive session and will have the capacity  DISPLAY command if you want to view screens.
```sh
$ docker run -it --name CONATINER_NAME -v FOLDER_DIRECTORY:/root/workspace -e DISPLAY=XLAUNCH_IP:0.0 ml_env
```
Example:
```sh
$ docker run -it --name ml -v /c/Users/gfdge/Documents/ml_folder:/root/workspace -e DISPLAY=192.168.56.1:0.0 ml_env
```
To open the container again you could use:
```sh
$ docker start -ai ml
```


