FROM node:20

WORKDIR /usr/src/app

COPY package.json ./

RUN npm install --force

COPY . .

EXPOSE 3000

CMD ["node", "app.js"]