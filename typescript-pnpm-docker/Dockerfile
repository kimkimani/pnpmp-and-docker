# Use an official Node.js  and it shoud be version 16 and above
FROM node:20-alpine
# Set the working directory in the container
WORKDIR /app
# Copy package.json and pnpm-lock.yaml
COPY pnpm-lock.yaml package.json ./
# Install app dependencies using PNPM
RUN npm install -g pnpm
# Install dependencies
RUN pnpm i 
# Copy the application code 
COPY . .
# Build the TypeScript code
RUN pnpm run build
# Expose the app
EXPOSE 3000
# Start the application
CMD ["pnpm", "start"]