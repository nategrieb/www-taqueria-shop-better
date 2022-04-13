FROM node:alpine

RUN mkdir -p /app/
ENV PORT 3000

WORKDIR /app/

COPY package.json /app/
COPY turbo.json /app/
COPY yarn.lock /app/
COPY site/ /app/site/
COPY packages/ /app/packages/

RUN yarn
# remove comment for production
# RUN yarn build

COPY . /app/

# use for production instead of dev
EXPOSE 3000
CMD [ "yarn", "start" ]
# CMD yarn next dev -p 8000