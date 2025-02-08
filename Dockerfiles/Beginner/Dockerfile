# Use OpenJDK image
FROM openjdk:17-jdk-slim
WORKDIR /app
COPY target/*.jar app.jar
CMD ["java", "-jar", "app.jar"] 

#######################################

# Use Node.js base image
FROM node:18
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
CMD ["npm", "start"]

######################################

# Use official Node.js base image
FROM node:18
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
CMD ["node", "server.js"]