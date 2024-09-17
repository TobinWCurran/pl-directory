FROM node:14.16-alpine

RUN mkdir -p /usr/src/pld-client

WORKDIR /usr/src/pld-client

# add `/app/node_modules/.bin` to $PATH
# ENV PATH /usr/src/pld-client/node_modules/.bin:$PATH

COPY ./package.json ./
COPY ./yarn.lock ./

RUN yarn

COPY . .

EXPOSE 3000

CMD ["yarn", "start"]
