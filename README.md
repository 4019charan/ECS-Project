# Node.js & MongoDB on AWS ECS

This project deploys a Node.js application alongside a MongoDB database using AWS ECS with Fargate. The architecture leverages the AWS Cloud ecosystem for a scalable and robust deployment.

![Architecture Diagram](https://github.com/4019charan/ECS-Project/blob/main/ECS-Project2.jpeg)

## Architecture Overview

The architecture is designed for high availability and scalability, including:

- **Amazon ECS (Elastic Container Service):** Runs Docker containers managed by Fargate, which abstracts the server management.
- **Application Load Balancer (ALB):** Distributes incoming application traffic across multiple containers.
- **Amazon CloudWatch:** Monitors the application and logs the events for troubleshooting and analytics.
- **VPC & Public Subnet:** Ensures network security and connectivity to the Internet.
- **AWS ECR (Elastic Container Registry):** Stores the Docker images used by ECS.

## Project Components

- `server.js`: The main Node.js server file that serves the application logic.
- `Dockerfile`: Instructions for Docker to build the Node.js application image.
- `docker-compose.yml`: Defines the multi-container setup for local testing.
- `ecs-task-definition.json`: The task definition file for AWS ECS deployment.

## How to access
-  so if you run locally you could see the webpage at 'localhost:3000'
-  To add the data you should visit 'localhost:3000/add' (Please refer to server.js for all other api's)

## Deployment Steps

1. Push the Node.js application Docker image to ECR.
2. Create an ECS cluster and configure the VPC and subnets.
3. Define an ECS task using the task definition JSON.
4. Run the task or service with the Application Load Balancer.
5. Monitor the application using Amazon CloudWatch.

## Local Development

To run the application locally, ensure Docker is installed and use:

docker-compose up --build

## Contributions

Contributions are welcome. Please fork the repository and submit a pull request.

