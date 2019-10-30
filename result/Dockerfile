FROM node:12.10.0
EXPOSE 80
WORKDIR /usr/result
COPY . .
RUN npm install
CMD [ "node", "server.js" ]