# Use lightweight Node.js image
FROM node:22-alpine

# Set working directory inside container
WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm ci --only=production

# Copy app source code
COPY . .

# Expose port (matches app.js)
EXPOSE 3000

# Command to start the app
CMD ["node", "app.js"]
