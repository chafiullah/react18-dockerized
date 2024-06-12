FROM node:20.14.0-alpine3.20

# if you don't want to give root access to the image users, define a new user and build the image for that user only
# RUN addgroup developer && adduser -S -G developer chafi
# USER chafi
# if you don't define the user before WORKDIR, you will have permission error
WORKDIR /app

# I forgot to add this line. Due to this there was an error of package.json not found
COPY package*.json .

RUN npm install

COPY . .

EXPOSE 3000

CMD [ "npm","start" ]