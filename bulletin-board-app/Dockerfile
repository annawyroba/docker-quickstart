# Start with FROM docker image (use from Docker Hub)
FROM node:current-slim

# WORKDIR is a path created in container
WORKDIR /usr/src/app

# COPY from path that begins with this directory to one in container (in this case . is set to WORKDIR /usr/src/app)
COPY package.json .

# RUN command after copying package.json
RUN npm install

# EXPOSE set on what port project is locally available
EXPOSE 8080

# CMD runs command after set up
CMD [ "npm", "start" ]

# Copy everything else from this directory to path in container (in this case . is set to WORKDIR /usr/src/app)
COPY . .

# When running container
# docker container run --publish 8000:8080 --detach --name bb bulletinboard:1.0
# flag --publish set up on what port api will be available

# To enter the container
# docker exec -it bb /bin/bash