FROM ubuntu:20.04
WORKDIR /
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update -y &&\
    apt-get install apt-utils build-essential python3-pip libgtk2.0-dev -y &&\
    pip3 install uwsgi flask flask_restful flask-cors Pillow boto3 requests celery celery[redis] pika redis &&\
    pip3 install flask_jwt_extended uwsgi &&\
    pip3 install pyyaml numpy==1.23.3 scanpy
RUN pip3 install opencv-python
RUN apt-get install libgl1-mesa-glx -y

VOLUME /hostpipe