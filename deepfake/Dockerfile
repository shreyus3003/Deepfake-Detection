FROM python:3.7

#RUN apt update && apt upgrade -y && apt install -y cmake
RUN apt-get update && apt-get upgrade -y && apt-get install -y cmake && apt-get install -y libavcodec-dev && apt-get install -y libavformat-dev && apt-get install -y libavutil-dev && apt-get install -y libswscale-dev

WORKDIR ~/deepfake
COPY requirements.txt /tmp/

RUN pip3 install -r /tmp/requirements.txt

COPY Deepfake_App/ .

ENTRYPOINT ["python3", "./app.py"]
