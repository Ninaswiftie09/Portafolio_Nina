# Frontend/Dockerfile

FROM node:22-alpine

WORKDIR /app

# Copiamos solo los archivos de dependencias para aprovechar la caché
COPY package*.json ./

# Instalamos dependencias
RUN npm install

# Copiamos el resto del código
COPY . .

# Exponemos el puerto de Vite
EXPOSE 5173

# Iniciamos el servidor de desarrollo
CMD ["npm", "run", "dev"]
