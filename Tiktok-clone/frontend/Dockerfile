#Use node official runtime as the base image
FROM node:22-alpine AS build

#Create a working directory
WORKDIR /app

#Copy and install dependencies
COPY package.json package-lock.json /app/
RUN npm install

#Copy the rest of the application
COPY . .

#Final stage of the application
FROM gcr.io/distroless/base

#Copy the application
COPY --from=build . .

#Expose port
EXPOSE 3001

#Run the application
CMD [ "npm", "start" ]

