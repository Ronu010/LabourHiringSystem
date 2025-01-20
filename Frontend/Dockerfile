# Use Node.js official image as the base image
FROM node:16

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install the dependencies
RUN npm install

# Install serve to serve the static files
RUN npm install -g serve

# Copy the rest of the application files
COPY . .

# Build the React application
RUN npm run build

# Expose port 3000 for the React app
EXPOSE 3000

# Serve the React app using serve
CMD ["serve", "-s", "build"]
