#building
FROM node:18

LABEL "name"="dov-bear"

ARG APP_DIR=/app 
ARG PORT=3000
ARG INSTANCE_NAME
ARG INSTANCE_HASH

RUN mkdir $APP_DIR

WORKDIR $APP_DIR

ADD main.js . 
ADD package.json . 
ADD package-lock.json .
ADD public public
ADD views views

RUN npm ci

#running 
ENV PORT=3000

EXPOSE $APP_PORT

ENTRYPOINT [ "node", "main.js" ]
