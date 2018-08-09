FROM node

WORKDIR /server

COPY  ./package.json ./

RUN npm i -g yarn 
RUN yarn install --production

COPY ./ormconfig.json .
COPY ./dist ./
COPY ./.env.production ./


WORKDIR ./

ENV NODE_ENV production

EXPOSE 4000

CMD ["node", "dist/index.js"]
