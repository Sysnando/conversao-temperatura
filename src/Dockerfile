ARG TAG=latest
FROM node:$TAG
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 8080

RUN chmod +x ./start.sh
ENTRYPOINT ["./start.sh"]
#CMD ["node", "server.js"]