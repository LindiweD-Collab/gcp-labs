# Use an official Node runtime as the parent image
FROM node:lts

# Set the working directory
WORKDIR /app

# Copy the current directory contents into the container
ADD . /app

# Make port 80 available
EXPOSE 80

# Run app.js
CMD ["node", "app.js"]
