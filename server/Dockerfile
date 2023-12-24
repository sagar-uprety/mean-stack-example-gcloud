FROM --platform=linux/amd64 node:17-slim 
WORKDIR /usr/app

# Install dependencies and build the project.
COPY package.json package-lock.json ./
RUN npm install
COPY . .
RUN npm run build

# Expose port 5200
EXPOSE 5200

# Run the web service on container startup.
CMD ["node", "dist/server.js"]
