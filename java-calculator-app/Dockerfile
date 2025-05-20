FROM openjdk:11-jre-slim

# Set the working directory
WORKDIR /app

# Copy the Maven project files
COPY pom.xml .
COPY src ./src

# Package the application
RUN ./mvnw clean package -DskipTests

# Copy the jar file to the image
COPY target/java-calculator-app-1.0-SNAPSHOT.jar app.jar

# Command to run the application
ENTRYPOINT ["java", "-jar", "app.jar"]