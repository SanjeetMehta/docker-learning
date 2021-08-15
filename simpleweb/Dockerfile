# Specify a base image
FROM node:alpine

WORKDIR /usr/app

# Only copy package.json
COPY ./package.json ./

# Install some dependencies
RUN npm install

# Copy current directory into container
COPY ./ ./

# Default command
CMD ["npm", "start"]