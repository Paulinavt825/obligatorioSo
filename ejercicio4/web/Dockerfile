# Usa una imagen oficial de Node.js como imagen base
FROM node:25-alpine

# Establece el directorio de trabajo en el contenedor
WORKDIR /app

# Copia package.json y package-lock.json (si está disponible)
COPY package*.json ./

# Instala las dependencias de la aplicación
RUN npm install

# Copia el resto del código fuente de la aplicación
# web/ (máquina host) -> app/ (contenedor)
COPY . .

# Hace que el puerto 5000 esté disponible para el exterior del contenedor
EXPOSE 5000

# Define el comando para ejecutar la aplicación
CMD ["npm", "start"]
