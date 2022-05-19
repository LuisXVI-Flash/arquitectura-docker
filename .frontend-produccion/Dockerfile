FROM node:16

WORKDIR /usr/src/app

COPY package.json .

RUN npm install
RUN npm install --save-dev @angular-devkit/build-angular
RUN npm install -g @angular/cli@latest
RUN ng config -g cli.warnings.versionMismatch false

COPY . .
RUN ng build --configuration production

CMD ng serve --configuration production --host 0.0.0.0