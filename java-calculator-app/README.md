# Java Calculator Application

This is a simple Java-based calculator application that performs basic arithmetic operations such as addition, subtraction, multiplication, and division. The application is built using Maven and is designed to be easily deployable using Docker and Kubernetes.

## Features

- Basic arithmetic operations:
  - Addition
  - Subtraction
  - Multiplication
  - Division

## Project Structure

```
java-calculator-app
├── src
│   └── main
│       └── java
│           └── com
│               └── example
│                   └── calculator
│                       └── Calculator.java
│   └── test
│       └── java
│           └── com
│               └── example
│                   └── calculator
│                       └── CalculatorTest.java
├── Dockerfile
├── pom.xml
├── .gitlab-ci.yml
├── sonar-project.properties
├── helm
│   ├── Chart.yaml
│   ├── values.yaml
│   └── templates
│       ├── deployment.yaml
│       ├── service.yaml
│       └── _helpers.tpl
├── README.md
```

## Prerequisites

- Java 11 or higher
- Maven
- Docker
- GitLab CI/CD
- JFrog Artifactory
- Azure Kubernetes Service (AKS)

## Setup Instructions

1. **Clone the repository:**
   ```
   git clone <repository-url>
   cd java-calculator-app
   ```

2. **Build the application:**
   ```
   mvn clean install
   ```

3. **Run the application locally:**
   ```
   mvn spring-boot:run
   ```

4. **Build the Docker image:**
   ```
   docker build -t java-calculator-app .
   ```

5. **Run the Docker container:**
   ```
   docker run -p 8080:8080 java-calculator-app
   ```

## CI/CD Pipeline

The project includes a `.gitlab-ci.yml` file that defines the CI/CD pipeline for building, testing, and deploying the application. The pipeline integrates with SonarQube for static code analysis and uses Trivy and Semgrep for scanning Docker images.

## Deployment

The application can be deployed to Azure Kubernetes Service (AKS) using Helm charts. The Helm chart templates are located in the `helm` directory.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.