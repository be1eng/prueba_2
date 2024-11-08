FROM node:20

WORKDIR /usr/src/app

# Configura el registro de npm y copia los archivos de dependencias
RUN npm set registry https://registry.npmjs.org/
COPY package*.json ./

# Instala las dependencias con un timeout extendido
RUN npm install --only=production --timeout=100000

# Copia el resto del código de la aplicación
COPY . .

EXPOSE 8080
CMD ["npm", "start"]
