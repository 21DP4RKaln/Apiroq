FROM node:18-alpine

WORKDIR /app

ARG CACHEBUST=1

COPY package*.json ./

RUN npm cache clean --force && \
    rm -rf node_modules && \
    npm install web-vitals && \
    npm install

COPY . .

EXPOSE 3000

CMD ["npm", "start"]