FROM node:20.17

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 3060

CMD ["node", "app.js"]