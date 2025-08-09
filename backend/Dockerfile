FROM node:20-alpine
WORKDIR /app

# Install dependencies first
COPY package.json package-lock.json* ./
RUN npm ci --production

# Copy the rest of the backend source code
COPY . .

ENV NODE_ENV=production
EXPOSE 5000

CMD ["node", "server.js"]