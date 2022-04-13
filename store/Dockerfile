FROM node:alpine

RUN mkdir -p /usr/site/app
ENV PORT 3000

WORKDIR /usr/site/app

COPY package.json /usr/site/app
COPY yarn.lock /usr/site/app

# Production use node instead of root
# USER node

RUN yarn install --production

COPY . /usr/site/app

RUN yarn build

EXPOSE 3000
CMD [ "yarn", "start" ]