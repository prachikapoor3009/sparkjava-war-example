# Use the official OpenJDK image as the base image
FROM openjdk:11-jre-slim
# Set the working directory inside the container
WORKDIR /app
# Copy the Spark Java application WAR file into the container
ADD . /app
# Replace 'your-app.war' with the actual file name
# Expose the port your application will run on
EXPOSE 8080
# Specify the command to run your Spark Java application using Jetty
CMD ["java", "-war", "sparkjava-hello-world-1.0.war"]
