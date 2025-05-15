# Use an official Node.js runtime as a parent image
FROM public.ecr.aws/lambda/nodejs:14

# Set the working directory in the container
WORKDIR /var/task

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy both service files to the working directory
COPY appointment-service.js patient-service.js index.js ./

# Command to run the application
CMD ["index.handler"]

