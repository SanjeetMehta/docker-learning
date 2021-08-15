# Specify a base image
FROM node:alpine

WORKDIR /usr/app

# Copy current directory into container
COPY ./ ./

# Install some dependencies
RUN npm install

# Default command
CMD ["npm", "start"]