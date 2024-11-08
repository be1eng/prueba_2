FROM node:20

WORKDIR /usr/src/app

# Copia solo package.json y package-lock.json
COPY package*.json ./

# Instala dependencias
RUN npm install

# Copia el resto del código
COPY . .

EXPOSE 8080
CMD [ "npm", "start" ]
