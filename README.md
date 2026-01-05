# Azure Docker Web App

A simple Dockerized web application deployed on Microsoft Azure using Azure App Service.

## Tech Stack

- Azure App Service
- Azure Container Registry
- Docker
- Nginx
- HTML

## Architecture

```
User -> Azure App Service -> Docker Container -> Azure Container Registry
```

## Project Structure

```
azure-docker-webapp/
|
+-- app/
|   +-- index.html
|
+-- Dockerfile
+-- .dockerignore
+-- README.md
+-- screenshots/
    +-- azure-app-service-running.png
```

## Steps to Run Locally

### Prerequisites
- Docker installed on your system
- Basic knowledge of Docker commands

### Build the Docker Image

```bash
docker build -t azure-docker-webapp .
```

### Run the Container

```bash
docker run -d -p 8080:80 azure-docker-webapp
```

Access the application at: http://localhost:8080

## Azure Deployment Steps

1. Created Azure Container Registry - Push Docker images to ACR
2. Tagged Docker Image - Prepared image for ACR push
3. Pushed Image to ACR - docker push <registry-name>.azurecr.io/azure-docker-webapp
4. Created Azure App Service - Selected Docker container option
5. Configured Image Source - Linked ACR as image source
6. Deployed and Accessed - Website live via Azure App Service URL

## Environment Variables

None required for this basic deployment.

## Key Features

✓ Lightweight Nginx-based container
✓ Clean, professional Dockerfile
✓ Ready for Azure App Service deployment
✓ Proper repository structure for DevOps roles
✓ Real deployment proof with screenshots

## What Interviewers Look For

✓ Proper repo structure
✓ Clear README documentation
✓ Dockerfile clarity and best practices
✓ Azure knowledge proof
✓ Real deployment screenshots

## Future Enhancements

Potential upgrades to this project:

- CI/CD using GitHub Actions
- Flask application instead of static HTML
- Private ACR authentication with managed identities
- Terraform for infrastructure-as-code
- Azure DevOps pipelines integration
- Custom domain and SSL/TLS configuration

## Author

Dhanush S M

## License

MIT License - Feel free to use this project for learning purposes.
