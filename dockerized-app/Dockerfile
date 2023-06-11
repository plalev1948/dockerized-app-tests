## These lines of code represent the image we're going to use along with copying the contents of the current directory into the container.

FROM node:18-alpine
WORKDIR /dockerized-app-tests
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"]