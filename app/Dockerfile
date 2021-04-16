# For arm64 build
FROM node:14@sha256:00e90d6cbb499653cd2c74a3770f4fa5982699145b113e422bdffe31a7905117
# For amd64 build
#FROM node:14@sha256:0bb7063dae2d6e3e6989f1c2348a50c03bc9d9c1e2f7ea6a0a36e9f0728ac78e

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./

RUN npm install
# If you are building your code for production
# RUN npm ci --only=production

# Bundle app source
COPY . .

EXPOSE 3000

# Run container as non root user for more security
USER node

CMD [ "node", "server.js" ]