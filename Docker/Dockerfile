# Use a specific version of the Node.js image
FROM docker.io/library/node:18.13

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and package-lock.json files to the working directory
COPY package*.json ./

# Install the dependencies
RUN npm install

# Install the Angular CLI
RUN npm install -g @angular/cli

# Uncomment the following line to build the Angular app in production mode
# RUN ng build --configuration=production --output-path=/dist

# Copy the rest of the app files to the working directory
COPY . .

# Expose port 4200 for the Angular CLI development server
EXPOSE 4200

# Define the command to run your Angular application
CMD ["ng", "serve", "--host", "0.0.0.0"]
