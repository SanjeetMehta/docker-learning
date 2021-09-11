# AS helps us to name the stage of the docker process, in this case 'builder' is 1st stage
FROM node:alpine AS builder 
WORKDIR '/usr/app'
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

# Second FROM terminates the eariler block
FROM nginx
COPY --from=builder '/usr/app/build' '/usr/share/nginx/html'