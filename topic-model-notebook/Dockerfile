
FROM python:3.12-slim

RUN apt-get update --fix-missing
RUN apt install -y git gcc g++
RUN apt-get install ffmpeg -y
RUN apt-get install flac

RUN pip install jupyter
WORKDIR /jupyter

COPY requirements.txt /jupyter/requirements.txt
RUN pip install -r requirements.txt 

WORKDIR /jupyter
ADD . /jupyter
