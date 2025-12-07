FROM ubuntu:latest

RUN apt-get update
RUN apt-get upgrade -y

# Python və pip quraşdır
RUN apt-get install -y python3 python3-pip

# EXTERNALLY-MANAGED xətasını düzəltmək üçün
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# pip ilə flask quraşdır
RUN pip3 install flask
RUN pip3 install flask-cors

# İş qovluğu
WORKDIR /app

# api.py faylını konteynerə kopyala
COPY ./api.py /app/api.py

# konteyner işə düşəndə flask serveri başlasın
CMD ["python3", "api.py"]

