# Use the latest Ubuntu as the base image
FROM ubuntu

# Update and upgrade APT
RUN apt-get update && apt-get upgrade -y

RUN apt-get install -y python3 python3-pip python3-venv

WORKDIR /app

RUN python3 -m venv venv

RUN . venv/bin/activate && pip install flask

COPY . .
EXPOSE 5252


CMD [ "venv/bin/python3", "api.py" ]
