FROM node:latest

#Create app directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# We copy just the requirements.txt first to leverage Docker cache
COPY package.json /usr/src/app

CMD [ "npm", "start" ]