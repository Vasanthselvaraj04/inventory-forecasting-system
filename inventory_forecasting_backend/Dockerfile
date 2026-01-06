# Use Java 21
FROM eclipse-temurin:21-jdk

# Working directory inside container
WORKDIR /app

# Copy Maven wrapper and pom
COPY . .

# Build Spring Boot app
RUN ./mvnw clean package -DskipTests || mvn clean package -DskipTests

# Run the JAR
CMD ["java", "-jar", "-Dspring.profiles.active=docker", "target/inventory-0.0.1-SNAPSHOT.jar"]



