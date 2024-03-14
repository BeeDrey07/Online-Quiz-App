FROM node:18-alpine as BUILD_IMAGE

WORKDIR /usr/src/app

COPY package.json .
# COPY package-lock.json .  
# COPY vite.config.js .

RUN npm install

COPY . .

RUN npm run build

# FROM node:18-alpine as PRODUCTION_IMAGE
# WORKDIR /usr/src/app

# COPY --from=BUILD_IMAGE /usr/src/app/dist ./dist

# COPY package.json .
# COPY vite.config.js .

# RUN npm install --production

EXPOSE 8080

CMD ["npm", "run", "dev"]
