# base image
FROM node:17

# set working directory
WORKDIR /usr/src/app

# install and cache app dependencies
COPY package*.json ./
RUN npm install
RUN npm install -g @angular/cli@latest

# add app
COPY . .

# start app
CMD ng serve --host 0.0.0.0