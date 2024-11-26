# Use the official Node.js image as the base image
FROM node:18

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json first (for caching npm install step)
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application files
COPY . .

# Ensure Cypress binaries are installed
RUN npx cypress install

# Set environment variables (optional)
ENV NODE_ENV=production
ENV PORT=3000

# Expose the port your application runs on
EXPOSE 3000

# Start the application (replace with your app's start command if different)
CMD ["npm", "start"]
