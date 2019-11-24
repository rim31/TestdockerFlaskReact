FROM ubuntu:latest

#Create app directory
RUN apt-get update -y
RUN apt-get install -y python-pip python-dev build-essential

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# We copy just the requirements.txt first to leverage Docker cache
COPY requirements.txt /usr/src/app

RUN pip install -r requirements.txt

ENTRYPOINT ["flask"]
CMD [ "npm", "--host=0.0.0.0" ]