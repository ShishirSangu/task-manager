FROM node:18-alpine

# Set work directory
WORKDIR /app

# Install dependencies first (for Docker layer caching)
COPY package.json package-lock.json* ./
RUN npm install

# Copy rest of the app
COPY . .

# Expose Vite's default port
EXPOSE 5173

# Keep container running (you'll start npm manually)
CMD ["tail", "-f", "/dev/null"]
