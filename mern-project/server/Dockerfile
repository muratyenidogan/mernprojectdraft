# Use the official Node.js image as the base image
FROM node:18

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json for dependency installation
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application files to the container
COPY . .

# Set environment variables (if needed, optional)
# Ensure .env is copied to the container runtime, or mount it during container execution
ENV NODE_ENV=production

# Expose the port your server runs on (adjust as needed)
EXPOSE 5050

# Run the server
CMD ["node", "server.mjs"]
